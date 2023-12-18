FROM jaegertracing/all-in-one@sha256:8aef1ce96cb863f151dda186a3c9ceea88e6c712cf3273f7b4f32b5b9b0d5680
HEALTHCHECK \
    --interval=1s \
    --timeout=1s \
    --start-period=1s \
    --retries=60 \
    CMD wget -q --header='Content-Type:application/json' -O - http://localhost:14269/health | grep "Server available"
