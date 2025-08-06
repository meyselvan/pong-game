FROM nginx:latest

COPY ./frontend-v2/nginx/nginx.conf /etc/nginx/nginx.conf

COPY ./frontend-v2/pages /usr/share/nginx/html

EXPOSE 8080

COPY ./frontend-v2/nginx/setup.sh /usr/local/bin/setup.sh

ENTRYPOINT ["./setup.sh"]

CMD ["nginx", "-g", "daemon off;"]