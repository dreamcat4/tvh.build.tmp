FROM ubuntu-debootstrap:14.04
MAINTAINER dreamcat4 <dreamcat4@gmail.com>


ENV _clean="rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*"
ENV _apt_clean="eval apt-get clean && $_clean"


# Install pbuilder base dependancy
RUN apt-get update -qq && apt-get install -qqy \
			git qemu-user-static pbuilder && $_apt_clean


# Download tvheadend
RUN mkdir /build /out \
 && git clone https://github.com/tvheadend/tvheadend.git /build/tvheadend

