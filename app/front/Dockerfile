FROM nginx:latest

COPY ./app/front /usr/share/nginx/html

WORKDIR /usr/share/nginx/html

ENV WS_BACK_URL=http://backend-service:8080

COPY ./app/front/entrypoint.sh /entrypoint.sh

RUN chmod +x /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]

# Expose port 80 to allow external access 
EXPOSE 80
