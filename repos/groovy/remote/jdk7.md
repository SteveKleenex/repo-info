## `groovy:jdk7`

```console
$ docker pull groovy@sha256:06d70f1c144bbe5edce98d60b198ed0ae11aeeebfa7ad23c7b137ba0164916a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `groovy:jdk7` - linux; amd64

```console
$ docker pull groovy@sha256:62d7be02709d7a76fec355830492f9e125fd13c90b99d17422f8e295eb6923e3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.7 MB (282741132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35be68ab812f1c1d757482ed9cd911b081061c26c7c9497fff615ebbece71853`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Mar 2018 23:40:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 11:17:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 11:17:16 GMT
ENV LANG=C.UTF-8
# Wed, 14 Mar 2018 11:17:17 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 14 Mar 2018 11:17:18 GMT
RUN ln -svT "/usr/lib/jvm/java-7-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 14 Mar 2018 11:17:18 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 10 Apr 2018 04:02:02 GMT
ENV JAVA_VERSION=7u171
# Tue, 10 Apr 2018 04:02:02 GMT
ENV JAVA_DEBIAN_VERSION=7u171-2.6.13-1~deb8u1
# Tue, 10 Apr 2018 04:03:17 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-7-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 10 Apr 2018 06:35:45 GMT
CMD ["groovysh"]
# Tue, 10 Apr 2018 06:35:46 GMT
ENV GROOVY_HOME=/opt/groovy
# Tue, 10 Apr 2018 06:35:46 GMT
ENV GROOVY_VERSION=2.4.15
# Tue, 10 Apr 2018 06:35:52 GMT
RUN set -o errexit -o nounset 	&& echo "Downloading Groovy" 	&& wget --no-verbose --output-document=groovy.zip "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip" 		&& echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server" 	&& export GNUPGHOME="$(mktemp -d)" 	&& for key in 		"7FAA0F2206DE228F0DB01AD741321490758AAD6F" 		"331224E1D7BE883D16E8A685825C06C827AF6B66" 		"34441E504A937F43EB0DAEF96A65176A0FB1CD0B" 		"9A810E3B766E089FFB27C70F11B595CEDC4AEBB5" 		"81CABC23EECA0790E8989B361FF96E10F0E13706" 	; do 		for server in 			"ha.pool.sks-keyservers.net" 			"hkp://p80.pool.sks-keyservers.net:80" 			"pgp.mit.edu" 		; do 			echo "  Trying ${server}"; 			if gpg --keyserver "${server}" --recv-keys "${key}"; then 				break; 			fi; 		done; 	done; 	if [ $(gpg --list-keys | grep -c "pub ") -ne 5 ]; then 		echo "ERROR: Failed to fetch GPG keys" >&2; 		exit 1; 	fi 		&& echo "Checking download signature" 	&& wget --no-verbose --output-document=groovy.zip.asc "https://dist.apache.org/repos/dist/release/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc" 	&& gpg --batch --verify groovy.zip.asc groovy.zip 	&& rm --recursive --force "${GNUPGHOME}" 	&& rm groovy.zip.asc 		&& echo "Installing Groovy" 	&& unzip groovy.zip 	&& rm groovy.zip 	&& mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/" 	&& ln --symbolic "${GROOVY_HOME}/bin/grape" /usr/bin/grape 	&& ln --symbolic "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy 	&& ln --symbolic "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc 	&& ln --symbolic "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole 	&& ln --symbolic "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc 	&& ln --symbolic "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh 	&& ln --symbolic "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy 		&& echo "Adding groovy user and group" 	&& groupadd --system --gid 1000 groovy 	&& useradd --system --gid groovy --uid 1000 --shell /bin/bash --create-home groovy 	&& mkdir --parents /home/groovy/.groovy/grapes 	&& chown --recursive groovy:groovy /home/groovy 		&& echo "Symlinking root .groovy to groovy .groovy" 	&& ln -s /home/groovy/.groovy /root/.groovy
# Tue, 10 Apr 2018 06:35:53 GMT
USER [groovy]
# Tue, 10 Apr 2018 06:35:53 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Tue, 10 Apr 2018 06:35:53 GMT
WORKDIR /home/groovy
# Tue, 10 Apr 2018 06:35:57 GMT
RUN set -o errexit -o nounset 	&& echo "Testing Groovy installation" 	&& groovy --version
```

-	Layers:
	-	`sha256:f2b6b4884fc8b2f1fcef843f92f7c82c9c149df85ac77e5f0de7a342ae442412`  
		Last Modified: Tue, 13 Mar 2018 22:43:41 GMT  
		Size: 52.6 MB (52608519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb899b4df216ab398fb05547f86dc371db944cf53dea7913d2f4261ed09e2be`  
		Last Modified: Wed, 14 Mar 2018 00:34:40 GMT  
		Size: 19.3 MB (19266189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74eaa8be7221e87fae8804464be5f691955f582b6b4efe703095a2c9b041696a`  
		Last Modified: Wed, 14 Mar 2018 00:37:48 GMT  
		Size: 43.3 MB (43254408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be20ca4c60d4b1bdeaa16f01e7c057d17a2abf947b5d18d8ba314643738bcd`  
		Last Modified: Wed, 14 Mar 2018 13:19:50 GMT  
		Size: 828.7 KB (828714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8a0c25768cd457b272cfde167ce6dda903e7fc4d8f02ed87d65409f7a716d5`  
		Last Modified: Wed, 14 Mar 2018 13:19:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8449367f126ca8237a10277d1ed86840137f134b28044248a06ec39a6f54511`  
		Last Modified: Wed, 14 Mar 2018 13:19:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81af614b694437fff357bafc11b7d5d2625ab536cea7283af5d0ab5308299c48`  
		Last Modified: Tue, 10 Apr 2018 04:35:34 GMT  
		Size: 129.6 MB (129639024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567c529e8a00a360fe2b3f6f00dd96c8e925e5395e78573b06f0d5ad5463904f`  
		Last Modified: Tue, 10 Apr 2018 06:53:25 GMT  
		Size: 37.1 MB (37143760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60389b5459e8ef0a9bf3cf9121bfda3bc448ee43a143840a3413d79822ca8422`  
		Last Modified: Tue, 10 Apr 2018 06:53:22 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
