FROM dreamcat4/tvh.build.pbuilder
MAINTAINER dreamcat4 <dreamcat4@gmail.com>


ENV _clean="rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*"
ENV _apt_clean="eval apt-get clean && $_clean"


# Install distribution tarball for target architecture
RUN pbuilder-dist sid armhf create


