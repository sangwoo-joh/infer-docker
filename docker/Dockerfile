FROM debian:stretch-slim

LABEL maintainer "Sangwoo Joh <lambdasnow@gmail.com>"

RUN apt-get update && \
  mkdir -p /usr/share/man/man1 && \
  apt-get install --yes --no-install-recommends \
    autoconf automake cmake curl libc6-dev libsqlite3-dev pkg-config zlib1g-dev \
    python2.7 libgmp-dev libc6-i386 lib32z1 lib32stdc++6 rsync libmpfr-dev \
    openjdk-8-jdk-headless tzdata bubblewrap patchelf && \
    patch unzip make gcc g++ xz-utils && \
  rm -rf /var/lib/apt/lists/*

RUN ln -s /usr/bin/python2.7 /usr/local/bin/python

# install opam
RUN curl -sL https://github.com/ocaml/opam/releases/download/2.0.5/opam-2.0.5-x86_64-linux > /usr/bin/opam && chmod +x /usr/bin/opam

RUN opam init --reinit --bare --disable-sandboxing --yes --auto-setup
