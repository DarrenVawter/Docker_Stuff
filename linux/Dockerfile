FROM ubuntu:16.04
 
RUN useradd -ms /bin/bash unity
 
WORKDIR /home/unity
 
COPY Server.tar.gz .
 
RUN chown unity:unity Server.tar.gz
 
USER unity
 
RUN tar --no-same-owner -xf Server.tar.gz && rm Server.tar.gz
 
ENTRYPOINT ["./Server.x86_64", "-logFile", "/dev/stdout"]