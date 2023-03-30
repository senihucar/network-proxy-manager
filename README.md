# nginx-proxy-manager

port 80 : application using for forwarding  <br />
port 81: application WEB GUI <br />
port 82: phpmyadmin web gui for MYSQL <br />

<br />
###EXAMPLE Structure for using nxinxproxyman docker network<br />
version: '3.9'<br />
services:<br />
  example-nginx-container:<br />
    image: nginx:latest<br />
    ports:<br />
      - 8101:80<br />
    networks:<br />
      - wp-proxynet<br />
networks:<br />
  wp-proxynet:<br />
    external:<br />
      name: nginxproxyman<br />
