# Filestash SSL
**Nginx configuration for using SSL with [filestash](https://www.filestash.app/). Try it [here](https://r4v10l1.github.io/filestash-ssl/var/www/html/).**

Check this out too: [r4v10l1/nginx-config](https://github.com/r4v10l1/nginx-config)

### Configuration
You need to edit all `YOUR-DOMAIN` and all `YOUR-USER`. In my case I used a local IP for the domain and it worked so you can try.
```c
./var/www/html/index.html:25:			<button onclick="window.location='https://YOUR-DOMAIN.com/'">Go to filestash</button>
./filestash/docker-compose.yml:7:		- /home/YOUR-USER/filestash/DATA:/app/data/state
./nginx/sites-available/filestash.conf:8:	server_name YOUR_DOMAIN.com;
./nginx/nginx.conf:32:				server_name YOUR-DOMAIN.com;
```
