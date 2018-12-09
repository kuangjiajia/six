worker_processes  1;

events {
​    worker_connections  1024;
}


http {
​    include       mime.types;
  	client_max_body_size 20m;

    server {
        client_max_body_size 20m;
        listen 443;
        server_name kuangjiajia.cn;
        ssl on;
        ssl_certificate   cert/214618952130248.pem;
        ssl_certificate_key  cert/214618952130248.key;
        ssl_session_timeout 5m;
        ssl_ciphers ECDHE-RSA-AES128-GCM-SHA256:ECDHE:ECDH:AES:HIGH:!NULL:!aNULL:!MD5:!ADH:!RC4;
        ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
        ssl_prefer_server_ciphers on;
    
        root html;
        index index.html index.htm;
    
        location / {
            client_max_body_size   100m;
            proxy_pass  http://kuangjiajia.natapp1.cc;
            proxy_http_version 1.1;
            proxy_set_header Upgrade $http_upgrade;
            proxy_set_header Connection "upgrade";
            proxy_connect_timeout 300s;
            proxy_send_timeout 300s;
            proxy_read_timeout 300s;
        }
        location /tencentCharity/ {
            alias  /var/www/static/;
            autoindex on;
        }
    }
}