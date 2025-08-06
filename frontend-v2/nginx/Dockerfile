FROM nginx:latest

COPY nginx.conf /etc/nginx/nginx.conf

COPY dist /usr/share/nginx/html

EXPOSE 8080

COPY setup.sh /usr/local/bin/setup.sh

ENTRYPOINT ["./setup.sh"]

CMD ["nginx", "-g", "daemon off;"]