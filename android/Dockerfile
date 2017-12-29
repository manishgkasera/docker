FROM ubuntu:14.04

RUN apt-get -y update
RUN apt-get -y upgrade

ENV USER=Kalki


RUN apt-get -y --force-yes install bc git-core gnupg flex bison gperf build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z-dev ccache libgl1-mesa-dev libxml2-utils xsltproc unzip python-networkx schedtool

RUN mkdir ~/bin
RUN curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo && chmod a+x ~/bin/repo
ENV PATH=~/bin:$PATH

ENV USE_CCACHE=1
ENV CCACHE_DIR=/android/.ccache/


CMD [". /android/build/envsetup.sh"]

