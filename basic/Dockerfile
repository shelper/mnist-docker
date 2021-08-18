FROM tensorflow/tensorflow:latest-gpu-py3

MAINTAINER Zhijia Yuan (mpnv38@zebra.com)
ENV DEBIAN_FRONTEND=nonintercative


RUN apt-get update && \
    apt-get install -y \
        python3-tk && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN pip install --upgrade \
        pip \
        keras
RUN pip install pillow

COPY mnist-learning /repositories/mnist-learning

WORKDIR /repositories/mnist-learning
ENTRYPOINT ["python3"]
CMD [ "train.py" ]
