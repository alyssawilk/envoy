FROM python:3.11.1-slim@sha256:79095e304e31196bad049e74f666508ac81909d201ec9371f9f3cd68fa365cf6

WORKDIR /client

COPY requirements.txt /client/requirements.txt

# Cache the dependencies
RUN pip install --require-hashes -qr /client/requirements.txt

# Copy the sources, including the stubs
COPY client.py /client/grpc-kv-client.py
COPY kv /client/kv

RUN chmod a+x /client/grpc-kv-client.py

# http://bigdatums.net/2017/11/07/how-to-keep-docker-containers-running/
# Call docker exec /client/grpc.py set | get
CMD tail -f /dev/null
