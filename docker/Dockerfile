FROM ocaml/opam2:ubuntu

LABEL maintainer "Sangwoo Joh <lambdasnow@gmail.com>"

RUN sudo apt-get update && \
  sudo apt-get install --yes --no-install-recommends \
    autoconf automake cmake curl libc6-dev libsqlite3-dev pkg-config zlib1g-dev \
    python libgmp-dev libc6-i386 lib32z1 lib32stdc++6 rsync libmpfr-dev \
    openjdk-8-jdk-headless
