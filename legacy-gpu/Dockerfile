FROM tensorflow/tensorflow:latest-gpu

RUN pip install --upgrade pip
RUN pip install \
        theano \
        Cython \
        numpy \
        matplotlib \
        seaborn \
        scipy \
        scikit-learn \
        pandas \
        pyyaml \
        imutils \
        opencv-python \
        torch \
        tqdm \
        psutil \
        h5py \
        jupyter

WORKDIR /app/codalab

# To add
# apt-get update
# apt-get -y install libgl1-mesa-glx
# apt-get -y install libglb2.0-0
