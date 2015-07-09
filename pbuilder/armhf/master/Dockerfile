FROM dreamcat4/tvh.build.pbuilder.armhf
MAINTAINER dreamcat4 <dreamcat4@gmail.com>


# Version to build
ENV tvh_branch="master"


# Update & checkout tvheadend
WORKDIR /build/tvheadend
RUN git pull && git checkout "$tvh_branch"


# (replace this:) # Compile tvheadend .deb pkgs - with ./Autogen.sh
# RUN AUTOBUILD_CONFIGURE_EXTRA="--enable-libffmpeg_static --enable-hdhomerun_static --enable-dvbcsa --enable-bundle" ./Autobuild.sh -w /build/work -t trusty-amd64 \
#  && mv /build/*.deb /out && mv /build/*.changes /out && rm -rf /build

# (with this:) # Compile tvheadend .deb pkgs - with pbuilder chroot environment
RUN TVH_BUILD="sid:armhf" ./support/pbuilder \
 && mv /build/*.deb /out && mv /build/*.changes /out && rm -rf /build


# (disabled for now) # Upload tvheadend ubuntu .deb pkgs --> bintray.com
# WORKDIR /out
# ADD upload-to-bintray /bin/
# RUN chmod +x /bin/upload-to-bintray


# (disabled for now) # Execute our upload script
# ADD bintray-env /out/
# RUN upload-to-bintray && rm /out/bintray-env


# Build products are copied to the volume '/out'
VOLUME /out





