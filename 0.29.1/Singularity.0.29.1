# =====================================
# HEADER
# =====================================
Bootstrap: docker
From: openjdk:8-jre-alpine3.7

%labels
  MAINTAINER fabrice.bonte@chru-lille.fr
  CONTAINER_VERSION 0.0.1
  SINGULARITY_VERSION 2.5.1
  NEXTFLOW_VERSION 0.29.1

%setup

%files

%environment
  HOME=/opt/nextflow

%help

%post
  # =====================================
  # INSTALL DEPENDENCIES
  # =====================================
  apk update && apk upgrade 
  apk add --no-cache coreutils 
  apk add --no-cache curl bash 
  apk add --no-cache wget 
  apk add --no-cache build-base 
  apk add --no-cache python
  apk add --no-cache --upgrade tar
  apk add --no-cache linux-headers
  apk add --no-cache sudo

  # =====================================
  # INSTALL NEXTFLOW
  # =====================================

  NEXTFLOW_VERSION=0.29.1
  HOME=/opt/nextflow
  mkdir -p /opt/nextflow 
  cd /opt/nextflow 
  curl -fsSL https://github.com/nextflow-io/nextflow/releases/download/v$NEXTFLOW_VERSION/nextflow | bash 
  ln -s /opt/nextflow/nextflow /usr/bin/nextflow
  nextflow -h
  chmod -R 777 /opt/nextflow/.


  # =====================================
  # INSTALL SINGULARITY
  # =====================================

  mkdir -p /opt/singularity && cd /opt/singularity
  
  SINGULARITY_VERSION=2.5.1
  wget https://github.com/singularityware/singularity/releases/download/$SINGULARITY_VERSION/singularity-$SINGULARITY_VERSION.tar.gz
  tar xvf singularity-$SINGULARITY_VERSION.tar.gz
  cd singularity-$SINGULARITY_VERSION
  ./configure --prefix=/usr/local
  make
  sudo make install