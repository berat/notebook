## Server

1- Delete port in ubuntu server 

``` bash
  sudo fuser -k 80/tcp
```

2- Restart to nginx service

``` bash
  sudo service nginx restart
```

3- Configre to nginx .conf file

``` bash
  nano /etc/nginx/sites-available/defaul
```

4- start to next.js project with pm2 on ubuntu server

``` bash
  pm2 start npm --name "nextProject" --start --watch
```

5- My config .conf file

``` bash
server {
	server_name davetiyem.co www.davetiyem.co;
	location / {
		proxy_pass http://localhost:3000;
		proxy_http_version 1.1;
		proxy_set_header Upgrade $http_upgrade;
		proxy_set_header Connection 'upgrade';
		proxy_set_header Host $host;
		proxy_cache_bypass $http_upgrade;
	}
}
```

