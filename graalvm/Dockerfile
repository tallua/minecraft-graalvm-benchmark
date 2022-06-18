FROM atm6:latest

RUN wget https://github.com/graalvm/graalvm-ce-builds/releases/download/vm-22.1.0/graalvm-ce-java11-linux-amd64-22.1.0.tar.gz && \
    mkdir graalvm && \
    tar -xzf graalvm-ce-java11-linux-amd64-22.1.0.tar.gz -C graalvm

ENV JAVA_HOME=/graalvm/graalvm-ce-java11-22.1.0
ENV PATH=/graalvm/graalvm-ce-java11-22.1.0/bin:$PATH

WORKDIR /atm6
CMD "./startserver.sh"