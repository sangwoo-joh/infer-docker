FROM ubuntu:16.04

LABEL maintainer "Sangwoo Joh <lambdasnow@gmail.com>"

RUN sudo apt-get update && \
  sudo apt-get install --yes --no-install-recommends \
    autoconf automake cmake curl libc6-dev libsqlite3-dev pkg-config zlib1g-dev \
    python libgmp-dev libc6-i386 lib32z1 lib32stdc++6 rsync libmpfr-dev \
    openjdk-8-jdk-headless tzdata bubblewrap patchelf && \
  rm -rf /var/lib/apt/lists/*

# install opam
RUN curl -sL https://github.com/ocaml/opam/releases/download/2.0.5/opam-2.0.5-x86_64-linux > /usr/bin/opam && chmod +x /usr/bin/opam

RUN opam init --reinit --bare --disable-sandboxing --yes --auto-setup
