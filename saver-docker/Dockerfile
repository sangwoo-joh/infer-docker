FROM ocaml/opam:ubuntu

LABEL maintainer "Sangwoo Joh <lambdasnosw@gmail.com>"

RUN opam repo add http https://opam.ocaml.org/1.2.2 && \
  opam update && \
  sudo apt-get update && \
  sudo apt-get install --yes --no-install-recommends \
    autoconf automake cmake curl libc6-dev libsqlite3-dev pkg-config zlib1g-dev \
    python libgmp-dev libc6-i386 lib32z1 lib32stdc++6 rsync libmpfr-dev \
    openjdk-8-jdk-headless tzdata && \
  opam switch -j 28 set infer-4.06.1+flambda --alias-of 4.06.1+flambda

# Before you build, you should install ocamlgraph via opam and build &
# install dependencies
