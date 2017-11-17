FROM tharvik/gentoo-portage

RUN rm /etc/portage/env/test
RUN echo "FEATURES=\"${FEATURES} noman noinfo nodoc\"" >> /etc/portage/make.conf
RUN emerge-accept gcc:7.2.0
RUN gcc-config x86_64-pc-linux-gnu-7.2.0
RUN . /etc/profile
RUN emerge -1 libtool
RUN emerge -1 git layman
