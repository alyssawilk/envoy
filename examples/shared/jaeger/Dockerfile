FROM jaegertracing/all-in-one@sha256:826bb040b1b0f9f3251d892ed3d726cadf8d221a55dd5a561188ad9a337edfd1
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
