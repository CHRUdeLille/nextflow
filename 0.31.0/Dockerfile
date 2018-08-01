FROM nextflow/nextflow:0.31.0

ENV SINGULARITY_VERSION=2.5.1

RUN apk update \
    && apk add --update --no-cache \
        curl file build-base autoconf automake libtool linux-headers \
        tar gzip bash python squashfs-tools libarchive-dev \
    && cd /tmp \
    && curl -fSsL https://github.com/singularityware/singularity/releases/download/${SINGULARITY_VERSION}/singularity-${SINGULARITY_VERSION}.tar.gz | tar -zxvpf - \
    && cd singularity-${SINGULARITY_VERSION} \
    && ./configure --prefix=/opt/singularity --sysconfdir=/opt/singularity/etc --localstatedir=/var/lib \
    && make -j4 \
    && make install \
    && cd .. \
    && rm -rf singularity-${SINGULARITY_VERSION} \
    && ldconfig /opt/singularity/lib/singularity \
    && ln -s /opt/singularity/bin/singularity /usr/bin/singularity \
    && apk del --purge \
        curl file build-base autoconf automake libtool linux-headers