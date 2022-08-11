FROM tensorflow/tensorflow:latest-gpu

RUN apt-get update && apt-get install -y \
        wget \
        && rm -rf /var/lib/apt/lists/*

RUN cd /opt \
        && wget https://packages.gurobi.com/9.5/gurobi9.5.2_linux64.tar.gz \
        && tar zxvf gurobi9.5.2_linux64.tar.gz \
        && rm gurobi9.5.2_linux64.tar.gz

ENV PATH="${PATH}":/opt/gurobi952/linux64/bin
ENV GUROBI_HOME=/opt/gurobi952/linux64

RUN pip install --upgrade pip
RUN pip install \
        theano==1.0.5 \
        Cython==0.29.30 \
        numpy==1.22.2 \
        matplotlib==3.5.1 \
        seaborn==0.11.2 \
        scipy==1.8.1 \
        scikit-learn==1.1.1 \
        pandas==1.4.3 \
        pyyaml==6.0 \
        imutils==0.5.4 \
        opencv-python==4.6.0.66 \
        torch==1.12.0 \
        tqdm==4.64.0 \
        psutil==5.9.1 \
        h5py==3.6.0 \
        jupyter==1.0.0 \
	gym==0.25.1 \ 
        gurobipy==9.5.2

ENV PYG_VERSION=1.12.0+cu102
RUN pip install torch-scatter -f https://data.pyg.org/whl/torch-${PYG_VERSION}.html \
        && pip install torch-sparse -f https://data.pyg.org/whl/torch-${PYG_VERSION}.html \
        && pip install torch-geometric \
        && pip install torch-cluster -f https://data.pyg.org/whl/torch-${PYG_VERSION}.html \ 
        && pip install torch-spline-conv -f https://data.pyg.org/whl/torch-${PYG_VERSION}.html

WORKDIR /app/codalab

# To add
# apt-get update
# apt-get -y install libgl1-mesa-glx
# apt-get -y install libglb2.0-0
