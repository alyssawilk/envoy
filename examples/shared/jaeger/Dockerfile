FROM jaegertracing/all-in-one@sha256:8927623d141919cf0c75d095a43952a20e4689036b9d2dc92c25a1b1780b0539
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
