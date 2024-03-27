FROM ubuntu:latest  

FROM nginx:alpine3.17

COPY . /usr/share/nginx/html

# Assuming your images are in a folder named "images" within your project directory
COPY images /usr/share/nginx/html/images


EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]



