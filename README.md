# Jellyfin Transmission Docker Compose

This docker compose includes
- [Jellyfin server](https://github.com/jellyfin/jellyfin)
- [Transmission (Torrent Client)](https://github.com/transmission/transmission)
- [File Browser](https://github.com/filebrowser/filebrowser)
- [nginx-certbot](https://github.com/JonasAlfredsson/docker-nginx-certbot)

[nginx-certbot](https://github.com/JonasAlfredsson/docker-nginx-certbot) will act as a reverse proxy, it will generate tls certificates and it will renew certificates automatically.

### Install
#
#### Clone the repo
```sh
git clone https://github.com/madusha98/jellyfin-transmission-docker-compsoe.git
```

#### Edit [nginx.conf](https://github.com/madusha98/jellyfin-transmission-docker-compsoe/tree/main/reverse_proxy)

replace yourdomain.com with your own domain name. 

#### Add your email in docker-compose.yml

add your email in docker-compose.yml for certbot to generate certificates.
```sh
    environment:
      - CERTBOT_EMAIL=youremail@email.com
```

#### That's it. Now you can run your own cloud media server with SSL

```sh
docker-compose up -d
```
