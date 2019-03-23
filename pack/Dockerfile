FROM alpine:latest
RUN wget https://github.com/buildpack/pack/releases/download/v0.0.9/pack-0.0.9-linux.tar.gz
RUN tar -xvf pack-0.0.9-linux.tar.gz 
RUN mv pack /usr/local/bin
ENTRYPOINT ["/usr/local/bin/pack"]
