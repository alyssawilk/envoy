FROM jaegertracing/all-in-one@sha256:49da568e22d597e05a4264cd21ed760292552fcf1d6735a14363e6becc3afefc
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
