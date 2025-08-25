FROM nginx:alpine

# Set working directory inside the container
WORKDIR /usr/share/nginx/html

RUN rm -rf ./*

COPY . .

EXPOSE 80
