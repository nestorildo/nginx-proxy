# nginx-proxy
## Docker manifest for nginx reverse proxy and letsencrypt containers
Usage: docker-compose -f nginx-proxy.yaml up -d

Notes: Separate nginx containers configured with domain variables for virtual host, ssl and forwarding

''''
CONTAINER ID   IMAGE                                    COMMAND                  CREATED          STATUS          PORTS                                                                      NAMES
8628a7a7203c   jwilder/nginx-proxy:alpine               "/app/docker-entrypo…"   20 minutes ago   Up 20 minutes   0.0.0.0:80->80/tcp, :::80->80/tcp, 0.0.0.0:443->443/tcp, :::443->443/tcp   nginx-proxy
28a4b8a4454d   jrcs/letsencrypt-nginx-proxy-companion   "/bin/bash /app/entr…"   20 minutes ago   Up 20 minutes
