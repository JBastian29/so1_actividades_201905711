## Frontend bug fixed

Este error sucedia puesto que con una aplicación de react.js las rutas se manejan en el frontend por el react-router. Por lo que para solucionar el error es necesario cargar el archivo o ruta principal para que nginx reconozca el archivo. Para se tiene que crear un nginx.conf con lo siguiente:

    server {
        listen       80;
        server_name  localhost;
        location / {
            root   /usr/share/nginx/html;
            index  index.html index.htm;
            try_files $uri /index.html;                 
        }
        error_page   500 502 503 504  /50x.html;
        location = /50x.html {
            root   /usr/share/nginx/html;
        }
    }

Y tambien debemos modificar lo siguiente a nuestro nginx.Dockerfile:


    FROM nginx:1.22.1-alpine as runner
    COPY nginx.conf /etc/nginx/conf.d/default.conf
    COPY --from=compilacion /opt/app/build /usr/share/nginx/html
    EXPOSE 80
    CMD ["nginx", "-g", "daemon off;"]
