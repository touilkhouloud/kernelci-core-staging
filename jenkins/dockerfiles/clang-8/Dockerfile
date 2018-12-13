FROM kernelci/build-base

RUN apt-get update && apt-get install --no-install-recommends -y \
    software-properties-common \
    gnupg2
RUN wget -q -O - https://apt.llvm.org/llvm-snapshot.gpg.key| apt-key add -
RUN apt-add-repository 'deb http://apt.llvm.org/unstable/ llvm-toolchain main'
RUN apt-get update && apt-get install --no-install-recommends -y \
    clang-8 clang

# clang kernel builds still use arch-specific GNU as/ld
RUN apt-get -y install binutils-aarch64-linux-gnu
