FROM --platform=$TARGETPLATFORM caddy:builder-alpine AS builder

RUN xcaddy build \
    --with github.com/caddy-dns/cloudflare

FROM --platform=$TARGETPLATFORM caddy:alpine

COPY --from=builder /usr/bin/caddy /usr/bin/caddy
