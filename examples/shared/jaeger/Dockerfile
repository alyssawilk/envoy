FROM jaegertracing/all-in-one@sha256:f6b5d09073f14f76873d300f565a6691d815e81bea8e07e1dc3ff67e0596dd4e
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
