FROM tharvik/gentoo-portage

RUN rm /etc/portage/env/test
RUN echo "FEATURES=\"${FEATURES} noman noinfo nodoc\"" >> /etc/portage/make.conf
RUN emerge-accept gcc:7.2.0
RUN gcc-config x86_64-pc-linux-gnu-7.2.0
RUN . /etc/profile
RUN emerge -1 libtool
RUN echo '*/* -bindist' > /etc/portage/package.use/no-bindist
RUN emerge-accept -DN @world
RUN emerge-accept dev-vcs/git layman
RUN sed -i 's/^check_official.*/check_official : no/' /etc/layman/layman.cfg
RUN layman -L
