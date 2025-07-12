# Caddy with cloudflare-dns

Custom [caddy] image with [cloudflare-dns]. Detail in [Dockerfile].

## Usage

Docker compose example:

```yaml
volumes:
  caddy_data:
  caddy_config:

services:
  caddy:
    environment:
      - CLOUDFLARE_API_TOKEN=<your cloudflare api token>
    image: 0xjerry/caddy-cloudflaredns
    volumes:
      - ./Caddyfile:/etc/caddy/Caddyfile
      - ./www:/srv
      - caddy_data:/data
      - caddy_config:/config
    ports:
      - 80:80
      - 443:443
    restart: unless-stopped
```

[caddy]: https://caddyserver.com/
[cloudflare-dns]: https://github.com/caddy-dns/cloudflare
[Dockerfile]: https://github.com/0x-jerry/docker-caddy-cloudflaredns/blob/main/dockerfile
