# Debian como imagen base
FROM debian:bookworm-slim

# Evita preguntas durante la instalación
ENV DEBIAN_FRONTEND=noninteractive

# Directorio de trabajo
WORKDIR /opt

# Dependencias necesarias
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        python3 \
        python3-pip \
        python3-venv \
        git \
        ca-certificates && \
    rm -rf /var/lib/apt/lists/*

# Actualizar pip
RUN python3 -m pip install --no-cache-dir --break-system-packages --upgrade pip

# ----------------------------
# Holehe
# ----------------------------
RUN python3 -m pip install --no-cache-dir --break-system-packages holehe

# ----------------------------
# Sherlock
# ----------------------------
RUN git clone https://github.com/sherlock-project/sherlock.git /opt/sherlock && \
    python3 -m pip install --no-cache-dir --break-system-packages /opt/sherlock

# ----------------------------
# GhostTrack
# ----------------------------
RUN git clone https://github.com/HunxByts/GhostTrack.git /opt/ghosttrack && \
    cd /opt/ghosttrack && \
    python3 -m pip install --no-cache-dir --break-system-packages -r requirements.txt

# ----------------------------

CMD ["/bin/bash"]
