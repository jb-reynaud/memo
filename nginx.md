## Install & run

```bash
brew install nginx

## Always run in sudo
sudo brew services start nginx
```

## Configure a website

1. Update hosts file
```diff
# /etc/hosts
+ 127.0.0.1 local.my-website.fr
```

2. Add vhost
- In `/usr/local/etc/nginx/servers` 
- or  in `/usr/local/etc/nginx/site_available` with a `ln -s` in `site_enabled

```
server {
     server_name local.my-website.fr; # Same as hosts file
     root /usr/local/var/www/data-bo-api/public; # Path to index

     error_log /usr/local/var/log/nginx/my-website-access.log;
     access_log /usr/local/var/log/nginx/my-website-error.log;

     location / {
         try_files $uri /index.php$is_args$args; # It could be app  "/app_local.php$is_args$args;"
     }

     location ~ ^/index\.php(/|$) {
         fastcgi_split_path_info ^(.+\.php)(/.*)$;

         include       fastcgi_params;

         fastcgi_param SCRIPT_FILENAME $realpath_root$fastcgi_script_name;
         fastcgi_pass  127.0.0.1:9000:x
         ;
     }
 }
```

3. Restart
```bash
sudo brew services reload nginx
```
