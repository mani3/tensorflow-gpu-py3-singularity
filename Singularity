Bootstrap: docker
From: tensorflow/tensorflow:1.13.1-gpu-py3

%post
    apt-get update && apt-get install -y --no-install-recommends \
        build-essential \
        zlib1g-dev \
        libssl-dev \
        libbz2-dev \
        libreadline-dev \
        libfreetype6-dev \
        libhdf5-serial-dev \
        libpng12-dev \
        libzmq3-dev \
        pkg-config \
        software-properties-common \
        curl \
        unzip \
        git \
        openssl \
        ca-certificates \
        python3 \
        python3-pip \
        python3-setuptools \
        python3-dev \
        && \
    apt-get clean && rm -rf /var/lib/apt/lists/*
    
    pip3 install -U setuptools
    pip3 --no-cache-dir install \
        wheel \
        Pillow \
        opencv-contrib-python==3.2.0.8 \
        h5py \
        keras_applications \
        keras_preprocessing \
        matplotlib \
        numpy \
        pandas \
        scipy \
        sklearn \
        tqdm \
        argparse \
        boto3 \
        mtcnn 

%environment
    export LC_ALL=C.UTF-8
    export LANG=C.UTF-8
    export SSL_CERT_FILE="/etc/ssl/certs/ca-certificates.crt"
