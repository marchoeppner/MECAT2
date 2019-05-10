Bootstrap:docker
From:ubuntu:19.04

%labels
    MAINTAINER Marc Hoeppner <m.hoeppner@ikmb.uni-kiel.de>
    DESCRIPTION Singularity image containing Mecat2
    VERSION 0.1

%environment
    PATH=/opt/mecat2/Linux-amd64/bin:$PATH
    export PATH
    LC_ALL=en_US.UTF-8
    export LC_ALL
    LANG=en_US.UTF-8
    export LANG

%files

%post

apt-get -y update
apt-get -y install wget build-essential perl coreutils locales

locale-gen en_US.UTF-8
update-locale LANG=en_US.UTF-8

cd /opt

wget https://github.com/xiaochuanle/MECAT2/releases/download/20192026/mecat2_20190226_linuax_amd64.tar.gz
tar -xvf mecat2_20190226_linuax_amd64.tar.gz
rm mecat2_20190226_linuax_amd64.tar.gz
mv MECAT2 mecat2
