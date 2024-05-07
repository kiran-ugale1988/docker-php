# docker-php
Practice purpose

https://hub.docker.com/


docker compose up - to run docker container

docker build -t kiran:php81 -f php/Dockerfile .
=> Here kiran:php81 name I have given for build name.

docker ps

docker compose ps

docker ps help

docker compose up -d

docker exec -it docker-php-web-1 sh
=> for interactive shell running


composer init  => to install composer.json file using console.
 and setup composer app

docker compose up --build -d


====================================================
existing nginx file content:


PS C:\docker-study\docker-php> docker exec -it docker-php-web-1 sh
# cat /etc/nginx/conf.d/default.conf

server {
    listen       80;
    listen  [::]:80;
    server_name  localhost;

    #access_log  /var/log/nginx/host.access.log  main;

    location / {
        root   /usr/share/nginx/html;
        index  index.html index.htm;
    }

    #error_page  404              /404.html;

    # redirect server error pages to the static page /50x.html
    #
    error_page   500 502 503 504  /50x.html;
    location = /50x.html {
        root   /usr/share/nginx/html;
    }

    # proxy the PHP scripts to Apache listening on 127.0.0.1:80
    #
    #location ~ \.php$ {
    #    proxy_pass   http://127.0.0.1;
    #}

    # pass the PHP scripts to FastCGI server listening on 127.0.0.1:9000
    #
    #location ~ \.php$ {
    #    root           html;
    #    fastcgi_pass   127.0.0.1:9000;
    #    fastcgi_index  index.php;
    #    fastcgi_param  SCRIPT_FILENAME  /scripts$fastcgi_script_name;
    #    include        fastcgi_params;
    #}

    # deny access to .htaccess files, if Apache's document root
    # concurs with nginx's one
    #
    #location ~ /\.ht {
    #    deny  all;
    #}
}

###################################################
