FROM ubuntu:23.10

RUN apt-get update && \
  apt-get -y upgrade && \
  apt-get -y install cmake gcc-arm-none-eabi \
  libnewlib-arm-none-eabi libstdc++-arm-none-eabi-newlib git \
  python3

RUN mkdir sdk
WORKDIR sdk
RUN git clone https://github.com/raspberrypi/pico-sdk
ENV PICO_SDK_PATH=/sdk/pico-sdk
WORKDIR pico-sdk
RUN git submodule update --init

WORKDIR /
RUN git clone https://github.com/raspberrypi/pico-examples
WORKDIR pico-examples

CMD ["sleep 300000"]
