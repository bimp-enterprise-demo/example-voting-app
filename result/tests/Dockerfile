FROM docker.io/library/node:8.17.0-slim@sha256:6f47d69e8deac79b425d3f5d49ee0f804dbfb07bfc0f8ee8688c1bff0fb50448

RUN apt-get update -qq && apt-get install -qy \ 
    ca-certificates \
    bzip2 \
    curl \
    libfontconfig \
    --no-install-recommends
RUN yarn global add phantomjs-prebuilt
ADD . /app
WORKDIR /app
CMD ["/app/tests.sh"]
