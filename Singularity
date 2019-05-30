Bootstrap: docker
From: tensorflow/tensorflow:1.13.1-gpu-py3

%post
    apt-get update && apt-get install -y --no-install-recommends \
        curl \
        unzip \
        git \
        openssl \
        ca-certificates \
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
