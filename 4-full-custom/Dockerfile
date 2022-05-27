FROM ubuntu:22.04
WORKDIR /app
COPY . .
RUN apt update -y
RUN apt install nodejs -y
RUN nodejs --version
RUN apt clean
ENTRYPOINT [ "nodejs", "index.js" ]