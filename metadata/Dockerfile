FROM debian:bookworm-slim

WORKDIR /data

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        exiv2 \
        libimage-exiftool-perl \
        poppler-utils \
        mediainfo \
        binutils \
        file && \
    rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]
