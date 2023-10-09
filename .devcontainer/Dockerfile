FROM ubuntu:latest

# Install basic tools
RUN apt-get update && apt-get install -y curl git unzip xz-utils zip libglu1-mesa openjdk-11-jdk wget

# Setup Flutter
RUN git clone https://github.com/flutter/flutter.git /usr/local/flutter
ENV PATH "$PATH:/usr/local/flutter/bin"
RUN flutter channel stable
RUN flutter upgrade
RUN flutter config --enable-web
RUN flutter doctor
