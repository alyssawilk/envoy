FROM jaegertracing/all-in-one@sha256:637f22e966954461b3131ee4c52053f518a39432868ad225bb6261757fb56e2d
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
