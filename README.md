# nginx-proxy-manager

port 80 : application using for forwarding
port 81: application WEB GUI
port 82: phpmyadmin web gui for MYSQL


###EXAMPLE Structure for using nxinxproxyman docker network
version: '3.9'
services:
  example-nginx-container:
    image: nginx:latest
    ports:
      - 8101:80
    networks:
      - wp-proxynet
networks:
  wp-proxynet:
    external:
      name: nginxproxyman
