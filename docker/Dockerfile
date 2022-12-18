FROM phoenixrtos/build

RUN apt-get update && \
    apt-get install -y python3-pip lsb-release wget software-properties-common gnupg

WORKDIR /

RUN wget https://apt.llvm.org/llvm.sh && \
    chmod +x llvm.sh && \
    ./llvm.sh 14

#RUN git clone -b dev https://github.com/szsam/whole-program-llvm.git
COPY whole-program-llvm/ whole-program-llvm/
RUN pip install whole-program-llvm/
