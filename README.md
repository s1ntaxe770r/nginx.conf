# nginx.conf
Nginx config files for various use cases.Because i never remember the syntax


## Basic 

```
server {
        listen 80;
	listen [::]:80;
	root /enter/path/to/html;
	index index.html index.htm;
	server_name cooldomai.xyz;

	location / {
	try_files $uri $uri/ =404;						        
	}
					
}

```

## Revrse Proxy Basic

```
server {
    listen 80;
    server_name www.example.com example.com;
    location /app {
	proxy_pass http://127.0.0.1:8080;
	}
	
}

```
