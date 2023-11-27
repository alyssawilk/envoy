FROM jaegertracing/all-in-one@sha256:80acdbc881aa958a1bb50de1d53823b01bd89167c6166baedfded675a690843c
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
