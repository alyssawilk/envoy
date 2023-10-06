FROM jaegertracing/all-in-one@sha256:75754af11f16ac9d77abf1afcb0e65ea7b6c49620d2372bb63fdb6215b155671
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
