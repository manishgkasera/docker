FROM ubuntu:14.04

RUN apt-get -y update
RUN apt-get -y upgrade

RUN apt-get -y --force-yes install git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache libgl1-mesa-dev libxml2-utils xsltproc unzip python-networkx

RUN mkdir ~/bin
RUN curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo && chmod a+x ~/bin/repo
ENV PATH=~/bin:$PATH

RUN echo "USE_CCACHE=1" >> ~/.bashrc && echo "CCACHE_DIR=/android/.ccache" >> ~/.bashrc && echo "/android/prebuilts/misc/linux-x86/ccache/ccache -M 50G" >> ~/.bashrc


CMD [". /android/build/envsetup.sh"]

