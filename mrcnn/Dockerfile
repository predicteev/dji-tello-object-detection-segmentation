FROM ubuntu:18.04

RUN DEBIAN_FRONTEND=noninteractive apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y python3-opencv nano sudo python3 python3-pip git

RUN pip3 install numpy==1.14.5 scipy==1.1.0 cython==0.28.3 \ 
&& h5py==2.8.0 \
&& Pillow==8.3.2 \
&& keras==2.2.5 \
&& jupyter==1.0.0 \
&& matplotlib==2.2.2 \
&& imgaug==0.2.6 \
&& tensorflow==1.9.0 \
&& imutils==0.5.4 \
&& python3 -m pip install -U pip && python3 -m pip install -U scikit-image \
&& pip3 install pycocotools

COPY "./saving.py" "/usr/local/lib/python3.6/dist-packages/keras/engine/saving.py"
WORKDIR /app_data
RUN git clone "https://github.com/predicteev/dji-tello-object-detection-segmentation.git"
ENTRYPOINT "/bin/bash"

