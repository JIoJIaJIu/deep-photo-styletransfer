FROM kaixhin/cuda-torch:latest

RUN apt-get update
RUN apt-get install -y libprotobuf-dev protobuf-compiler wget python3-pip
RUN luarocks install csvigo && luarocks install loadcaffe

RUN git clone https://github.com/jiojiajiu/deep-photo-styletransfer.git  /opt/deep_photo

WORKDIR /opt/deep_photo

RUN bash models/download_models.sh
RUN pip3 install numpy scipy
RUN make clean all
