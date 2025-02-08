# NGINX Configuration Guide

Este documento fornece instruções para a instalação, configuração e inicialização do servidor NGINX com um conjunto de configurações personalizadas para redirecionamento e proxy reverso.

## Requisitos

- Servidor Linux (Ubuntu recomendado)
- Permissões de superusuário
- NGINX instalado

## Passos de Instalação

### 1. Instalar o NGINX

Execute os comandos abaixo no terminal para instalar o NGINX:

```bash
sudo apt update
sudo apt install nginx -y
```

### 2. Configurar NGINX

#### Arquivo de configuração

Copie o conteúdo abaixo para um novo arquivo de configuração em `/etc/nginx/sites-available/sindipol`:

```nginx
server {
    listen 80;
    server_name _; # Substitua por seu domínio, se houver

    root /var/www/html/sindipol.online/front/dist;
    index index.html;

    location / {
        try_files $uri /index.html;
    }

    error_page 404 /index.html;
}

server {
    listen 81;
    server_name _; # Substitua por seu domínio, se houver

    location / {
        proxy_pass http://localhost:3001; # Porta do container Docker
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}

server {
    listen 82;
    server_name _; # Substitua por seu domínio, se houver

    location / {
        proxy_pass http://localhost:3002;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}

server {
    listen 83;
    server_name _; # Substitua por seu domínio, se houver

    location / {
        proxy_pass http://localhost:3003;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
        proxy_set_header X-Forwarded-Proto $scheme;
    }
}
```

#### Ativar a configuração

```bash
sudo ln -s /etc/nginx/sites-available/sindipol /etc/nginx/sites-enabled/
```

### 3. Testar e Reiniciar o NGINX

Antes de reiniciar o servidor, teste a configuração:

```bash
sudo nginx -t
```

Se tudo estiver correto, reinicie o NGINX:

```bash
sudo systemctl restart nginx
```

### 4. Configurar Firewall (opcional)

Certifique-se de que o firewall permite o tráfego nas portas 80, 81, 82 e 83:

```bash
sudo ufw allow 80
sudo ufw allow 81
sudo ufw allow 82
sudo ufw allow 83
sudo ufw reload
```

### 5. Verificação

Acesse os seguintes endereços em seu navegador para validar:

- [http://seu-dominio-ou-ip:80](http://seu-dominio-ou-ip:80)
- [http://seu-dominio-ou-ip:81](http://seu-dominio-ou-ip:81)
- [http://seu-dominio-ou-ip:82](http://seu-dominio-ou-ip:82)
- [http://seu-dominio-ou-ip:83](http://seu-dominio-ou-ip:83)

## Solução de Problemas

- Se o NGINX não iniciar, verifique os logs:

```bash
sudo tail -f /var/log/nginx/error.log
```

- Certifique-se de que não há outro processo ocupando as portas configuradas:

```bash
sudo lsof -i :80 :81 :82 :83
```

## Conclusão

Este guia configurou um ambiente NGINX com múltiplos servidores virtuais, incluindo suporte a proxy reverso. Certifique-se de personalizar os domínios e caminhos conforme suas necessidades.

