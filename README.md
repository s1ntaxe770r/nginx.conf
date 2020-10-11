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


