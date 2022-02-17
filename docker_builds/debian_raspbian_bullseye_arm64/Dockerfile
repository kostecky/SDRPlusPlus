FROM myoung34/github-runner:debian-bullseye

RUN sudo apt-get update \
  && sudo apt-get install -y --no-install-recommends \
    python3-dev \
    python3-pip \
    python3-coverage \
    python \
    python-dev \
    cmake \
    build-essential \
    p7zip-full \
    wget \
    libzstd-dev \
    libfftw3-3 \
    libfftw3-dev \
    libglfw3-dev \
    libvolk2-dev \
    libglfw3 \
    libvolk2.4 \
    libairspy0 \
    libairspyhf1 \
    libsoapysdr0.7 \
    libiio0 \
    libad9361-0 \
    libairspy-dev \
    libairspyhf-dev \
    libsoapysdr-dev \
    libiio-dev \
    libad9361-dev \
    libbladerf2 \
    libbladerf-dev \
    libhackrf0 \
    libhackrf-dev \
    librtlsdr0 \
    librtlsdr-dev \
    portaudio19-dev \
    librtaudio-dev \
    libcodec2-0.9 \
    libcodec2-dev \
    liblimesuite20.10-1 \
    liblimesuite-dev \
    libgl1-mesa-dev \
  && rm -rf /tmp/*

# Need this to install SDRPlay API
RUN mkdir -p /etc/udev/rules.d

# Install SDRPlay libraries
RUN wget https://www.sdrplay.com/software/SDRplay_RSP_API-ARM64-3.07.1.run \
    && 7z x ./SDRplay_RSP_API-ARM64-3.07.1.run \
    && 7z x ./SDRplay_RSP_API-ARM64-3.07.1 \
    && cp aarch64/libsdrplay_api.so.3.07 /usr/lib/libsdrplay_api.so \
    && cp inc/* /usr/include/
