FROM ldh0227/base-ubuntu-20.04

RUN export VERSION="10.24.1" SHA256="b11ce837867e50d1b2bf09da6a85336bedfa257bf92f34712aeb94360c0bcd6e" && \
	curl -Lo /tmp/nodejs.tar.xz "https://nodejs.org/download/release/v$VERSION/node-v$VERSION-linux-arm64.tar.xz" && \
	sha256sum /tmp/nodejs.tar.xz && \
	echo "$SHA256 /tmp/nodejs.tar.xz" | sha256sum --check --status && \
	mkdir -p /opt/node && \
	tar --strip-components 1 -C /opt/node -xf /tmp/nodejs.tar.xz && \
	rm -f /tmp/nodejs.tar.xz

ENV PATH=/opt/node/bin:$PATH
