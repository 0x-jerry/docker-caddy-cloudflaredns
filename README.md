# Build Docker Image

Custom [caddy] image with [cloudflare-dns]. Detail in [Dockerfile].

## Prepare

1. You need to create a `secret` named `DOCKERHUB_TOKEN`
2. You need to create a `variable` named `DOCKERHUB_USERNAME`

[caddy]: https://caddyserver.com/
[cloudflare-dns]: https://github.com/caddy-dns/cloudflare
[Dockerfile]: https://github.com/0x-jerry/docker-caddy-cloudflaredns/blob/main/dockerfile