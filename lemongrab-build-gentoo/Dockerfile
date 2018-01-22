FROM loonygnoll/gentoo-gcc7

RUN layman -a earshark
RUN emerge-accept gtest ruby lcov
RUN gem install coveralls-lcov
RUN emerge-accept --onlydeps lemongrab
RUN rm -rf /usr/portage

ENTRYPOINT ["/root/build-in-docker.sh"]
