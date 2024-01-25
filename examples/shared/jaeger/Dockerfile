FROM jaegertracing/all-in-one@sha256:3b8ca835a4271f03b2488337955e09dc1b38ba261fda91933e6db03e01cb3e5b
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
