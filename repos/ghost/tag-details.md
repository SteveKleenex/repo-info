<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ghost`

-	[`ghost:0`](#ghost0)
-	[`ghost:0.11`](#ghost011)
-	[`ghost:0.11.12`](#ghost01112)
-	[`ghost:0.11.12-alpine`](#ghost01112-alpine)
-	[`ghost:0.11-alpine`](#ghost011-alpine)
-	[`ghost:0-alpine`](#ghost0-alpine)
-	[`ghost:1`](#ghost1)
-	[`ghost:1.22`](#ghost122)
-	[`ghost:1.22.4`](#ghost1224)
-	[`ghost:1.22.4-alpine`](#ghost1224-alpine)
-	[`ghost:1.22-alpine`](#ghost122-alpine)
-	[`ghost:1-alpine`](#ghost1-alpine)
-	[`ghost:alpine`](#ghostalpine)
-	[`ghost:latest`](#ghostlatest)

## `ghost:0`

```console
$ docker pull ghost@sha256:bacb8330293d2cb71eda62af696cce318164c5a93285183fb9f2b60fe9e0fb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:0` - linux; amd64

```console
$ docker pull ghost@sha256:b92f1bc2512a5e1bbb6901aa732e24cc96c93fabc6442e7de7c9e6ccf05170dc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113786323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8ca5cdf069950b6f388c0f4f3cc6f2fefed7d3a9702bdb10b346c13141379f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:03:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:03:53 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 01:31:24 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:31:50 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 01:31:51 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:31:55 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 01:31:55 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:51:09 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Tue, 03 Apr 2018 03:51:09 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 03:51:15 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 03:51:15 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 03:51:15 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 03:51:15 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 03:52:32 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 03:52:33 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 03:52:34 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 03:52:34 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 03:52:34 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Tue, 03 Apr 2018 03:52:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Apr 2018 03:52:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 03:52:36 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 03:52:36 GMT
CMD ["npm" "start"]
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
	-	`sha256:c669d5da499dfc3f959bff647d84aa109d42bd9dc4a84cd1736607a9a193931e`  
		Last Modified: Thu, 15 Mar 2018 05:16:20 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8ff4c87216eb5e2bdc5aeab7d50e312312df3b9358eac4f84cd10c0db8d7c`  
		Last Modified: Thu, 15 Mar 2018 05:16:18 GMT  
		Size: 117.6 KB (117624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d93f330ca2fc79c95fa142b121be257ae64491015b8997cd012096fbd113fb`  
		Last Modified: Tue, 03 Apr 2018 02:26:55 GMT  
		Size: 14.7 MB (14743833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5858a3ea9339b3a6db832ae2fbb00a02d8b6475f2af80f473668cd6e3f468e`  
		Last Modified: Tue, 03 Apr 2018 02:26:50 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c1052636ab321eee45cc1619becae1525ac9392854707536e6c03fd7280fb3`  
		Last Modified: Tue, 03 Apr 2018 04:29:27 GMT  
		Size: 4.5 KB (4463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8925eb724b45a3ccb2460c08b1047a3306b9dbec9ea185971e2d7c6bd51f3d`  
		Last Modified: Tue, 03 Apr 2018 04:29:28 GMT  
		Size: 500.7 KB (500671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c31ef7135d57fa0312b48beac94e99e9d44a3f5eb5805bc45c6d47d4e50613`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b8c39ec852f876618629bb0b256034ac40c79ef24030cc2fda1ff1a825cf5a`  
		Last Modified: Tue, 03 Apr 2018 04:29:43 GMT  
		Size: 25.5 MB (25478478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3276306d6c16c4cc43f841cd645202c5ab36078d6355619c80ef57ef22184b33`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e4eadce21ee792c3f70a75ffb7be3a8095364aaff12c78faecdddad41151a9`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadb91902da8a85e2b892633445c7e54bdfaee61858b2562452d914f414e8bd8`  
		Last Modified: Tue, 03 Apr 2018 04:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; arm variant v7

```console
$ docker pull ghost@sha256:8f5618b2a3def4ba2b777bed71b4f6bdfa57d96b9591fa81d40769b804096325
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114292463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0bf8068e56597b32dff6a34f2f52cdbf822c6f47d12af9038f1814589bdf97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:05 GMT
ADD file:aeb57f3a84dc1b93e1d38a80409a407df553344149d5070ed79b656865c90c54 in / 
# Tue, 12 Dec 2017 13:27:06 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:14:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 16:51:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 12 Dec 2017 16:51:03 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 04 Jan 2018 05:56:34 GMT
ENV NODE_VERSION=6.12.3
# Thu, 04 Jan 2018 05:57:13 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 04 Jan 2018 05:57:13 GMT
ENV YARN_VERSION=1.3.2
# Thu, 04 Jan 2018 05:57:15 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 04 Jan 2018 05:57:15 GMT
CMD ["node"]
# Thu, 04 Jan 2018 06:21:23 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Thu, 04 Jan 2018 06:21:23 GMT
ENV GOSU_VERSION=1.10
# Thu, 04 Jan 2018 06:21:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Thu, 04 Jan 2018 06:21:25 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Thu, 04 Jan 2018 06:21:25 GMT
WORKDIR /usr/src/ghost
# Thu, 04 Jan 2018 06:21:26 GMT
ENV GHOST_VERSION=0.11.12
# Thu, 04 Jan 2018 06:24:44 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Thu, 04 Jan 2018 06:24:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Thu, 04 Jan 2018 06:24:46 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Thu, 04 Jan 2018 06:24:46 GMT
VOLUME [/var/lib/ghost]
# Thu, 04 Jan 2018 06:24:46 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Thu, 04 Jan 2018 06:24:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Jan 2018 06:24:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2018 06:24:48 GMT
EXPOSE 2368/tcp
# Thu, 04 Jan 2018 06:24:48 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:95e140a16c792899abc97cadee0138064dd21346fe51aa332ca4cbbd5563383c`  
		Last Modified: Tue, 12 Dec 2017 13:38:47 GMT  
		Size: 48.7 MB (48691755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237499cbbf2c5155fadc128c997700f0c5ec6355ba9704d0ec3f81c29640c9c4`  
		Last Modified: Tue, 12 Dec 2017 14:30:53 GMT  
		Size: 18.3 MB (18265038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7408ea57a3c623d05d98e0e2a8d1a36968f3cfb919f8eb77dd0f3c8b0c43e2f6`  
		Last Modified: Tue, 12 Dec 2017 17:08:14 GMT  
		Size: 4.4 KB (4421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f0215d0d14824f8aa396ea7e1c57ce35f615a7ec5940d7b062e0910fb762b`  
		Last Modified: Tue, 12 Dec 2017 17:08:15 GMT  
		Size: 117.7 KB (117653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91ca6e2c719405e37da625085a7a2a0a6bfaa5cf524106550961274aa6511c3`  
		Last Modified: Thu, 04 Jan 2018 06:00:16 GMT  
		Size: 13.9 MB (13893491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed646e769eb45256e10211baf583c05c0fd8c1c5744512e9be2a1c91d5183a3`  
		Last Modified: Thu, 04 Jan 2018 06:00:12 GMT  
		Size: 1.0 MB (1010387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcd75a03ea7f7e96329e123b1b30f8b3122525ee95867980110c3f94a9f5017`  
		Last Modified: Thu, 04 Jan 2018 06:25:54 GMT  
		Size: 4.5 KB (4475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79eef35f1ac351e8eb84a1fad4985e259c4fa1ef9a1b554b80f9bf113c9c004`  
		Last Modified: Thu, 04 Jan 2018 06:25:54 GMT  
		Size: 475.3 KB (475267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62750cfb0e5747c2bf6c266163dd1cd28cdc449df05d1fdc1e7adc0839857116`  
		Last Modified: Thu, 04 Jan 2018 06:25:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadecc065c3066d71e27fe78d5aeaff9da878a4ff15f10b2eabd84df0ac6d454`  
		Last Modified: Thu, 04 Jan 2018 06:26:06 GMT  
		Size: 31.8 MB (31828808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17650e651bcba806d752e675d63c28b1088d0182a62283d9cfb4ad1c1e71bc34`  
		Last Modified: Thu, 04 Jan 2018 06:25:52 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2678a13fe628a7dadef3c86ebf430ccc7ae1032d23718373657b6d030aee945`  
		Last Modified: Thu, 04 Jan 2018 06:25:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee4f5126794b668943996d328e05c783429a6757f53b198fc2aa42f106d8db`  
		Last Modified: Thu, 04 Jan 2018 06:25:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:943089edf5197d48090c854fa53e703467782e7ef5637aeb4ff8fc2adb9ddc30
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117222156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e93268da1a134b5856f63864b7e73266a543499125b5effefe8d0eb1112b53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 14 Mar 2018 17:24:26 GMT
ADD file:bcd41493879aaeeecb9c960b91c9954b1e0229e91b7a070cb6b2dfdadc8c52b8 in / 
# Wed, 14 Mar 2018 17:24:27 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 18:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:32:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:32:54 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 17:20:46 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 17:21:12 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 17:21:13 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 17:21:17 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 17:21:18 GMT
CMD ["node"]
# Tue, 03 Apr 2018 18:16:44 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Tue, 03 Apr 2018 18:16:45 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 18:16:50 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 18:16:50 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 18:16:51 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 18:16:52 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 18:21:49 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 18:21:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 18:21:52 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 18:21:53 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 18:21:54 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Tue, 03 Apr 2018 18:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Apr 2018 18:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 18:21:57 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 18:21:57 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:21ccda36f02cc1214a990aa0c90bf9e705d50f6bf9844bffa71a8fbff898df30`  
		Last Modified: Wed, 14 Mar 2018 17:37:55 GMT  
		Size: 49.9 MB (49933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0a429742ffe0333a0070020d4aa3cfeaa1d0f87e652544b8b823ab168f1bd`  
		Last Modified: Wed, 14 Mar 2018 19:01:35 GMT  
		Size: 18.7 MB (18739890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63586fce2b79360f2899b20720f2e27aa341e7aadc0a15c96e68e3823f9704a7`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 4.4 KB (4414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc8c07863bd16bea098044bed1067f4cff1c67dcb8c2277e0ac929e47f7278`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 117.6 KB (117626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641f57e7df1914d159b6cc44e74272a61708d45911dd38659ed7a0bc8652cc0c`  
		Last Modified: Tue, 03 Apr 2018 17:44:50 GMT  
		Size: 14.7 MB (14726891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c99f90a2f0cf1c8de6b92bf7de39a380732bb3a57eb38e7f264cfaf03d55e68`  
		Last Modified: Tue, 03 Apr 2018 17:44:44 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf7bbccab4cdebf37f3263404fdef4e55ef1e68c6ccfc596f1e5c99581c1e9e`  
		Last Modified: Tue, 03 Apr 2018 18:24:39 GMT  
		Size: 4.5 KB (4478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932a0b5b6aa476a7eeda44d0b1b4f2cd438a74eb41f4631d75df710a88a4666a`  
		Last Modified: Tue, 03 Apr 2018 18:24:39 GMT  
		Size: 468.7 KB (468694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc995f347df41507949eb829e02226b7d30ebf6cc9a7909ac5ae815be21b6d93`  
		Last Modified: Tue, 03 Apr 2018 18:24:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47999a69c2bc52566e44648ec10cc30ca5612d42b9010e24cadc6463408c965`  
		Last Modified: Tue, 03 Apr 2018 18:24:54 GMT  
		Size: 32.2 MB (32164555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a21d615c23d968bd1217aaec449e04f7c1aa7e59e79d05bb45eb8e5a67d40f7`  
		Last Modified: Tue, 03 Apr 2018 18:24:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2cd40598fd498f7f251721be00ee654e13230a86e3ed6607b950316d2333bf`  
		Last Modified: Tue, 03 Apr 2018 18:24:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc22978343b04cc1f665f30a1dbfaa6ef12c946934dfb9d5c2a6d73f4e544ba`  
		Last Modified: Tue, 03 Apr 2018 18:24:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; 386

```console
$ docker pull ghost@sha256:ef5f6939cb01f67a3cc0597799e78c315bf49e76ec8742f8c9e68ca5143982c5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122519622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3174b3987e62ce95bf7708e1aa4fd77a81f685ed393ad3fb36d6032c83f714f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 10:39:32 GMT
ADD file:ce5174f2b2c155a2421fac3ff37a02d9551d5d79e31a541189bcfd2416a6903a in / 
# Sat, 28 Apr 2018 10:39:32 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:05:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 19:37:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 19:37:46 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 19:40:46 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 19:41:22 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 19:41:23 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 19:41:26 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 19:41:26 GMT
CMD ["node"]
# Sun, 29 Apr 2018 01:10:02 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sun, 29 Apr 2018 01:10:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 29 Apr 2018 01:10:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 29 Apr 2018 01:10:07 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sun, 29 Apr 2018 01:10:07 GMT
WORKDIR /usr/src/ghost
# Sun, 29 Apr 2018 01:10:07 GMT
ENV GHOST_VERSION=0.11.12
# Sun, 29 Apr 2018 01:12:14 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sun, 29 Apr 2018 01:12:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sun, 29 Apr 2018 01:12:15 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sun, 29 Apr 2018 01:12:15 GMT
VOLUME [/var/lib/ghost]
# Sun, 29 Apr 2018 01:12:15 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sun, 29 Apr 2018 01:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sun, 29 Apr 2018 01:12:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 29 Apr 2018 01:12:16 GMT
EXPOSE 2368/tcp
# Sun, 29 Apr 2018 01:12:16 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:05b419d667f793c8c2edf0ff0aec14fc4d66733cdb89957ac89e8bfbeaddd0fa`  
		Last Modified: Sat, 28 Apr 2018 10:44:20 GMT  
		Size: 54.5 MB (54486782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b9c3b7ebe34e933c240e5eb7f8620732974e6e15e2c5d17cb91ca2aefffa4`  
		Last Modified: Sat, 28 Apr 2018 12:41:22 GMT  
		Size: 19.9 MB (19866118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618a70cca8b81e7f688c7591ffb047d440d878e7c088b564e9e8611c1157dba5`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 4.4 KB (4394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2b5615162ffa8552b2e45aa789d255d2331fa388ef168bf3115fe546951502`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 117.6 KB (117613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaed2e884f6af6104db06b2e80bded57362da5e944d4989cfbeff5a34d9e92c`  
		Last Modified: Sat, 28 Apr 2018 19:49:36 GMT  
		Size: 14.3 MB (14261060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5257a1a666582990768f9724f4b53651529a7198d15c2c70284e376f9e365fc`  
		Last Modified: Sat, 28 Apr 2018 19:49:31 GMT  
		Size: 1.1 MB (1061027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844834beb3da1adb73b111366e1d988bf785843ef6dcdc4cf78b8021d3a0dd9`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9789d2bdad3cc0a62d7f4a94165126d09357ed4400a2ab0c35fbe826ab015913`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 480.6 KB (480568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7bee8581e1a4d6199827368ca6b3d023321f5b7b21a0ea47fa32a6ff3704a`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f12456a6efb1214356eee9bfa76ca82769adc9b49d02a47caf6e2b47f92ef`  
		Last Modified: Sun, 29 Apr 2018 01:15:58 GMT  
		Size: 32.2 MB (32236514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57116799470241dcd072b692a8dae3b6c7e724f9744322dc9559ca9fe6beef1`  
		Last Modified: Sun, 29 Apr 2018 01:15:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807bc6fa4ae841660a2ec8fd7e26e4c87a9213ef1f5fd4fe6a04672864515b5`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d271f91b703a51f80600acec6050328a1dbf7db812a57c9912fe59f164773d`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; ppc64le

```console
$ docker pull ghost@sha256:08d38e3b3f9814b6e9bbe1a386b0fd423b9dea01fae67028800f025f8c413ca0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119759777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205b4dc64f84c37e04b752b1d5d19d738a5f929ad54a6c2d3431af64672829cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 08:17:46 GMT
ADD file:6a4bd4ea54f669286e984ecf8178e1fa7c12c8b6fc0f96e4203ae7a6f99a2279 in / 
# Sat, 28 Apr 2018 08:17:47 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:49:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:49:27 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 16:06:30 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 16:07:44 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 16:07:46 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 16:07:54 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 16:07:55 GMT
CMD ["node"]
# Sat, 28 Apr 2018 20:31:41 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sat, 28 Apr 2018 20:31:41 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 20:31:46 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 20:31:46 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sat, 28 Apr 2018 20:31:47 GMT
WORKDIR /usr/src/ghost
# Sat, 28 Apr 2018 20:31:48 GMT
ENV GHOST_VERSION=0.11.12
# Sat, 28 Apr 2018 20:35:24 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sat, 28 Apr 2018 20:35:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sat, 28 Apr 2018 20:35:28 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sat, 28 Apr 2018 20:35:29 GMT
VOLUME [/var/lib/ghost]
# Sat, 28 Apr 2018 20:35:30 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sat, 28 Apr 2018 20:35:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Apr 2018 20:35:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 20:35:34 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 20:35:34 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:2668401c9f940b1d6b03e5f0086fa248cb957610ef9a7c79983d2fb0707ec76c`  
		Last Modified: Sat, 28 Apr 2018 08:24:36 GMT  
		Size: 53.4 MB (53392811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feb4c62e83f77f05ed3c1a72c453fce29bc8adee3ff31855937f28f0b9ad00`  
		Last Modified: Sat, 28 Apr 2018 10:38:43 GMT  
		Size: 17.6 MB (17571133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033729a6b8a78e4b13cad1f1d95e6f4ab8461fcb87c89fb4882c297de02fbad`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 4.4 KB (4438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd479c883acc5f45e3b06fe53ee3e824909480d7ee4035c57a3303a6058d3c1`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 117.7 KB (117651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5de8244112e4f1d6cb1f72cc7c9021d8f19e4df7a44412b636ab3b2dcc500d`  
		Last Modified: Sat, 28 Apr 2018 16:38:33 GMT  
		Size: 14.5 MB (14503944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbfc0285034d19463723dc2bed92d0074a197c39428886cf1bbe764a96829bd`  
		Last Modified: Sat, 28 Apr 2018 16:38:26 GMT  
		Size: 1.1 MB (1061054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1149a2cb4eee9745b4c094d6d21cb1b7411a26d289c2ab9839d5dab2d00eaf22`  
		Last Modified: Sat, 28 Apr 2018 20:37:34 GMT  
		Size: 4.5 KB (4493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87c1d75b2e07f95919646be22128d325f057a34915b478b2f940c9b20808e9`  
		Last Modified: Sat, 28 Apr 2018 20:37:34 GMT  
		Size: 469.8 KB (469846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bbf03cfcfaf60d5ff4ae48c178a7ff5f35382ac3962117e89422aa3606686a`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81578de7958d44a57ae81f362eef0feb9e362238f9ca61497f65fd355aee63c1`  
		Last Modified: Sat, 28 Apr 2018 20:37:44 GMT  
		Size: 32.6 MB (32633242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7056e33db910d8b79c06696ebbccd1dd51d374520f243c0f4c666f2b045df606`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 253.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21990cf2afd673ea5b231448f84b60f8d598e43885f9d182e169d0367de91f9a`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd63678267ec2a032258767e669e61fe8a05f9dc2428d2a4c81881d75501d26`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0` - linux; s390x

```console
$ docker pull ghost@sha256:98fa686bd911133c39e8efbcfe692a60cc49baae272d21a5414e6766b1d89106
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121453913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9bd09623e7bc0e57e125ed427b7a7ff0ad310d0d9aab43a0e02d14b43dd608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 11:42:31 GMT
ADD file:ac1cfec75c7e1898f2c9b7d17653da3684fdda7d14440ce16f1939bb66105cdc in / 
# Sat, 28 Apr 2018 11:42:31 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 13:13:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:13:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:27:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 13:27:15 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 17:51:04 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 17:51:18 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 17:51:18 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 17:51:20 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 17:51:21 GMT
CMD ["node"]
# Sat, 28 Apr 2018 21:26:22 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sat, 28 Apr 2018 21:26:23 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 21:26:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 21:26:28 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sat, 28 Apr 2018 21:26:28 GMT
WORKDIR /usr/src/ghost
# Sat, 28 Apr 2018 21:26:29 GMT
ENV GHOST_VERSION=0.11.12
# Sat, 28 Apr 2018 21:28:27 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sat, 28 Apr 2018 21:28:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sat, 28 Apr 2018 21:28:29 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sat, 28 Apr 2018 21:28:29 GMT
VOLUME [/var/lib/ghost]
# Sat, 28 Apr 2018 21:28:29 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sat, 28 Apr 2018 21:28:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Apr 2018 21:28:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 21:28:30 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 21:28:30 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e0524893a6d25f3e36c190fea678ecf1845e7c0d2ba833b077a429d64b943e0a`  
		Last Modified: Sat, 28 Apr 2018 11:47:52 GMT  
		Size: 54.5 MB (54465857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331cf8e884c1052e19f6b80b3efb54a7163ab49bf54c631bd861332c232029f`  
		Last Modified: Sat, 28 Apr 2018 13:29:06 GMT  
		Size: 17.8 MB (17767296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1573c40a4e9e40c7d5639586badca4c9ac2080488a599636910b77ac19a689`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd78e74bc99cbd7061122cf0fe9a054fb495f9bef7ef1502f65f98935d869fb`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 117.6 KB (117619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffe8a451803f5c963bc7fe27269ca01a9b6c131bcd1e034753682cd9a541d8`  
		Last Modified: Sat, 28 Apr 2018 17:57:39 GMT  
		Size: 14.9 MB (14874582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a235333140b41b4b113ac11697676cd325aeb3a46bcc9b1fd3e651dabb7cecd`  
		Last Modified: Sat, 28 Apr 2018 17:57:35 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a171f9a26483009feb5429cf10abcdbde3fdca46d40e5b14ccd68d79e207739`  
		Last Modified: Sat, 28 Apr 2018 21:29:51 GMT  
		Size: 4.5 KB (4458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6078238ec1d2a568460bf65cc9de23145d2c3e077602a1723d767ce08c12ea20`  
		Last Modified: Sat, 28 Apr 2018 21:29:50 GMT  
		Size: 486.8 KB (486820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2486b66854d7e889b03b37cb8eef2142f24b563db36acfbae10418c2ab42be8d`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a651b89b09b8a01ee8c66a42fcab842cd8aa39c725f36a23e46f6031ba0620fd`  
		Last Modified: Sat, 28 Apr 2018 21:30:00 GMT  
		Size: 32.7 MB (32670732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aec065995b11f80609e45643d443f1942a27e7289ad5405c86a71fd3c042687`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c34027c16b3ca4fbe8d26a43b559c708169acb574682e0cd9d4fb37e584a4`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c4596a07033948943bf374a7584778441fa39e2a0852553a64b49d1f2fe5a0`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11`

```console
$ docker pull ghost@sha256:bacb8330293d2cb71eda62af696cce318164c5a93285183fb9f2b60fe9e0fb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:0.11` - linux; amd64

```console
$ docker pull ghost@sha256:b92f1bc2512a5e1bbb6901aa732e24cc96c93fabc6442e7de7c9e6ccf05170dc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113786323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8ca5cdf069950b6f388c0f4f3cc6f2fefed7d3a9702bdb10b346c13141379f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:03:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:03:53 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 01:31:24 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:31:50 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 01:31:51 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:31:55 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 01:31:55 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:51:09 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Tue, 03 Apr 2018 03:51:09 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 03:51:15 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 03:51:15 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 03:51:15 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 03:51:15 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 03:52:32 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 03:52:33 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 03:52:34 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 03:52:34 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 03:52:34 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Tue, 03 Apr 2018 03:52:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Apr 2018 03:52:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 03:52:36 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 03:52:36 GMT
CMD ["npm" "start"]
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
	-	`sha256:c669d5da499dfc3f959bff647d84aa109d42bd9dc4a84cd1736607a9a193931e`  
		Last Modified: Thu, 15 Mar 2018 05:16:20 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8ff4c87216eb5e2bdc5aeab7d50e312312df3b9358eac4f84cd10c0db8d7c`  
		Last Modified: Thu, 15 Mar 2018 05:16:18 GMT  
		Size: 117.6 KB (117624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d93f330ca2fc79c95fa142b121be257ae64491015b8997cd012096fbd113fb`  
		Last Modified: Tue, 03 Apr 2018 02:26:55 GMT  
		Size: 14.7 MB (14743833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5858a3ea9339b3a6db832ae2fbb00a02d8b6475f2af80f473668cd6e3f468e`  
		Last Modified: Tue, 03 Apr 2018 02:26:50 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c1052636ab321eee45cc1619becae1525ac9392854707536e6c03fd7280fb3`  
		Last Modified: Tue, 03 Apr 2018 04:29:27 GMT  
		Size: 4.5 KB (4463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8925eb724b45a3ccb2460c08b1047a3306b9dbec9ea185971e2d7c6bd51f3d`  
		Last Modified: Tue, 03 Apr 2018 04:29:28 GMT  
		Size: 500.7 KB (500671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c31ef7135d57fa0312b48beac94e99e9d44a3f5eb5805bc45c6d47d4e50613`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b8c39ec852f876618629bb0b256034ac40c79ef24030cc2fda1ff1a825cf5a`  
		Last Modified: Tue, 03 Apr 2018 04:29:43 GMT  
		Size: 25.5 MB (25478478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3276306d6c16c4cc43f841cd645202c5ab36078d6355619c80ef57ef22184b33`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e4eadce21ee792c3f70a75ffb7be3a8095364aaff12c78faecdddad41151a9`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadb91902da8a85e2b892633445c7e54bdfaee61858b2562452d914f414e8bd8`  
		Last Modified: Tue, 03 Apr 2018 04:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; arm variant v7

```console
$ docker pull ghost@sha256:8f5618b2a3def4ba2b777bed71b4f6bdfa57d96b9591fa81d40769b804096325
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114292463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0bf8068e56597b32dff6a34f2f52cdbf822c6f47d12af9038f1814589bdf97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:05 GMT
ADD file:aeb57f3a84dc1b93e1d38a80409a407df553344149d5070ed79b656865c90c54 in / 
# Tue, 12 Dec 2017 13:27:06 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:14:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 16:51:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 12 Dec 2017 16:51:03 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 04 Jan 2018 05:56:34 GMT
ENV NODE_VERSION=6.12.3
# Thu, 04 Jan 2018 05:57:13 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 04 Jan 2018 05:57:13 GMT
ENV YARN_VERSION=1.3.2
# Thu, 04 Jan 2018 05:57:15 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 04 Jan 2018 05:57:15 GMT
CMD ["node"]
# Thu, 04 Jan 2018 06:21:23 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Thu, 04 Jan 2018 06:21:23 GMT
ENV GOSU_VERSION=1.10
# Thu, 04 Jan 2018 06:21:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Thu, 04 Jan 2018 06:21:25 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Thu, 04 Jan 2018 06:21:25 GMT
WORKDIR /usr/src/ghost
# Thu, 04 Jan 2018 06:21:26 GMT
ENV GHOST_VERSION=0.11.12
# Thu, 04 Jan 2018 06:24:44 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Thu, 04 Jan 2018 06:24:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Thu, 04 Jan 2018 06:24:46 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Thu, 04 Jan 2018 06:24:46 GMT
VOLUME [/var/lib/ghost]
# Thu, 04 Jan 2018 06:24:46 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Thu, 04 Jan 2018 06:24:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Jan 2018 06:24:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2018 06:24:48 GMT
EXPOSE 2368/tcp
# Thu, 04 Jan 2018 06:24:48 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:95e140a16c792899abc97cadee0138064dd21346fe51aa332ca4cbbd5563383c`  
		Last Modified: Tue, 12 Dec 2017 13:38:47 GMT  
		Size: 48.7 MB (48691755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237499cbbf2c5155fadc128c997700f0c5ec6355ba9704d0ec3f81c29640c9c4`  
		Last Modified: Tue, 12 Dec 2017 14:30:53 GMT  
		Size: 18.3 MB (18265038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7408ea57a3c623d05d98e0e2a8d1a36968f3cfb919f8eb77dd0f3c8b0c43e2f6`  
		Last Modified: Tue, 12 Dec 2017 17:08:14 GMT  
		Size: 4.4 KB (4421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f0215d0d14824f8aa396ea7e1c57ce35f615a7ec5940d7b062e0910fb762b`  
		Last Modified: Tue, 12 Dec 2017 17:08:15 GMT  
		Size: 117.7 KB (117653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91ca6e2c719405e37da625085a7a2a0a6bfaa5cf524106550961274aa6511c3`  
		Last Modified: Thu, 04 Jan 2018 06:00:16 GMT  
		Size: 13.9 MB (13893491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed646e769eb45256e10211baf583c05c0fd8c1c5744512e9be2a1c91d5183a3`  
		Last Modified: Thu, 04 Jan 2018 06:00:12 GMT  
		Size: 1.0 MB (1010387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcd75a03ea7f7e96329e123b1b30f8b3122525ee95867980110c3f94a9f5017`  
		Last Modified: Thu, 04 Jan 2018 06:25:54 GMT  
		Size: 4.5 KB (4475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79eef35f1ac351e8eb84a1fad4985e259c4fa1ef9a1b554b80f9bf113c9c004`  
		Last Modified: Thu, 04 Jan 2018 06:25:54 GMT  
		Size: 475.3 KB (475267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62750cfb0e5747c2bf6c266163dd1cd28cdc449df05d1fdc1e7adc0839857116`  
		Last Modified: Thu, 04 Jan 2018 06:25:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadecc065c3066d71e27fe78d5aeaff9da878a4ff15f10b2eabd84df0ac6d454`  
		Last Modified: Thu, 04 Jan 2018 06:26:06 GMT  
		Size: 31.8 MB (31828808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17650e651bcba806d752e675d63c28b1088d0182a62283d9cfb4ad1c1e71bc34`  
		Last Modified: Thu, 04 Jan 2018 06:25:52 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2678a13fe628a7dadef3c86ebf430ccc7ae1032d23718373657b6d030aee945`  
		Last Modified: Thu, 04 Jan 2018 06:25:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee4f5126794b668943996d328e05c783429a6757f53b198fc2aa42f106d8db`  
		Last Modified: Thu, 04 Jan 2018 06:25:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:943089edf5197d48090c854fa53e703467782e7ef5637aeb4ff8fc2adb9ddc30
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117222156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e93268da1a134b5856f63864b7e73266a543499125b5effefe8d0eb1112b53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 14 Mar 2018 17:24:26 GMT
ADD file:bcd41493879aaeeecb9c960b91c9954b1e0229e91b7a070cb6b2dfdadc8c52b8 in / 
# Wed, 14 Mar 2018 17:24:27 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 18:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:32:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:32:54 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 17:20:46 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 17:21:12 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 17:21:13 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 17:21:17 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 17:21:18 GMT
CMD ["node"]
# Tue, 03 Apr 2018 18:16:44 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Tue, 03 Apr 2018 18:16:45 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 18:16:50 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 18:16:50 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 18:16:51 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 18:16:52 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 18:21:49 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 18:21:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 18:21:52 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 18:21:53 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 18:21:54 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Tue, 03 Apr 2018 18:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Apr 2018 18:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 18:21:57 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 18:21:57 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:21ccda36f02cc1214a990aa0c90bf9e705d50f6bf9844bffa71a8fbff898df30`  
		Last Modified: Wed, 14 Mar 2018 17:37:55 GMT  
		Size: 49.9 MB (49933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0a429742ffe0333a0070020d4aa3cfeaa1d0f87e652544b8b823ab168f1bd`  
		Last Modified: Wed, 14 Mar 2018 19:01:35 GMT  
		Size: 18.7 MB (18739890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63586fce2b79360f2899b20720f2e27aa341e7aadc0a15c96e68e3823f9704a7`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 4.4 KB (4414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc8c07863bd16bea098044bed1067f4cff1c67dcb8c2277e0ac929e47f7278`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 117.6 KB (117626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641f57e7df1914d159b6cc44e74272a61708d45911dd38659ed7a0bc8652cc0c`  
		Last Modified: Tue, 03 Apr 2018 17:44:50 GMT  
		Size: 14.7 MB (14726891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c99f90a2f0cf1c8de6b92bf7de39a380732bb3a57eb38e7f264cfaf03d55e68`  
		Last Modified: Tue, 03 Apr 2018 17:44:44 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf7bbccab4cdebf37f3263404fdef4e55ef1e68c6ccfc596f1e5c99581c1e9e`  
		Last Modified: Tue, 03 Apr 2018 18:24:39 GMT  
		Size: 4.5 KB (4478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932a0b5b6aa476a7eeda44d0b1b4f2cd438a74eb41f4631d75df710a88a4666a`  
		Last Modified: Tue, 03 Apr 2018 18:24:39 GMT  
		Size: 468.7 KB (468694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc995f347df41507949eb829e02226b7d30ebf6cc9a7909ac5ae815be21b6d93`  
		Last Modified: Tue, 03 Apr 2018 18:24:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47999a69c2bc52566e44648ec10cc30ca5612d42b9010e24cadc6463408c965`  
		Last Modified: Tue, 03 Apr 2018 18:24:54 GMT  
		Size: 32.2 MB (32164555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a21d615c23d968bd1217aaec449e04f7c1aa7e59e79d05bb45eb8e5a67d40f7`  
		Last Modified: Tue, 03 Apr 2018 18:24:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2cd40598fd498f7f251721be00ee654e13230a86e3ed6607b950316d2333bf`  
		Last Modified: Tue, 03 Apr 2018 18:24:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc22978343b04cc1f665f30a1dbfaa6ef12c946934dfb9d5c2a6d73f4e544ba`  
		Last Modified: Tue, 03 Apr 2018 18:24:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; 386

```console
$ docker pull ghost@sha256:ef5f6939cb01f67a3cc0597799e78c315bf49e76ec8742f8c9e68ca5143982c5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122519622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3174b3987e62ce95bf7708e1aa4fd77a81f685ed393ad3fb36d6032c83f714f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 10:39:32 GMT
ADD file:ce5174f2b2c155a2421fac3ff37a02d9551d5d79e31a541189bcfd2416a6903a in / 
# Sat, 28 Apr 2018 10:39:32 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:05:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 19:37:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 19:37:46 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 19:40:46 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 19:41:22 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 19:41:23 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 19:41:26 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 19:41:26 GMT
CMD ["node"]
# Sun, 29 Apr 2018 01:10:02 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sun, 29 Apr 2018 01:10:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 29 Apr 2018 01:10:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 29 Apr 2018 01:10:07 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sun, 29 Apr 2018 01:10:07 GMT
WORKDIR /usr/src/ghost
# Sun, 29 Apr 2018 01:10:07 GMT
ENV GHOST_VERSION=0.11.12
# Sun, 29 Apr 2018 01:12:14 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sun, 29 Apr 2018 01:12:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sun, 29 Apr 2018 01:12:15 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sun, 29 Apr 2018 01:12:15 GMT
VOLUME [/var/lib/ghost]
# Sun, 29 Apr 2018 01:12:15 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sun, 29 Apr 2018 01:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sun, 29 Apr 2018 01:12:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 29 Apr 2018 01:12:16 GMT
EXPOSE 2368/tcp
# Sun, 29 Apr 2018 01:12:16 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:05b419d667f793c8c2edf0ff0aec14fc4d66733cdb89957ac89e8bfbeaddd0fa`  
		Last Modified: Sat, 28 Apr 2018 10:44:20 GMT  
		Size: 54.5 MB (54486782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b9c3b7ebe34e933c240e5eb7f8620732974e6e15e2c5d17cb91ca2aefffa4`  
		Last Modified: Sat, 28 Apr 2018 12:41:22 GMT  
		Size: 19.9 MB (19866118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618a70cca8b81e7f688c7591ffb047d440d878e7c088b564e9e8611c1157dba5`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 4.4 KB (4394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2b5615162ffa8552b2e45aa789d255d2331fa388ef168bf3115fe546951502`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 117.6 KB (117613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaed2e884f6af6104db06b2e80bded57362da5e944d4989cfbeff5a34d9e92c`  
		Last Modified: Sat, 28 Apr 2018 19:49:36 GMT  
		Size: 14.3 MB (14261060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5257a1a666582990768f9724f4b53651529a7198d15c2c70284e376f9e365fc`  
		Last Modified: Sat, 28 Apr 2018 19:49:31 GMT  
		Size: 1.1 MB (1061027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844834beb3da1adb73b111366e1d988bf785843ef6dcdc4cf78b8021d3a0dd9`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9789d2bdad3cc0a62d7f4a94165126d09357ed4400a2ab0c35fbe826ab015913`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 480.6 KB (480568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7bee8581e1a4d6199827368ca6b3d023321f5b7b21a0ea47fa32a6ff3704a`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f12456a6efb1214356eee9bfa76ca82769adc9b49d02a47caf6e2b47f92ef`  
		Last Modified: Sun, 29 Apr 2018 01:15:58 GMT  
		Size: 32.2 MB (32236514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57116799470241dcd072b692a8dae3b6c7e724f9744322dc9559ca9fe6beef1`  
		Last Modified: Sun, 29 Apr 2018 01:15:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807bc6fa4ae841660a2ec8fd7e26e4c87a9213ef1f5fd4fe6a04672864515b5`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d271f91b703a51f80600acec6050328a1dbf7db812a57c9912fe59f164773d`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; ppc64le

```console
$ docker pull ghost@sha256:08d38e3b3f9814b6e9bbe1a386b0fd423b9dea01fae67028800f025f8c413ca0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119759777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205b4dc64f84c37e04b752b1d5d19d738a5f929ad54a6c2d3431af64672829cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 08:17:46 GMT
ADD file:6a4bd4ea54f669286e984ecf8178e1fa7c12c8b6fc0f96e4203ae7a6f99a2279 in / 
# Sat, 28 Apr 2018 08:17:47 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:49:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:49:27 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 16:06:30 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 16:07:44 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 16:07:46 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 16:07:54 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 16:07:55 GMT
CMD ["node"]
# Sat, 28 Apr 2018 20:31:41 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sat, 28 Apr 2018 20:31:41 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 20:31:46 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 20:31:46 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sat, 28 Apr 2018 20:31:47 GMT
WORKDIR /usr/src/ghost
# Sat, 28 Apr 2018 20:31:48 GMT
ENV GHOST_VERSION=0.11.12
# Sat, 28 Apr 2018 20:35:24 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sat, 28 Apr 2018 20:35:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sat, 28 Apr 2018 20:35:28 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sat, 28 Apr 2018 20:35:29 GMT
VOLUME [/var/lib/ghost]
# Sat, 28 Apr 2018 20:35:30 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sat, 28 Apr 2018 20:35:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Apr 2018 20:35:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 20:35:34 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 20:35:34 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:2668401c9f940b1d6b03e5f0086fa248cb957610ef9a7c79983d2fb0707ec76c`  
		Last Modified: Sat, 28 Apr 2018 08:24:36 GMT  
		Size: 53.4 MB (53392811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feb4c62e83f77f05ed3c1a72c453fce29bc8adee3ff31855937f28f0b9ad00`  
		Last Modified: Sat, 28 Apr 2018 10:38:43 GMT  
		Size: 17.6 MB (17571133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033729a6b8a78e4b13cad1f1d95e6f4ab8461fcb87c89fb4882c297de02fbad`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 4.4 KB (4438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd479c883acc5f45e3b06fe53ee3e824909480d7ee4035c57a3303a6058d3c1`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 117.7 KB (117651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5de8244112e4f1d6cb1f72cc7c9021d8f19e4df7a44412b636ab3b2dcc500d`  
		Last Modified: Sat, 28 Apr 2018 16:38:33 GMT  
		Size: 14.5 MB (14503944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbfc0285034d19463723dc2bed92d0074a197c39428886cf1bbe764a96829bd`  
		Last Modified: Sat, 28 Apr 2018 16:38:26 GMT  
		Size: 1.1 MB (1061054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1149a2cb4eee9745b4c094d6d21cb1b7411a26d289c2ab9839d5dab2d00eaf22`  
		Last Modified: Sat, 28 Apr 2018 20:37:34 GMT  
		Size: 4.5 KB (4493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87c1d75b2e07f95919646be22128d325f057a34915b478b2f940c9b20808e9`  
		Last Modified: Sat, 28 Apr 2018 20:37:34 GMT  
		Size: 469.8 KB (469846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bbf03cfcfaf60d5ff4ae48c178a7ff5f35382ac3962117e89422aa3606686a`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81578de7958d44a57ae81f362eef0feb9e362238f9ca61497f65fd355aee63c1`  
		Last Modified: Sat, 28 Apr 2018 20:37:44 GMT  
		Size: 32.6 MB (32633242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7056e33db910d8b79c06696ebbccd1dd51d374520f243c0f4c666f2b045df606`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 253.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21990cf2afd673ea5b231448f84b60f8d598e43885f9d182e169d0367de91f9a`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd63678267ec2a032258767e669e61fe8a05f9dc2428d2a4c81881d75501d26`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11` - linux; s390x

```console
$ docker pull ghost@sha256:98fa686bd911133c39e8efbcfe692a60cc49baae272d21a5414e6766b1d89106
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121453913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9bd09623e7bc0e57e125ed427b7a7ff0ad310d0d9aab43a0e02d14b43dd608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 11:42:31 GMT
ADD file:ac1cfec75c7e1898f2c9b7d17653da3684fdda7d14440ce16f1939bb66105cdc in / 
# Sat, 28 Apr 2018 11:42:31 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 13:13:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:13:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:27:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 13:27:15 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 17:51:04 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 17:51:18 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 17:51:18 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 17:51:20 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 17:51:21 GMT
CMD ["node"]
# Sat, 28 Apr 2018 21:26:22 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sat, 28 Apr 2018 21:26:23 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 21:26:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 21:26:28 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sat, 28 Apr 2018 21:26:28 GMT
WORKDIR /usr/src/ghost
# Sat, 28 Apr 2018 21:26:29 GMT
ENV GHOST_VERSION=0.11.12
# Sat, 28 Apr 2018 21:28:27 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sat, 28 Apr 2018 21:28:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sat, 28 Apr 2018 21:28:29 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sat, 28 Apr 2018 21:28:29 GMT
VOLUME [/var/lib/ghost]
# Sat, 28 Apr 2018 21:28:29 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sat, 28 Apr 2018 21:28:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Apr 2018 21:28:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 21:28:30 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 21:28:30 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e0524893a6d25f3e36c190fea678ecf1845e7c0d2ba833b077a429d64b943e0a`  
		Last Modified: Sat, 28 Apr 2018 11:47:52 GMT  
		Size: 54.5 MB (54465857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331cf8e884c1052e19f6b80b3efb54a7163ab49bf54c631bd861332c232029f`  
		Last Modified: Sat, 28 Apr 2018 13:29:06 GMT  
		Size: 17.8 MB (17767296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1573c40a4e9e40c7d5639586badca4c9ac2080488a599636910b77ac19a689`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd78e74bc99cbd7061122cf0fe9a054fb495f9bef7ef1502f65f98935d869fb`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 117.6 KB (117619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffe8a451803f5c963bc7fe27269ca01a9b6c131bcd1e034753682cd9a541d8`  
		Last Modified: Sat, 28 Apr 2018 17:57:39 GMT  
		Size: 14.9 MB (14874582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a235333140b41b4b113ac11697676cd325aeb3a46bcc9b1fd3e651dabb7cecd`  
		Last Modified: Sat, 28 Apr 2018 17:57:35 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a171f9a26483009feb5429cf10abcdbde3fdca46d40e5b14ccd68d79e207739`  
		Last Modified: Sat, 28 Apr 2018 21:29:51 GMT  
		Size: 4.5 KB (4458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6078238ec1d2a568460bf65cc9de23145d2c3e077602a1723d767ce08c12ea20`  
		Last Modified: Sat, 28 Apr 2018 21:29:50 GMT  
		Size: 486.8 KB (486820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2486b66854d7e889b03b37cb8eef2142f24b563db36acfbae10418c2ab42be8d`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a651b89b09b8a01ee8c66a42fcab842cd8aa39c725f36a23e46f6031ba0620fd`  
		Last Modified: Sat, 28 Apr 2018 21:30:00 GMT  
		Size: 32.7 MB (32670732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aec065995b11f80609e45643d443f1942a27e7289ad5405c86a71fd3c042687`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c34027c16b3ca4fbe8d26a43b559c708169acb574682e0cd9d4fb37e584a4`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c4596a07033948943bf374a7584778441fa39e2a0852553a64b49d1f2fe5a0`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11.12`

```console
$ docker pull ghost@sha256:bacb8330293d2cb71eda62af696cce318164c5a93285183fb9f2b60fe9e0fb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:0.11.12` - linux; amd64

```console
$ docker pull ghost@sha256:b92f1bc2512a5e1bbb6901aa732e24cc96c93fabc6442e7de7c9e6ccf05170dc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113786323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa8ca5cdf069950b6f388c0f4f3cc6f2fefed7d3a9702bdb10b346c13141379f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:03:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:03:53 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 01:31:24 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:31:50 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 01:31:51 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:31:55 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 01:31:55 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:51:09 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Tue, 03 Apr 2018 03:51:09 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 03:51:15 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 03:51:15 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 03:51:15 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 03:51:15 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 03:52:32 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 03:52:33 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 03:52:34 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 03:52:34 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 03:52:34 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Tue, 03 Apr 2018 03:52:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Apr 2018 03:52:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 03:52:36 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 03:52:36 GMT
CMD ["npm" "start"]
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
	-	`sha256:c669d5da499dfc3f959bff647d84aa109d42bd9dc4a84cd1736607a9a193931e`  
		Last Modified: Thu, 15 Mar 2018 05:16:20 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8ff4c87216eb5e2bdc5aeab7d50e312312df3b9358eac4f84cd10c0db8d7c`  
		Last Modified: Thu, 15 Mar 2018 05:16:18 GMT  
		Size: 117.6 KB (117624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d93f330ca2fc79c95fa142b121be257ae64491015b8997cd012096fbd113fb`  
		Last Modified: Tue, 03 Apr 2018 02:26:55 GMT  
		Size: 14.7 MB (14743833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5858a3ea9339b3a6db832ae2fbb00a02d8b6475f2af80f473668cd6e3f468e`  
		Last Modified: Tue, 03 Apr 2018 02:26:50 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c1052636ab321eee45cc1619becae1525ac9392854707536e6c03fd7280fb3`  
		Last Modified: Tue, 03 Apr 2018 04:29:27 GMT  
		Size: 4.5 KB (4463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8925eb724b45a3ccb2460c08b1047a3306b9dbec9ea185971e2d7c6bd51f3d`  
		Last Modified: Tue, 03 Apr 2018 04:29:28 GMT  
		Size: 500.7 KB (500671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c31ef7135d57fa0312b48beac94e99e9d44a3f5eb5805bc45c6d47d4e50613`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b8c39ec852f876618629bb0b256034ac40c79ef24030cc2fda1ff1a825cf5a`  
		Last Modified: Tue, 03 Apr 2018 04:29:43 GMT  
		Size: 25.5 MB (25478478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3276306d6c16c4cc43f841cd645202c5ab36078d6355619c80ef57ef22184b33`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e4eadce21ee792c3f70a75ffb7be3a8095364aaff12c78faecdddad41151a9`  
		Last Modified: Tue, 03 Apr 2018 04:29:25 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadb91902da8a85e2b892633445c7e54bdfaee61858b2562452d914f414e8bd8`  
		Last Modified: Tue, 03 Apr 2018 04:29:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.12` - linux; arm variant v7

```console
$ docker pull ghost@sha256:8f5618b2a3def4ba2b777bed71b4f6bdfa57d96b9591fa81d40769b804096325
```

-	Docker Version: 17.06.0-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114292463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0bf8068e56597b32dff6a34f2f52cdbf822c6f47d12af9038f1814589bdf97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 12 Dec 2017 13:27:05 GMT
ADD file:aeb57f3a84dc1b93e1d38a80409a407df553344149d5070ed79b656865c90c54 in / 
# Tue, 12 Dec 2017 13:27:06 GMT
CMD ["bash"]
# Tue, 12 Dec 2017 14:14:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Dec 2017 14:14:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Dec 2017 16:51:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 12 Dec 2017 16:51:03 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done
# Thu, 04 Jan 2018 05:56:34 GMT
ENV NODE_VERSION=6.12.3
# Thu, 04 Jan 2018 05:57:13 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Thu, 04 Jan 2018 05:57:13 GMT
ENV YARN_VERSION=1.3.2
# Thu, 04 Jan 2018 05:57:15 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver pgp.mit.edu --recv-keys "$key" ||     gpg --keyserver keyserver.pgp.com --recv-keys "$key" ||     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Thu, 04 Jan 2018 05:57:15 GMT
CMD ["node"]
# Thu, 04 Jan 2018 06:21:23 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Thu, 04 Jan 2018 06:21:23 GMT
ENV GOSU_VERSION=1.10
# Thu, 04 Jan 2018 06:21:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Thu, 04 Jan 2018 06:21:25 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Thu, 04 Jan 2018 06:21:25 GMT
WORKDIR /usr/src/ghost
# Thu, 04 Jan 2018 06:21:26 GMT
ENV GHOST_VERSION=0.11.12
# Thu, 04 Jan 2018 06:24:44 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Thu, 04 Jan 2018 06:24:45 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Thu, 04 Jan 2018 06:24:46 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Thu, 04 Jan 2018 06:24:46 GMT
VOLUME [/var/lib/ghost]
# Thu, 04 Jan 2018 06:24:46 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Thu, 04 Jan 2018 06:24:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Jan 2018 06:24:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Jan 2018 06:24:48 GMT
EXPOSE 2368/tcp
# Thu, 04 Jan 2018 06:24:48 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:95e140a16c792899abc97cadee0138064dd21346fe51aa332ca4cbbd5563383c`  
		Last Modified: Tue, 12 Dec 2017 13:38:47 GMT  
		Size: 48.7 MB (48691755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237499cbbf2c5155fadc128c997700f0c5ec6355ba9704d0ec3f81c29640c9c4`  
		Last Modified: Tue, 12 Dec 2017 14:30:53 GMT  
		Size: 18.3 MB (18265038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7408ea57a3c623d05d98e0e2a8d1a36968f3cfb919f8eb77dd0f3c8b0c43e2f6`  
		Last Modified: Tue, 12 Dec 2017 17:08:14 GMT  
		Size: 4.4 KB (4421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f0215d0d14824f8aa396ea7e1c57ce35f615a7ec5940d7b062e0910fb762b`  
		Last Modified: Tue, 12 Dec 2017 17:08:15 GMT  
		Size: 117.7 KB (117653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91ca6e2c719405e37da625085a7a2a0a6bfaa5cf524106550961274aa6511c3`  
		Last Modified: Thu, 04 Jan 2018 06:00:16 GMT  
		Size: 13.9 MB (13893491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed646e769eb45256e10211baf583c05c0fd8c1c5744512e9be2a1c91d5183a3`  
		Last Modified: Thu, 04 Jan 2018 06:00:12 GMT  
		Size: 1.0 MB (1010387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcd75a03ea7f7e96329e123b1b30f8b3122525ee95867980110c3f94a9f5017`  
		Last Modified: Thu, 04 Jan 2018 06:25:54 GMT  
		Size: 4.5 KB (4475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79eef35f1ac351e8eb84a1fad4985e259c4fa1ef9a1b554b80f9bf113c9c004`  
		Last Modified: Thu, 04 Jan 2018 06:25:54 GMT  
		Size: 475.3 KB (475267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62750cfb0e5747c2bf6c266163dd1cd28cdc449df05d1fdc1e7adc0839857116`  
		Last Modified: Thu, 04 Jan 2018 06:25:53 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cadecc065c3066d71e27fe78d5aeaff9da878a4ff15f10b2eabd84df0ac6d454`  
		Last Modified: Thu, 04 Jan 2018 06:26:06 GMT  
		Size: 31.8 MB (31828808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17650e651bcba806d752e675d63c28b1088d0182a62283d9cfb4ad1c1e71bc34`  
		Last Modified: Thu, 04 Jan 2018 06:25:52 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2678a13fe628a7dadef3c86ebf430ccc7ae1032d23718373657b6d030aee945`  
		Last Modified: Thu, 04 Jan 2018 06:25:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee4f5126794b668943996d328e05c783429a6757f53b198fc2aa42f106d8db`  
		Last Modified: Thu, 04 Jan 2018 06:25:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.12` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:943089edf5197d48090c854fa53e703467782e7ef5637aeb4ff8fc2adb9ddc30
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117222156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e93268da1a134b5856f63864b7e73266a543499125b5effefe8d0eb1112b53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Wed, 14 Mar 2018 17:24:26 GMT
ADD file:bcd41493879aaeeecb9c960b91c9954b1e0229e91b7a070cb6b2dfdadc8c52b8 in / 
# Wed, 14 Mar 2018 17:24:27 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 18:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:32:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:32:54 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 17:20:46 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 17:21:12 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 17:21:13 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 17:21:17 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 17:21:18 GMT
CMD ["node"]
# Tue, 03 Apr 2018 18:16:44 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Tue, 03 Apr 2018 18:16:45 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 18:16:50 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 18:16:50 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 18:16:51 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 18:16:52 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 18:21:49 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 18:21:50 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 18:21:52 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 18:21:53 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 18:21:54 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Tue, 03 Apr 2018 18:21:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 03 Apr 2018 18:21:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 18:21:57 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 18:21:57 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:21ccda36f02cc1214a990aa0c90bf9e705d50f6bf9844bffa71a8fbff898df30`  
		Last Modified: Wed, 14 Mar 2018 17:37:55 GMT  
		Size: 49.9 MB (49933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0a429742ffe0333a0070020d4aa3cfeaa1d0f87e652544b8b823ab168f1bd`  
		Last Modified: Wed, 14 Mar 2018 19:01:35 GMT  
		Size: 18.7 MB (18739890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63586fce2b79360f2899b20720f2e27aa341e7aadc0a15c96e68e3823f9704a7`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 4.4 KB (4414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc8c07863bd16bea098044bed1067f4cff1c67dcb8c2277e0ac929e47f7278`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 117.6 KB (117626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641f57e7df1914d159b6cc44e74272a61708d45911dd38659ed7a0bc8652cc0c`  
		Last Modified: Tue, 03 Apr 2018 17:44:50 GMT  
		Size: 14.7 MB (14726891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c99f90a2f0cf1c8de6b92bf7de39a380732bb3a57eb38e7f264cfaf03d55e68`  
		Last Modified: Tue, 03 Apr 2018 17:44:44 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf7bbccab4cdebf37f3263404fdef4e55ef1e68c6ccfc596f1e5c99581c1e9e`  
		Last Modified: Tue, 03 Apr 2018 18:24:39 GMT  
		Size: 4.5 KB (4478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932a0b5b6aa476a7eeda44d0b1b4f2cd438a74eb41f4631d75df710a88a4666a`  
		Last Modified: Tue, 03 Apr 2018 18:24:39 GMT  
		Size: 468.7 KB (468694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc995f347df41507949eb829e02226b7d30ebf6cc9a7909ac5ae815be21b6d93`  
		Last Modified: Tue, 03 Apr 2018 18:24:38 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47999a69c2bc52566e44648ec10cc30ca5612d42b9010e24cadc6463408c965`  
		Last Modified: Tue, 03 Apr 2018 18:24:54 GMT  
		Size: 32.2 MB (32164555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a21d615c23d968bd1217aaec449e04f7c1aa7e59e79d05bb45eb8e5a67d40f7`  
		Last Modified: Tue, 03 Apr 2018 18:24:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2cd40598fd498f7f251721be00ee654e13230a86e3ed6607b950316d2333bf`  
		Last Modified: Tue, 03 Apr 2018 18:24:37 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc22978343b04cc1f665f30a1dbfaa6ef12c946934dfb9d5c2a6d73f4e544ba`  
		Last Modified: Tue, 03 Apr 2018 18:24:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.12` - linux; 386

```console
$ docker pull ghost@sha256:ef5f6939cb01f67a3cc0597799e78c315bf49e76ec8742f8c9e68ca5143982c5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122519622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3174b3987e62ce95bf7708e1aa4fd77a81f685ed393ad3fb36d6032c83f714f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 10:39:32 GMT
ADD file:ce5174f2b2c155a2421fac3ff37a02d9551d5d79e31a541189bcfd2416a6903a in / 
# Sat, 28 Apr 2018 10:39:32 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:05:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 19:37:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 19:37:46 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 19:40:46 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 19:41:22 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 19:41:23 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 19:41:26 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 19:41:26 GMT
CMD ["node"]
# Sun, 29 Apr 2018 01:10:02 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sun, 29 Apr 2018 01:10:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 29 Apr 2018 01:10:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 29 Apr 2018 01:10:07 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sun, 29 Apr 2018 01:10:07 GMT
WORKDIR /usr/src/ghost
# Sun, 29 Apr 2018 01:10:07 GMT
ENV GHOST_VERSION=0.11.12
# Sun, 29 Apr 2018 01:12:14 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sun, 29 Apr 2018 01:12:14 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sun, 29 Apr 2018 01:12:15 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sun, 29 Apr 2018 01:12:15 GMT
VOLUME [/var/lib/ghost]
# Sun, 29 Apr 2018 01:12:15 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sun, 29 Apr 2018 01:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sun, 29 Apr 2018 01:12:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 29 Apr 2018 01:12:16 GMT
EXPOSE 2368/tcp
# Sun, 29 Apr 2018 01:12:16 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:05b419d667f793c8c2edf0ff0aec14fc4d66733cdb89957ac89e8bfbeaddd0fa`  
		Last Modified: Sat, 28 Apr 2018 10:44:20 GMT  
		Size: 54.5 MB (54486782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b9c3b7ebe34e933c240e5eb7f8620732974e6e15e2c5d17cb91ca2aefffa4`  
		Last Modified: Sat, 28 Apr 2018 12:41:22 GMT  
		Size: 19.9 MB (19866118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618a70cca8b81e7f688c7591ffb047d440d878e7c088b564e9e8611c1157dba5`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 4.4 KB (4394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2b5615162ffa8552b2e45aa789d255d2331fa388ef168bf3115fe546951502`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 117.6 KB (117613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaed2e884f6af6104db06b2e80bded57362da5e944d4989cfbeff5a34d9e92c`  
		Last Modified: Sat, 28 Apr 2018 19:49:36 GMT  
		Size: 14.3 MB (14261060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5257a1a666582990768f9724f4b53651529a7198d15c2c70284e376f9e365fc`  
		Last Modified: Sat, 28 Apr 2018 19:49:31 GMT  
		Size: 1.1 MB (1061027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844834beb3da1adb73b111366e1d988bf785843ef6dcdc4cf78b8021d3a0dd9`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 4.4 KB (4444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9789d2bdad3cc0a62d7f4a94165126d09357ed4400a2ab0c35fbe826ab015913`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 480.6 KB (480568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f7bee8581e1a4d6199827368ca6b3d023321f5b7b21a0ea47fa32a6ff3704a`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66f12456a6efb1214356eee9bfa76ca82769adc9b49d02a47caf6e2b47f92ef`  
		Last Modified: Sun, 29 Apr 2018 01:15:58 GMT  
		Size: 32.2 MB (32236514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57116799470241dcd072b692a8dae3b6c7e724f9744322dc9559ca9fe6beef1`  
		Last Modified: Sun, 29 Apr 2018 01:15:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5807bc6fa4ae841660a2ec8fd7e26e4c87a9213ef1f5fd4fe6a04672864515b5`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d271f91b703a51f80600acec6050328a1dbf7db812a57c9912fe59f164773d`  
		Last Modified: Sun, 29 Apr 2018 01:15:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.12` - linux; ppc64le

```console
$ docker pull ghost@sha256:08d38e3b3f9814b6e9bbe1a386b0fd423b9dea01fae67028800f025f8c413ca0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119759777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205b4dc64f84c37e04b752b1d5d19d738a5f929ad54a6c2d3431af64672829cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 08:17:46 GMT
ADD file:6a4bd4ea54f669286e984ecf8178e1fa7c12c8b6fc0f96e4203ae7a6f99a2279 in / 
# Sat, 28 Apr 2018 08:17:47 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:49:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:49:27 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 16:06:30 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 16:07:44 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 16:07:46 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 16:07:54 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 16:07:55 GMT
CMD ["node"]
# Sat, 28 Apr 2018 20:31:41 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sat, 28 Apr 2018 20:31:41 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 20:31:46 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 20:31:46 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sat, 28 Apr 2018 20:31:47 GMT
WORKDIR /usr/src/ghost
# Sat, 28 Apr 2018 20:31:48 GMT
ENV GHOST_VERSION=0.11.12
# Sat, 28 Apr 2018 20:35:24 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sat, 28 Apr 2018 20:35:26 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sat, 28 Apr 2018 20:35:28 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sat, 28 Apr 2018 20:35:29 GMT
VOLUME [/var/lib/ghost]
# Sat, 28 Apr 2018 20:35:30 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sat, 28 Apr 2018 20:35:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Apr 2018 20:35:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 20:35:34 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 20:35:34 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:2668401c9f940b1d6b03e5f0086fa248cb957610ef9a7c79983d2fb0707ec76c`  
		Last Modified: Sat, 28 Apr 2018 08:24:36 GMT  
		Size: 53.4 MB (53392811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feb4c62e83f77f05ed3c1a72c453fce29bc8adee3ff31855937f28f0b9ad00`  
		Last Modified: Sat, 28 Apr 2018 10:38:43 GMT  
		Size: 17.6 MB (17571133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033729a6b8a78e4b13cad1f1d95e6f4ab8461fcb87c89fb4882c297de02fbad`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 4.4 KB (4438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd479c883acc5f45e3b06fe53ee3e824909480d7ee4035c57a3303a6058d3c1`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 117.7 KB (117651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5de8244112e4f1d6cb1f72cc7c9021d8f19e4df7a44412b636ab3b2dcc500d`  
		Last Modified: Sat, 28 Apr 2018 16:38:33 GMT  
		Size: 14.5 MB (14503944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbfc0285034d19463723dc2bed92d0074a197c39428886cf1bbe764a96829bd`  
		Last Modified: Sat, 28 Apr 2018 16:38:26 GMT  
		Size: 1.1 MB (1061054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1149a2cb4eee9745b4c094d6d21cb1b7411a26d289c2ab9839d5dab2d00eaf22`  
		Last Modified: Sat, 28 Apr 2018 20:37:34 GMT  
		Size: 4.5 KB (4493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f87c1d75b2e07f95919646be22128d325f057a34915b478b2f940c9b20808e9`  
		Last Modified: Sat, 28 Apr 2018 20:37:34 GMT  
		Size: 469.8 KB (469846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bbf03cfcfaf60d5ff4ae48c178a7ff5f35382ac3962117e89422aa3606686a`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81578de7958d44a57ae81f362eef0feb9e362238f9ca61497f65fd355aee63c1`  
		Last Modified: Sat, 28 Apr 2018 20:37:44 GMT  
		Size: 32.6 MB (32633242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7056e33db910d8b79c06696ebbccd1dd51d374520f243c0f4c666f2b045df606`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 253.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21990cf2afd673ea5b231448f84b60f8d598e43885f9d182e169d0367de91f9a`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd63678267ec2a032258767e669e61fe8a05f9dc2428d2a4c81881d75501d26`  
		Last Modified: Sat, 28 Apr 2018 20:37:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:0.11.12` - linux; s390x

```console
$ docker pull ghost@sha256:98fa686bd911133c39e8efbcfe692a60cc49baae272d21a5414e6766b1d89106
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121453913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9bd09623e7bc0e57e125ed427b7a7ff0ad310d0d9aab43a0e02d14b43dd608`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Sat, 28 Apr 2018 11:42:31 GMT
ADD file:ac1cfec75c7e1898f2c9b7d17653da3684fdda7d14440ce16f1939bb66105cdc in / 
# Sat, 28 Apr 2018 11:42:31 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 13:13:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:13:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:27:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 13:27:15 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 17:51:04 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 17:51:18 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 17:51:18 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 17:51:20 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 17:51:21 GMT
CMD ["node"]
# Sat, 28 Apr 2018 21:26:22 GMT
RUN groupadd user && useradd --create-home --home-dir /home/user -g user user
# Sat, 28 Apr 2018 21:26:23 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 21:26:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 21:26:28 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Sat, 28 Apr 2018 21:26:28 GMT
WORKDIR /usr/src/ghost
# Sat, 28 Apr 2018 21:26:29 GMT
ENV GHOST_VERSION=0.11.12
# Sat, 28 Apr 2018 21:28:27 GMT
RUN set -ex; 		buildDeps=' 		g++ 		gcc 		libc6-dev 		make 		python 		unzip 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apt-get purge -y --auto-remove $buildDeps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Sat, 28 Apr 2018 21:28:28 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Sat, 28 Apr 2018 21:28:29 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R user:user "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Sat, 28 Apr 2018 21:28:29 GMT
VOLUME [/var/lib/ghost]
# Sat, 28 Apr 2018 21:28:29 GMT
COPY file:9cace68ea99d0317c469464495249094669747893a60585016756f169051a609 in /usr/local/bin/ 
# Sat, 28 Apr 2018 21:28:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Apr 2018 21:28:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 21:28:30 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 21:28:30 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:e0524893a6d25f3e36c190fea678ecf1845e7c0d2ba833b077a429d64b943e0a`  
		Last Modified: Sat, 28 Apr 2018 11:47:52 GMT  
		Size: 54.5 MB (54465857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331cf8e884c1052e19f6b80b3efb54a7163ab49bf54c631bd861332c232029f`  
		Last Modified: Sat, 28 Apr 2018 13:29:06 GMT  
		Size: 17.8 MB (17767296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1573c40a4e9e40c7d5639586badca4c9ac2080488a599636910b77ac19a689`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd78e74bc99cbd7061122cf0fe9a054fb495f9bef7ef1502f65f98935d869fb`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 117.6 KB (117619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffe8a451803f5c963bc7fe27269ca01a9b6c131bcd1e034753682cd9a541d8`  
		Last Modified: Sat, 28 Apr 2018 17:57:39 GMT  
		Size: 14.9 MB (14874582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a235333140b41b4b113ac11697676cd325aeb3a46bcc9b1fd3e651dabb7cecd`  
		Last Modified: Sat, 28 Apr 2018 17:57:35 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a171f9a26483009feb5429cf10abcdbde3fdca46d40e5b14ccd68d79e207739`  
		Last Modified: Sat, 28 Apr 2018 21:29:51 GMT  
		Size: 4.5 KB (4458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6078238ec1d2a568460bf65cc9de23145d2c3e077602a1723d767ce08c12ea20`  
		Last Modified: Sat, 28 Apr 2018 21:29:50 GMT  
		Size: 486.8 KB (486820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2486b66854d7e889b03b37cb8eef2142f24b563db36acfbae10418c2ab42be8d`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a651b89b09b8a01ee8c66a42fcab842cd8aa39c725f36a23e46f6031ba0620fd`  
		Last Modified: Sat, 28 Apr 2018 21:30:00 GMT  
		Size: 32.7 MB (32670732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aec065995b11f80609e45643d443f1942a27e7289ad5405c86a71fd3c042687`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c34027c16b3ca4fbe8d26a43b559c708169acb574682e0cd9d4fb37e584a4`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c4596a07033948943bf374a7584778441fa39e2a0852553a64b49d1f2fe5a0`  
		Last Modified: Sat, 28 Apr 2018 21:29:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11.12-alpine`

```console
$ docker pull ghost@sha256:4fa70f29c72bc11997651612b9baf7e66120dac112ac5c6bcc5ab347641e2cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:0.11.12-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:142b57ac38c76ee3760720a834d1e55295fcc1a52564b303438064774948b892
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45530587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2511b28d2d2e4e56f43fc6235559aabe34667c2dd38f65f89ef4b6228a38a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 09 Jan 2018 21:12:40 GMT
ADD file:69848cb51056edaf120230b6f218a79968ac797295c2cef6728332e1801357be in / 
# Tue, 09 Jan 2018 21:12:40 GMT
CMD ["/bin/sh"]
# Tue, 03 Apr 2018 00:59:06 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:11:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Tue, 03 Apr 2018 01:11:15 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:11:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 03 Apr 2018 01:11:28 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:30:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 03 Apr 2018 03:53:06 GMT
RUN apk add --no-cache 		bash 		tar
# Tue, 03 Apr 2018 03:53:06 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 03:53:07 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 03:53:07 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 03:53:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gcc 		make 		openssl 		python 		unzip 	; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apk del .build-deps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 03:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 03:53:56 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R node:node "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 03:53:56 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 03:53:56 GMT
COPY file:2cb0a64ef22301242537372657c5d88304b43153f351a7f2d0d61e05c3dfb29a in /usr/local/bin/ 
# Tue, 03 Apr 2018 03:53:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 03:53:57 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 03:53:57 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:81033e7c1d6a5b44a94bb6b40033a6e589f50fd6b61578da6fc809e61f83898d`  
		Last Modified: Tue, 09 Jan 2018 21:15:04 GMT  
		Size: 2.4 MB (2387570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209940bfc9f474ff72013592d16fc0ac86f853491445f1bf606be599b1dbcb00`  
		Last Modified: Tue, 03 Apr 2018 02:24:08 GMT  
		Size: 15.5 MB (15474763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa77586de2de2644543aefeb4063f73eada8e9f8a796defd6f52b933113ab498`  
		Last Modified: Tue, 03 Apr 2018 02:24:03 GMT  
		Size: 1.1 MB (1067448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f63a91c1a5067bc9ab0a4de592d46c41d6362a6197ff98c476a68c48e2d293`  
		Last Modified: Tue, 03 Apr 2018 04:22:20 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa806e420b3f4337138119a7f674f698198814352899bc58ecd12a72a4dedb27`  
		Last Modified: Tue, 03 Apr 2018 04:31:04 GMT  
		Size: 1.4 MB (1360662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ac54dce8b93f24e75491c4272f400d3cd4c5a49ef8598cad9af537c474b46e`  
		Last Modified: Tue, 03 Apr 2018 04:31:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9947d6b44f7f8b74a50458ce981717104f601befdcc54e9faf95a634106b84be`  
		Last Modified: Tue, 03 Apr 2018 04:31:20 GMT  
		Size: 25.2 MB (25230816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf9d786cb58eb8f53375e4f0b6a4a9fc4b460e1de263e22b17317bff282b8ed`  
		Last Modified: Tue, 03 Apr 2018 04:31:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe80ff0a8bb25a5e9be14813af9a040056509b3a43f72e23deacc2ec014ff24`  
		Last Modified: Tue, 03 Apr 2018 04:31:02 GMT  
		Size: 606.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0.11-alpine`

```console
$ docker pull ghost@sha256:4fa70f29c72bc11997651612b9baf7e66120dac112ac5c6bcc5ab347641e2cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:0.11-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:142b57ac38c76ee3760720a834d1e55295fcc1a52564b303438064774948b892
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45530587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2511b28d2d2e4e56f43fc6235559aabe34667c2dd38f65f89ef4b6228a38a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 09 Jan 2018 21:12:40 GMT
ADD file:69848cb51056edaf120230b6f218a79968ac797295c2cef6728332e1801357be in / 
# Tue, 09 Jan 2018 21:12:40 GMT
CMD ["/bin/sh"]
# Tue, 03 Apr 2018 00:59:06 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:11:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Tue, 03 Apr 2018 01:11:15 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:11:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 03 Apr 2018 01:11:28 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:30:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 03 Apr 2018 03:53:06 GMT
RUN apk add --no-cache 		bash 		tar
# Tue, 03 Apr 2018 03:53:06 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 03:53:07 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 03:53:07 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 03:53:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gcc 		make 		openssl 		python 		unzip 	; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apk del .build-deps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 03:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 03:53:56 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R node:node "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 03:53:56 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 03:53:56 GMT
COPY file:2cb0a64ef22301242537372657c5d88304b43153f351a7f2d0d61e05c3dfb29a in /usr/local/bin/ 
# Tue, 03 Apr 2018 03:53:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 03:53:57 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 03:53:57 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:81033e7c1d6a5b44a94bb6b40033a6e589f50fd6b61578da6fc809e61f83898d`  
		Last Modified: Tue, 09 Jan 2018 21:15:04 GMT  
		Size: 2.4 MB (2387570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209940bfc9f474ff72013592d16fc0ac86f853491445f1bf606be599b1dbcb00`  
		Last Modified: Tue, 03 Apr 2018 02:24:08 GMT  
		Size: 15.5 MB (15474763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa77586de2de2644543aefeb4063f73eada8e9f8a796defd6f52b933113ab498`  
		Last Modified: Tue, 03 Apr 2018 02:24:03 GMT  
		Size: 1.1 MB (1067448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f63a91c1a5067bc9ab0a4de592d46c41d6362a6197ff98c476a68c48e2d293`  
		Last Modified: Tue, 03 Apr 2018 04:22:20 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa806e420b3f4337138119a7f674f698198814352899bc58ecd12a72a4dedb27`  
		Last Modified: Tue, 03 Apr 2018 04:31:04 GMT  
		Size: 1.4 MB (1360662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ac54dce8b93f24e75491c4272f400d3cd4c5a49ef8598cad9af537c474b46e`  
		Last Modified: Tue, 03 Apr 2018 04:31:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9947d6b44f7f8b74a50458ce981717104f601befdcc54e9faf95a634106b84be`  
		Last Modified: Tue, 03 Apr 2018 04:31:20 GMT  
		Size: 25.2 MB (25230816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf9d786cb58eb8f53375e4f0b6a4a9fc4b460e1de263e22b17317bff282b8ed`  
		Last Modified: Tue, 03 Apr 2018 04:31:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe80ff0a8bb25a5e9be14813af9a040056509b3a43f72e23deacc2ec014ff24`  
		Last Modified: Tue, 03 Apr 2018 04:31:02 GMT  
		Size: 606.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:0-alpine`

```console
$ docker pull ghost@sha256:4fa70f29c72bc11997651612b9baf7e66120dac112ac5c6bcc5ab347641e2cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:142b57ac38c76ee3760720a834d1e55295fcc1a52564b303438064774948b892
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45530587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2511b28d2d2e4e56f43fc6235559aabe34667c2dd38f65f89ef4b6228a38a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 09 Jan 2018 21:12:40 GMT
ADD file:69848cb51056edaf120230b6f218a79968ac797295c2cef6728332e1801357be in / 
# Tue, 09 Jan 2018 21:12:40 GMT
CMD ["/bin/sh"]
# Tue, 03 Apr 2018 00:59:06 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:11:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Tue, 03 Apr 2018 01:11:15 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:11:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 03 Apr 2018 01:11:28 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:30:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 03 Apr 2018 03:53:06 GMT
RUN apk add --no-cache 		bash 		tar
# Tue, 03 Apr 2018 03:53:06 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Tue, 03 Apr 2018 03:53:07 GMT
WORKDIR /usr/src/ghost
# Tue, 03 Apr 2018 03:53:07 GMT
ENV GHOST_VERSION=0.11.12
# Tue, 03 Apr 2018 03:53:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gcc 		make 		openssl 		python 		unzip 	; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apk del .build-deps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Tue, 03 Apr 2018 03:53:55 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Tue, 03 Apr 2018 03:53:56 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R node:node "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Tue, 03 Apr 2018 03:53:56 GMT
VOLUME [/var/lib/ghost]
# Tue, 03 Apr 2018 03:53:56 GMT
COPY file:2cb0a64ef22301242537372657c5d88304b43153f351a7f2d0d61e05c3dfb29a in /usr/local/bin/ 
# Tue, 03 Apr 2018 03:53:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Apr 2018 03:53:57 GMT
EXPOSE 2368/tcp
# Tue, 03 Apr 2018 03:53:57 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:81033e7c1d6a5b44a94bb6b40033a6e589f50fd6b61578da6fc809e61f83898d`  
		Last Modified: Tue, 09 Jan 2018 21:15:04 GMT  
		Size: 2.4 MB (2387570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209940bfc9f474ff72013592d16fc0ac86f853491445f1bf606be599b1dbcb00`  
		Last Modified: Tue, 03 Apr 2018 02:24:08 GMT  
		Size: 15.5 MB (15474763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa77586de2de2644543aefeb4063f73eada8e9f8a796defd6f52b933113ab498`  
		Last Modified: Tue, 03 Apr 2018 02:24:03 GMT  
		Size: 1.1 MB (1067448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f63a91c1a5067bc9ab0a4de592d46c41d6362a6197ff98c476a68c48e2d293`  
		Last Modified: Tue, 03 Apr 2018 04:22:20 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa806e420b3f4337138119a7f674f698198814352899bc58ecd12a72a4dedb27`  
		Last Modified: Tue, 03 Apr 2018 04:31:04 GMT  
		Size: 1.4 MB (1360662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ac54dce8b93f24e75491c4272f400d3cd4c5a49ef8598cad9af537c474b46e`  
		Last Modified: Tue, 03 Apr 2018 04:31:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9947d6b44f7f8b74a50458ce981717104f601befdcc54e9faf95a634106b84be`  
		Last Modified: Tue, 03 Apr 2018 04:31:20 GMT  
		Size: 25.2 MB (25230816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf9d786cb58eb8f53375e4f0b6a4a9fc4b460e1de263e22b17317bff282b8ed`  
		Last Modified: Tue, 03 Apr 2018 04:31:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe80ff0a8bb25a5e9be14813af9a040056509b3a43f72e23deacc2ec014ff24`  
		Last Modified: Tue, 03 Apr 2018 04:31:02 GMT  
		Size: 606.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1`

```console
$ docker pull ghost@sha256:718305e66b49acc4b3baa55f5168b0b15e7b7e711bb7bc0b3c022230802fa4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:1` - linux; amd64

```console
$ docker pull ghost@sha256:e40c4bcc7eb80cf7dbf70b5da7c55318de86fb87c0915cc9c257d398ac128db6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203864383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ae45da9a3820b25a40b776e08a494dc9c54ed52c21f3b6ef00317821830898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:03:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:03:53 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 01:31:24 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:31:50 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 01:31:51 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:31:55 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 01:31:55 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:16:20 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 03:16:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 03:16:26 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 00:58:56 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 00:59:18 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 00:59:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 00:59:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Apr 2018 22:20:44 GMT
ENV GHOST_VERSION=1.22.4
# Thu, 26 Apr 2018 22:21:41 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Thu, 26 Apr 2018 22:21:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Thu, 26 Apr 2018 22:21:57 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Thu, 26 Apr 2018 22:21:58 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Apr 2018 22:21:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Apr 2018 22:21:58 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Thu, 26 Apr 2018 22:21:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Apr 2018 22:21:59 GMT
EXPOSE 2368/tcp
# Thu, 26 Apr 2018 22:22:00 GMT
CMD ["node" "current/index.js"]
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
	-	`sha256:c669d5da499dfc3f959bff647d84aa109d42bd9dc4a84cd1736607a9a193931e`  
		Last Modified: Thu, 15 Mar 2018 05:16:20 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8ff4c87216eb5e2bdc5aeab7d50e312312df3b9358eac4f84cd10c0db8d7c`  
		Last Modified: Thu, 15 Mar 2018 05:16:18 GMT  
		Size: 117.6 KB (117624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d93f330ca2fc79c95fa142b121be257ae64491015b8997cd012096fbd113fb`  
		Last Modified: Tue, 03 Apr 2018 02:26:55 GMT  
		Size: 14.7 MB (14743833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5858a3ea9339b3a6db832ae2fbb00a02d8b6475f2af80f473668cd6e3f468e`  
		Last Modified: Tue, 03 Apr 2018 02:26:50 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b010a0bd596683d76af178e796e93e84e436e54c58dcc7ad9c45bc570397b991`  
		Last Modified: Tue, 03 Apr 2018 04:09:56 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7606873b40fac8eab3ac4b91312c121e6e805ae0e43240d3d8eab946e0017894`  
		Last Modified: Thu, 12 Apr 2018 01:35:39 GMT  
		Size: 16.2 MB (16182884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017a974e240a8939f895809f77d39022cae4b5948af764e43bdd2d3607be561d`  
		Last Modified: Thu, 26 Apr 2018 22:47:01 GMT  
		Size: 92.5 MB (92526922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408055898ca79d33a62bdc62b3c661f56ded6cc1ed390deec9dac794634fec4c`  
		Last Modified: Thu, 26 Apr 2018 22:46:27 GMT  
		Size: 6.9 MB (6851727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2d4b7c515fcfd6fac3c947eac8d79cfaf5dd0e6485adf1d1f1605862a8ea33`  
		Last Modified: Thu, 26 Apr 2018 22:46:26 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:365d6e3763e08cfd769c13f2740d28a4a4ed5a54ce122d0e27ffee79a35d85d6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204156200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fecd9bfe81d041879ca054db1a813e34f8ba550d90ce6b63ee3fc843d41b66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Mar 2018 17:24:26 GMT
ADD file:bcd41493879aaeeecb9c960b91c9954b1e0229e91b7a070cb6b2dfdadc8c52b8 in / 
# Wed, 14 Mar 2018 17:24:27 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 18:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:32:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:32:54 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 17:20:46 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 17:21:12 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 17:21:13 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 17:21:17 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 17:21:18 GMT
CMD ["node"]
# Tue, 03 Apr 2018 18:09:28 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 18:09:33 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 18:09:34 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 08:40:29 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 08:41:24 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 08:41:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 08:41:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 27 Apr 2018 09:14:12 GMT
ENV GHOST_VERSION=1.22.4
# Fri, 27 Apr 2018 09:15:57 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Fri, 27 Apr 2018 09:16:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Fri, 27 Apr 2018 09:20:18 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Fri, 27 Apr 2018 09:20:29 GMT
WORKDIR /var/lib/ghost
# Fri, 27 Apr 2018 09:20:30 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 27 Apr 2018 09:20:53 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Fri, 27 Apr 2018 09:20:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Apr 2018 09:20:54 GMT
EXPOSE 2368/tcp
# Fri, 27 Apr 2018 09:20:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21ccda36f02cc1214a990aa0c90bf9e705d50f6bf9844bffa71a8fbff898df30`  
		Last Modified: Wed, 14 Mar 2018 17:37:55 GMT  
		Size: 49.9 MB (49933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0a429742ffe0333a0070020d4aa3cfeaa1d0f87e652544b8b823ab168f1bd`  
		Last Modified: Wed, 14 Mar 2018 19:01:35 GMT  
		Size: 18.7 MB (18739890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63586fce2b79360f2899b20720f2e27aa341e7aadc0a15c96e68e3823f9704a7`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 4.4 KB (4414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc8c07863bd16bea098044bed1067f4cff1c67dcb8c2277e0ac929e47f7278`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 117.6 KB (117626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641f57e7df1914d159b6cc44e74272a61708d45911dd38659ed7a0bc8652cc0c`  
		Last Modified: Tue, 03 Apr 2018 17:44:50 GMT  
		Size: 14.7 MB (14726891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c99f90a2f0cf1c8de6b92bf7de39a380732bb3a57eb38e7f264cfaf03d55e68`  
		Last Modified: Tue, 03 Apr 2018 17:44:44 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dbd2b75e13cb287246e957f883f7fd160dbce4c9a09b16068447af044293e7`  
		Last Modified: Tue, 03 Apr 2018 18:22:31 GMT  
		Size: 468.7 KB (468695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea4b61c0d04f6207030b358953ed1e4e68e476a0507cf6eeb1631c3a3cca44`  
		Last Modified: Thu, 12 Apr 2018 08:49:33 GMT  
		Size: 16.2 MB (16184727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d7f6494548f90898a2d52bfd78e46701fbb3714ecc1ca975edcab447688d3e`  
		Last Modified: Fri, 27 Apr 2018 09:22:49 GMT  
		Size: 88.4 MB (88418844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab5dcc29fe315af7f8ef53411f43bbb652bcd0b92275277eba4067017856620`  
		Last Modified: Fri, 27 Apr 2018 09:22:15 GMT  
		Size: 14.5 MB (14500041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a11ab7a7ca0663ae27821e2c4c8cedec882e37fb388588153c4f20db1f01052`  
		Last Modified: Fri, 27 Apr 2018 09:22:10 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1` - linux; 386

```console
$ docker pull ghost@sha256:b3001b000c2743b8ff351324c20904ab969514e75e5f6df488a5f3d154e785ad
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209528850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce0f03200c6e6899adf222c7102400d24ba98f7e08f54abcebcee3ce26defc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 10:39:32 GMT
ADD file:ce5174f2b2c155a2421fac3ff37a02d9551d5d79e31a541189bcfd2416a6903a in / 
# Sat, 28 Apr 2018 10:39:32 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:05:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 19:37:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 19:37:46 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 19:40:46 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 19:41:22 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 19:41:23 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 19:41:26 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 19:41:26 GMT
CMD ["node"]
# Sun, 29 Apr 2018 01:04:49 GMT
ENV GOSU_VERSION=1.10
# Sun, 29 Apr 2018 01:04:54 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 29 Apr 2018 01:04:54 GMT
ENV NODE_ENV=production
# Sun, 29 Apr 2018 01:04:54 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sun, 29 Apr 2018 01:05:16 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sun, 29 Apr 2018 01:05:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 29 Apr 2018 01:05:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 29 Apr 2018 01:05:17 GMT
ENV GHOST_VERSION=1.22.4
# Sun, 29 Apr 2018 01:05:56 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sun, 29 Apr 2018 01:05:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sun, 29 Apr 2018 01:07:53 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sun, 29 Apr 2018 01:07:53 GMT
WORKDIR /var/lib/ghost
# Sun, 29 Apr 2018 01:07:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 29 Apr 2018 01:07:53 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sun, 29 Apr 2018 01:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 29 Apr 2018 01:07:54 GMT
EXPOSE 2368/tcp
# Sun, 29 Apr 2018 01:07:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:05b419d667f793c8c2edf0ff0aec14fc4d66733cdb89957ac89e8bfbeaddd0fa`  
		Last Modified: Sat, 28 Apr 2018 10:44:20 GMT  
		Size: 54.5 MB (54486782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b9c3b7ebe34e933c240e5eb7f8620732974e6e15e2c5d17cb91ca2aefffa4`  
		Last Modified: Sat, 28 Apr 2018 12:41:22 GMT  
		Size: 19.9 MB (19866118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618a70cca8b81e7f688c7591ffb047d440d878e7c088b564e9e8611c1157dba5`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 4.4 KB (4394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2b5615162ffa8552b2e45aa789d255d2331fa388ef168bf3115fe546951502`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 117.6 KB (117613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaed2e884f6af6104db06b2e80bded57362da5e944d4989cfbeff5a34d9e92c`  
		Last Modified: Sat, 28 Apr 2018 19:49:36 GMT  
		Size: 14.3 MB (14261060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5257a1a666582990768f9724f4b53651529a7198d15c2c70284e376f9e365fc`  
		Last Modified: Sat, 28 Apr 2018 19:49:31 GMT  
		Size: 1.1 MB (1061027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f8e5a06d23067ba52decc6561352f68a27347a09f11ee293c7a77d17cfdd21`  
		Last Modified: Sun, 29 Apr 2018 01:14:28 GMT  
		Size: 480.6 KB (480570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae231f09a834d53c6c0d553571b32a5fe50227c6ed7d0a1f3bfc940d12f8bab7`  
		Last Modified: Sun, 29 Apr 2018 01:14:47 GMT  
		Size: 16.3 MB (16257053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd380884828285357ffcb654be990d63b59cba21329d7b0e86bb84c392f380d`  
		Last Modified: Sun, 29 Apr 2018 01:15:22 GMT  
		Size: 88.4 MB (88416045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc216f41b9ef5303ebabc6dbb110ebc7888185cc3f13ee1a8aa785d0ef87c87`  
		Last Modified: Sun, 29 Apr 2018 01:14:33 GMT  
		Size: 14.6 MB (14577619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb69e16e51ae732ae305f11738095bd7425a0f0acd139d0fb9512903c5bed5b`  
		Last Modified: Sun, 29 Apr 2018 01:14:28 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1` - linux; ppc64le

```console
$ docker pull ghost@sha256:f56272ee3bec0ff565923fe3319939386bbe4848be8e233ccf5b4b7d1f87ddb2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206764570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2fc081e3183a1e5c400d2d8d3d5e1b26a9f841efce50d1afd6ce1a06b942f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 08:17:46 GMT
ADD file:6a4bd4ea54f669286e984ecf8178e1fa7c12c8b6fc0f96e4203ae7a6f99a2279 in / 
# Sat, 28 Apr 2018 08:17:47 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:49:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:49:27 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 16:06:30 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 16:07:44 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 16:07:46 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 16:07:54 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 16:07:55 GMT
CMD ["node"]
# Sat, 28 Apr 2018 20:25:42 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 20:25:47 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 20:25:51 GMT
ENV NODE_ENV=production
# Sat, 28 Apr 2018 20:25:52 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sat, 28 Apr 2018 20:26:21 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sat, 28 Apr 2018 20:26:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 28 Apr 2018 20:26:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 28 Apr 2018 20:26:26 GMT
ENV GHOST_VERSION=1.22.4
# Sat, 28 Apr 2018 20:27:39 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sat, 28 Apr 2018 20:27:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 28 Apr 2018 20:31:17 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sat, 28 Apr 2018 20:31:18 GMT
WORKDIR /var/lib/ghost
# Sat, 28 Apr 2018 20:31:19 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 28 Apr 2018 20:31:20 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 28 Apr 2018 20:31:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 20:31:22 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 20:31:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2668401c9f940b1d6b03e5f0086fa248cb957610ef9a7c79983d2fb0707ec76c`  
		Last Modified: Sat, 28 Apr 2018 08:24:36 GMT  
		Size: 53.4 MB (53392811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feb4c62e83f77f05ed3c1a72c453fce29bc8adee3ff31855937f28f0b9ad00`  
		Last Modified: Sat, 28 Apr 2018 10:38:43 GMT  
		Size: 17.6 MB (17571133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033729a6b8a78e4b13cad1f1d95e6f4ab8461fcb87c89fb4882c297de02fbad`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 4.4 KB (4438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd479c883acc5f45e3b06fe53ee3e824909480d7ee4035c57a3303a6058d3c1`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 117.7 KB (117651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5de8244112e4f1d6cb1f72cc7c9021d8f19e4df7a44412b636ab3b2dcc500d`  
		Last Modified: Sat, 28 Apr 2018 16:38:33 GMT  
		Size: 14.5 MB (14503944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbfc0285034d19463723dc2bed92d0074a197c39428886cf1bbe764a96829bd`  
		Last Modified: Sat, 28 Apr 2018 16:38:26 GMT  
		Size: 1.1 MB (1061054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106276b354e2e0c612a5a63f7f154018817cdf54431e5f43f5776c5e07ecbfeb`  
		Last Modified: Sat, 28 Apr 2018 20:35:58 GMT  
		Size: 469.8 KB (469843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874747483b33baf03454207a8496c6f1c13e7e1b2e2ed153e2ef152a446fc2c4`  
		Last Modified: Sat, 28 Apr 2018 20:36:04 GMT  
		Size: 16.3 MB (16257633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61761a09547322f759f585ad3a5e134158e4d86a38ca93bfeb01eebe4172601f`  
		Last Modified: Sat, 28 Apr 2018 20:36:24 GMT  
		Size: 88.4 MB (88416450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b047143f9c8053ed1d51a6cb0ba106e4b5eb48804b0361be72bdba4a2b2f49c1`  
		Last Modified: Sat, 28 Apr 2018 20:36:02 GMT  
		Size: 15.0 MB (14969044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5cdc26a555aab106ec7f00ffedbc2a1d5bd8a34ef6cb46ae3d485f3c63cdad`  
		Last Modified: Sat, 28 Apr 2018 20:35:58 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1` - linux; s390x

```console
$ docker pull ghost@sha256:81f5f3c0951fad3eaf4783cfb506783cb58e4cb0b883bc1e12f276bc4e2bb63b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208458660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc7a15740f7dda893e38d7a798724139b63760ada2f2d7281fab8a109b9f9ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 11:42:31 GMT
ADD file:ac1cfec75c7e1898f2c9b7d17653da3684fdda7d14440ce16f1939bb66105cdc in / 
# Sat, 28 Apr 2018 11:42:31 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 13:13:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:13:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:27:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 13:27:15 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 17:51:04 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 17:51:18 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 17:51:18 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 17:51:20 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 17:51:21 GMT
CMD ["node"]
# Sat, 28 Apr 2018 21:23:28 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 21:23:31 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 21:23:31 GMT
ENV NODE_ENV=production
# Sat, 28 Apr 2018 21:23:31 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sat, 28 Apr 2018 21:23:58 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_VERSION=1.22.4
# Sat, 28 Apr 2018 21:24:34 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sat, 28 Apr 2018 21:24:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 28 Apr 2018 21:26:09 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sat, 28 Apr 2018 21:26:09 GMT
WORKDIR /var/lib/ghost
# Sat, 28 Apr 2018 21:26:09 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 28 Apr 2018 21:26:09 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 28 Apr 2018 21:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 21:26:10 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 21:26:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e0524893a6d25f3e36c190fea678ecf1845e7c0d2ba833b077a429d64b943e0a`  
		Last Modified: Sat, 28 Apr 2018 11:47:52 GMT  
		Size: 54.5 MB (54465857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331cf8e884c1052e19f6b80b3efb54a7163ab49bf54c631bd861332c232029f`  
		Last Modified: Sat, 28 Apr 2018 13:29:06 GMT  
		Size: 17.8 MB (17767296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1573c40a4e9e40c7d5639586badca4c9ac2080488a599636910b77ac19a689`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd78e74bc99cbd7061122cf0fe9a054fb495f9bef7ef1502f65f98935d869fb`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 117.6 KB (117619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffe8a451803f5c963bc7fe27269ca01a9b6c131bcd1e034753682cd9a541d8`  
		Last Modified: Sat, 28 Apr 2018 17:57:39 GMT  
		Size: 14.9 MB (14874582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a235333140b41b4b113ac11697676cd325aeb3a46bcc9b1fd3e651dabb7cecd`  
		Last Modified: Sat, 28 Apr 2018 17:57:35 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f537d58daec665e17610dcf1d6af3558ca76a008f6a2fdadf737f9325c7d3082`  
		Last Modified: Sat, 28 Apr 2018 21:28:52 GMT  
		Size: 486.8 KB (486818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a074f20bae5534585e5d7a6fe7d254e379da438972f46189a6a5875a54f57985`  
		Last Modified: Sat, 28 Apr 2018 21:28:57 GMT  
		Size: 16.3 MB (16257593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51badbc99b7366403d7cb169dcb78e5028627a527199373496307783407df534`  
		Last Modified: Sat, 28 Apr 2018 21:29:11 GMT  
		Size: 88.4 MB (88415393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f4480bd6e9f5b63057a66c4282d12c8100f94d143cb2d862714b3f2ac2936b`  
		Last Modified: Sat, 28 Apr 2018 21:28:55 GMT  
		Size: 15.0 MB (15007486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec20f88c0d9020e097835ab6d067f49ddeb0f0cc23f833f2285b91b22eed9e1`  
		Last Modified: Sat, 28 Apr 2018 21:28:51 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1.22`

```console
$ docker pull ghost@sha256:718305e66b49acc4b3baa55f5168b0b15e7b7e711bb7bc0b3c022230802fa4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:1.22` - linux; amd64

```console
$ docker pull ghost@sha256:e40c4bcc7eb80cf7dbf70b5da7c55318de86fb87c0915cc9c257d398ac128db6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203864383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ae45da9a3820b25a40b776e08a494dc9c54ed52c21f3b6ef00317821830898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:03:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:03:53 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 01:31:24 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:31:50 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 01:31:51 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:31:55 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 01:31:55 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:16:20 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 03:16:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 03:16:26 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 00:58:56 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 00:59:18 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 00:59:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 00:59:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Apr 2018 22:20:44 GMT
ENV GHOST_VERSION=1.22.4
# Thu, 26 Apr 2018 22:21:41 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Thu, 26 Apr 2018 22:21:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Thu, 26 Apr 2018 22:21:57 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Thu, 26 Apr 2018 22:21:58 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Apr 2018 22:21:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Apr 2018 22:21:58 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Thu, 26 Apr 2018 22:21:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Apr 2018 22:21:59 GMT
EXPOSE 2368/tcp
# Thu, 26 Apr 2018 22:22:00 GMT
CMD ["node" "current/index.js"]
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
	-	`sha256:c669d5da499dfc3f959bff647d84aa109d42bd9dc4a84cd1736607a9a193931e`  
		Last Modified: Thu, 15 Mar 2018 05:16:20 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8ff4c87216eb5e2bdc5aeab7d50e312312df3b9358eac4f84cd10c0db8d7c`  
		Last Modified: Thu, 15 Mar 2018 05:16:18 GMT  
		Size: 117.6 KB (117624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d93f330ca2fc79c95fa142b121be257ae64491015b8997cd012096fbd113fb`  
		Last Modified: Tue, 03 Apr 2018 02:26:55 GMT  
		Size: 14.7 MB (14743833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5858a3ea9339b3a6db832ae2fbb00a02d8b6475f2af80f473668cd6e3f468e`  
		Last Modified: Tue, 03 Apr 2018 02:26:50 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b010a0bd596683d76af178e796e93e84e436e54c58dcc7ad9c45bc570397b991`  
		Last Modified: Tue, 03 Apr 2018 04:09:56 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7606873b40fac8eab3ac4b91312c121e6e805ae0e43240d3d8eab946e0017894`  
		Last Modified: Thu, 12 Apr 2018 01:35:39 GMT  
		Size: 16.2 MB (16182884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017a974e240a8939f895809f77d39022cae4b5948af764e43bdd2d3607be561d`  
		Last Modified: Thu, 26 Apr 2018 22:47:01 GMT  
		Size: 92.5 MB (92526922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408055898ca79d33a62bdc62b3c661f56ded6cc1ed390deec9dac794634fec4c`  
		Last Modified: Thu, 26 Apr 2018 22:46:27 GMT  
		Size: 6.9 MB (6851727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2d4b7c515fcfd6fac3c947eac8d79cfaf5dd0e6485adf1d1f1605862a8ea33`  
		Last Modified: Thu, 26 Apr 2018 22:46:26 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.22` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:365d6e3763e08cfd769c13f2740d28a4a4ed5a54ce122d0e27ffee79a35d85d6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204156200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fecd9bfe81d041879ca054db1a813e34f8ba550d90ce6b63ee3fc843d41b66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Mar 2018 17:24:26 GMT
ADD file:bcd41493879aaeeecb9c960b91c9954b1e0229e91b7a070cb6b2dfdadc8c52b8 in / 
# Wed, 14 Mar 2018 17:24:27 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 18:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:32:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:32:54 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 17:20:46 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 17:21:12 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 17:21:13 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 17:21:17 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 17:21:18 GMT
CMD ["node"]
# Tue, 03 Apr 2018 18:09:28 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 18:09:33 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 18:09:34 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 08:40:29 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 08:41:24 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 08:41:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 08:41:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 27 Apr 2018 09:14:12 GMT
ENV GHOST_VERSION=1.22.4
# Fri, 27 Apr 2018 09:15:57 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Fri, 27 Apr 2018 09:16:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Fri, 27 Apr 2018 09:20:18 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Fri, 27 Apr 2018 09:20:29 GMT
WORKDIR /var/lib/ghost
# Fri, 27 Apr 2018 09:20:30 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 27 Apr 2018 09:20:53 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Fri, 27 Apr 2018 09:20:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Apr 2018 09:20:54 GMT
EXPOSE 2368/tcp
# Fri, 27 Apr 2018 09:20:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21ccda36f02cc1214a990aa0c90bf9e705d50f6bf9844bffa71a8fbff898df30`  
		Last Modified: Wed, 14 Mar 2018 17:37:55 GMT  
		Size: 49.9 MB (49933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0a429742ffe0333a0070020d4aa3cfeaa1d0f87e652544b8b823ab168f1bd`  
		Last Modified: Wed, 14 Mar 2018 19:01:35 GMT  
		Size: 18.7 MB (18739890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63586fce2b79360f2899b20720f2e27aa341e7aadc0a15c96e68e3823f9704a7`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 4.4 KB (4414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc8c07863bd16bea098044bed1067f4cff1c67dcb8c2277e0ac929e47f7278`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 117.6 KB (117626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641f57e7df1914d159b6cc44e74272a61708d45911dd38659ed7a0bc8652cc0c`  
		Last Modified: Tue, 03 Apr 2018 17:44:50 GMT  
		Size: 14.7 MB (14726891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c99f90a2f0cf1c8de6b92bf7de39a380732bb3a57eb38e7f264cfaf03d55e68`  
		Last Modified: Tue, 03 Apr 2018 17:44:44 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dbd2b75e13cb287246e957f883f7fd160dbce4c9a09b16068447af044293e7`  
		Last Modified: Tue, 03 Apr 2018 18:22:31 GMT  
		Size: 468.7 KB (468695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea4b61c0d04f6207030b358953ed1e4e68e476a0507cf6eeb1631c3a3cca44`  
		Last Modified: Thu, 12 Apr 2018 08:49:33 GMT  
		Size: 16.2 MB (16184727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d7f6494548f90898a2d52bfd78e46701fbb3714ecc1ca975edcab447688d3e`  
		Last Modified: Fri, 27 Apr 2018 09:22:49 GMT  
		Size: 88.4 MB (88418844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab5dcc29fe315af7f8ef53411f43bbb652bcd0b92275277eba4067017856620`  
		Last Modified: Fri, 27 Apr 2018 09:22:15 GMT  
		Size: 14.5 MB (14500041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a11ab7a7ca0663ae27821e2c4c8cedec882e37fb388588153c4f20db1f01052`  
		Last Modified: Fri, 27 Apr 2018 09:22:10 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.22` - linux; 386

```console
$ docker pull ghost@sha256:b3001b000c2743b8ff351324c20904ab969514e75e5f6df488a5f3d154e785ad
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209528850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce0f03200c6e6899adf222c7102400d24ba98f7e08f54abcebcee3ce26defc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 10:39:32 GMT
ADD file:ce5174f2b2c155a2421fac3ff37a02d9551d5d79e31a541189bcfd2416a6903a in / 
# Sat, 28 Apr 2018 10:39:32 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:05:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 19:37:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 19:37:46 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 19:40:46 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 19:41:22 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 19:41:23 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 19:41:26 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 19:41:26 GMT
CMD ["node"]
# Sun, 29 Apr 2018 01:04:49 GMT
ENV GOSU_VERSION=1.10
# Sun, 29 Apr 2018 01:04:54 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 29 Apr 2018 01:04:54 GMT
ENV NODE_ENV=production
# Sun, 29 Apr 2018 01:04:54 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sun, 29 Apr 2018 01:05:16 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sun, 29 Apr 2018 01:05:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 29 Apr 2018 01:05:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 29 Apr 2018 01:05:17 GMT
ENV GHOST_VERSION=1.22.4
# Sun, 29 Apr 2018 01:05:56 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sun, 29 Apr 2018 01:05:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sun, 29 Apr 2018 01:07:53 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sun, 29 Apr 2018 01:07:53 GMT
WORKDIR /var/lib/ghost
# Sun, 29 Apr 2018 01:07:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 29 Apr 2018 01:07:53 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sun, 29 Apr 2018 01:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 29 Apr 2018 01:07:54 GMT
EXPOSE 2368/tcp
# Sun, 29 Apr 2018 01:07:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:05b419d667f793c8c2edf0ff0aec14fc4d66733cdb89957ac89e8bfbeaddd0fa`  
		Last Modified: Sat, 28 Apr 2018 10:44:20 GMT  
		Size: 54.5 MB (54486782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b9c3b7ebe34e933c240e5eb7f8620732974e6e15e2c5d17cb91ca2aefffa4`  
		Last Modified: Sat, 28 Apr 2018 12:41:22 GMT  
		Size: 19.9 MB (19866118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618a70cca8b81e7f688c7591ffb047d440d878e7c088b564e9e8611c1157dba5`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 4.4 KB (4394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2b5615162ffa8552b2e45aa789d255d2331fa388ef168bf3115fe546951502`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 117.6 KB (117613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaed2e884f6af6104db06b2e80bded57362da5e944d4989cfbeff5a34d9e92c`  
		Last Modified: Sat, 28 Apr 2018 19:49:36 GMT  
		Size: 14.3 MB (14261060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5257a1a666582990768f9724f4b53651529a7198d15c2c70284e376f9e365fc`  
		Last Modified: Sat, 28 Apr 2018 19:49:31 GMT  
		Size: 1.1 MB (1061027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f8e5a06d23067ba52decc6561352f68a27347a09f11ee293c7a77d17cfdd21`  
		Last Modified: Sun, 29 Apr 2018 01:14:28 GMT  
		Size: 480.6 KB (480570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae231f09a834d53c6c0d553571b32a5fe50227c6ed7d0a1f3bfc940d12f8bab7`  
		Last Modified: Sun, 29 Apr 2018 01:14:47 GMT  
		Size: 16.3 MB (16257053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd380884828285357ffcb654be990d63b59cba21329d7b0e86bb84c392f380d`  
		Last Modified: Sun, 29 Apr 2018 01:15:22 GMT  
		Size: 88.4 MB (88416045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc216f41b9ef5303ebabc6dbb110ebc7888185cc3f13ee1a8aa785d0ef87c87`  
		Last Modified: Sun, 29 Apr 2018 01:14:33 GMT  
		Size: 14.6 MB (14577619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb69e16e51ae732ae305f11738095bd7425a0f0acd139d0fb9512903c5bed5b`  
		Last Modified: Sun, 29 Apr 2018 01:14:28 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.22` - linux; ppc64le

```console
$ docker pull ghost@sha256:f56272ee3bec0ff565923fe3319939386bbe4848be8e233ccf5b4b7d1f87ddb2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206764570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2fc081e3183a1e5c400d2d8d3d5e1b26a9f841efce50d1afd6ce1a06b942f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 08:17:46 GMT
ADD file:6a4bd4ea54f669286e984ecf8178e1fa7c12c8b6fc0f96e4203ae7a6f99a2279 in / 
# Sat, 28 Apr 2018 08:17:47 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:49:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:49:27 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 16:06:30 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 16:07:44 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 16:07:46 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 16:07:54 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 16:07:55 GMT
CMD ["node"]
# Sat, 28 Apr 2018 20:25:42 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 20:25:47 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 20:25:51 GMT
ENV NODE_ENV=production
# Sat, 28 Apr 2018 20:25:52 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sat, 28 Apr 2018 20:26:21 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sat, 28 Apr 2018 20:26:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 28 Apr 2018 20:26:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 28 Apr 2018 20:26:26 GMT
ENV GHOST_VERSION=1.22.4
# Sat, 28 Apr 2018 20:27:39 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sat, 28 Apr 2018 20:27:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 28 Apr 2018 20:31:17 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sat, 28 Apr 2018 20:31:18 GMT
WORKDIR /var/lib/ghost
# Sat, 28 Apr 2018 20:31:19 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 28 Apr 2018 20:31:20 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 28 Apr 2018 20:31:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 20:31:22 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 20:31:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2668401c9f940b1d6b03e5f0086fa248cb957610ef9a7c79983d2fb0707ec76c`  
		Last Modified: Sat, 28 Apr 2018 08:24:36 GMT  
		Size: 53.4 MB (53392811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feb4c62e83f77f05ed3c1a72c453fce29bc8adee3ff31855937f28f0b9ad00`  
		Last Modified: Sat, 28 Apr 2018 10:38:43 GMT  
		Size: 17.6 MB (17571133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033729a6b8a78e4b13cad1f1d95e6f4ab8461fcb87c89fb4882c297de02fbad`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 4.4 KB (4438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd479c883acc5f45e3b06fe53ee3e824909480d7ee4035c57a3303a6058d3c1`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 117.7 KB (117651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5de8244112e4f1d6cb1f72cc7c9021d8f19e4df7a44412b636ab3b2dcc500d`  
		Last Modified: Sat, 28 Apr 2018 16:38:33 GMT  
		Size: 14.5 MB (14503944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbfc0285034d19463723dc2bed92d0074a197c39428886cf1bbe764a96829bd`  
		Last Modified: Sat, 28 Apr 2018 16:38:26 GMT  
		Size: 1.1 MB (1061054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106276b354e2e0c612a5a63f7f154018817cdf54431e5f43f5776c5e07ecbfeb`  
		Last Modified: Sat, 28 Apr 2018 20:35:58 GMT  
		Size: 469.8 KB (469843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874747483b33baf03454207a8496c6f1c13e7e1b2e2ed153e2ef152a446fc2c4`  
		Last Modified: Sat, 28 Apr 2018 20:36:04 GMT  
		Size: 16.3 MB (16257633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61761a09547322f759f585ad3a5e134158e4d86a38ca93bfeb01eebe4172601f`  
		Last Modified: Sat, 28 Apr 2018 20:36:24 GMT  
		Size: 88.4 MB (88416450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b047143f9c8053ed1d51a6cb0ba106e4b5eb48804b0361be72bdba4a2b2f49c1`  
		Last Modified: Sat, 28 Apr 2018 20:36:02 GMT  
		Size: 15.0 MB (14969044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5cdc26a555aab106ec7f00ffedbc2a1d5bd8a34ef6cb46ae3d485f3c63cdad`  
		Last Modified: Sat, 28 Apr 2018 20:35:58 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.22` - linux; s390x

```console
$ docker pull ghost@sha256:81f5f3c0951fad3eaf4783cfb506783cb58e4cb0b883bc1e12f276bc4e2bb63b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208458660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc7a15740f7dda893e38d7a798724139b63760ada2f2d7281fab8a109b9f9ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 11:42:31 GMT
ADD file:ac1cfec75c7e1898f2c9b7d17653da3684fdda7d14440ce16f1939bb66105cdc in / 
# Sat, 28 Apr 2018 11:42:31 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 13:13:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:13:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:27:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 13:27:15 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 17:51:04 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 17:51:18 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 17:51:18 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 17:51:20 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 17:51:21 GMT
CMD ["node"]
# Sat, 28 Apr 2018 21:23:28 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 21:23:31 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 21:23:31 GMT
ENV NODE_ENV=production
# Sat, 28 Apr 2018 21:23:31 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sat, 28 Apr 2018 21:23:58 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_VERSION=1.22.4
# Sat, 28 Apr 2018 21:24:34 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sat, 28 Apr 2018 21:24:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 28 Apr 2018 21:26:09 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sat, 28 Apr 2018 21:26:09 GMT
WORKDIR /var/lib/ghost
# Sat, 28 Apr 2018 21:26:09 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 28 Apr 2018 21:26:09 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 28 Apr 2018 21:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 21:26:10 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 21:26:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e0524893a6d25f3e36c190fea678ecf1845e7c0d2ba833b077a429d64b943e0a`  
		Last Modified: Sat, 28 Apr 2018 11:47:52 GMT  
		Size: 54.5 MB (54465857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331cf8e884c1052e19f6b80b3efb54a7163ab49bf54c631bd861332c232029f`  
		Last Modified: Sat, 28 Apr 2018 13:29:06 GMT  
		Size: 17.8 MB (17767296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1573c40a4e9e40c7d5639586badca4c9ac2080488a599636910b77ac19a689`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd78e74bc99cbd7061122cf0fe9a054fb495f9bef7ef1502f65f98935d869fb`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 117.6 KB (117619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffe8a451803f5c963bc7fe27269ca01a9b6c131bcd1e034753682cd9a541d8`  
		Last Modified: Sat, 28 Apr 2018 17:57:39 GMT  
		Size: 14.9 MB (14874582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a235333140b41b4b113ac11697676cd325aeb3a46bcc9b1fd3e651dabb7cecd`  
		Last Modified: Sat, 28 Apr 2018 17:57:35 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f537d58daec665e17610dcf1d6af3558ca76a008f6a2fdadf737f9325c7d3082`  
		Last Modified: Sat, 28 Apr 2018 21:28:52 GMT  
		Size: 486.8 KB (486818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a074f20bae5534585e5d7a6fe7d254e379da438972f46189a6a5875a54f57985`  
		Last Modified: Sat, 28 Apr 2018 21:28:57 GMT  
		Size: 16.3 MB (16257593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51badbc99b7366403d7cb169dcb78e5028627a527199373496307783407df534`  
		Last Modified: Sat, 28 Apr 2018 21:29:11 GMT  
		Size: 88.4 MB (88415393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f4480bd6e9f5b63057a66c4282d12c8100f94d143cb2d862714b3f2ac2936b`  
		Last Modified: Sat, 28 Apr 2018 21:28:55 GMT  
		Size: 15.0 MB (15007486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec20f88c0d9020e097835ab6d067f49ddeb0f0cc23f833f2285b91b22eed9e1`  
		Last Modified: Sat, 28 Apr 2018 21:28:51 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1.22.4`

```console
$ docker pull ghost@sha256:718305e66b49acc4b3baa55f5168b0b15e7b7e711bb7bc0b3c022230802fa4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:1.22.4` - linux; amd64

```console
$ docker pull ghost@sha256:e40c4bcc7eb80cf7dbf70b5da7c55318de86fb87c0915cc9c257d398ac128db6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203864383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ae45da9a3820b25a40b776e08a494dc9c54ed52c21f3b6ef00317821830898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:03:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:03:53 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 01:31:24 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:31:50 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 01:31:51 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:31:55 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 01:31:55 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:16:20 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 03:16:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 03:16:26 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 00:58:56 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 00:59:18 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 00:59:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 00:59:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Apr 2018 22:20:44 GMT
ENV GHOST_VERSION=1.22.4
# Thu, 26 Apr 2018 22:21:41 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Thu, 26 Apr 2018 22:21:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Thu, 26 Apr 2018 22:21:57 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Thu, 26 Apr 2018 22:21:58 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Apr 2018 22:21:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Apr 2018 22:21:58 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Thu, 26 Apr 2018 22:21:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Apr 2018 22:21:59 GMT
EXPOSE 2368/tcp
# Thu, 26 Apr 2018 22:22:00 GMT
CMD ["node" "current/index.js"]
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
	-	`sha256:c669d5da499dfc3f959bff647d84aa109d42bd9dc4a84cd1736607a9a193931e`  
		Last Modified: Thu, 15 Mar 2018 05:16:20 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8ff4c87216eb5e2bdc5aeab7d50e312312df3b9358eac4f84cd10c0db8d7c`  
		Last Modified: Thu, 15 Mar 2018 05:16:18 GMT  
		Size: 117.6 KB (117624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d93f330ca2fc79c95fa142b121be257ae64491015b8997cd012096fbd113fb`  
		Last Modified: Tue, 03 Apr 2018 02:26:55 GMT  
		Size: 14.7 MB (14743833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5858a3ea9339b3a6db832ae2fbb00a02d8b6475f2af80f473668cd6e3f468e`  
		Last Modified: Tue, 03 Apr 2018 02:26:50 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b010a0bd596683d76af178e796e93e84e436e54c58dcc7ad9c45bc570397b991`  
		Last Modified: Tue, 03 Apr 2018 04:09:56 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7606873b40fac8eab3ac4b91312c121e6e805ae0e43240d3d8eab946e0017894`  
		Last Modified: Thu, 12 Apr 2018 01:35:39 GMT  
		Size: 16.2 MB (16182884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017a974e240a8939f895809f77d39022cae4b5948af764e43bdd2d3607be561d`  
		Last Modified: Thu, 26 Apr 2018 22:47:01 GMT  
		Size: 92.5 MB (92526922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408055898ca79d33a62bdc62b3c661f56ded6cc1ed390deec9dac794634fec4c`  
		Last Modified: Thu, 26 Apr 2018 22:46:27 GMT  
		Size: 6.9 MB (6851727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2d4b7c515fcfd6fac3c947eac8d79cfaf5dd0e6485adf1d1f1605862a8ea33`  
		Last Modified: Thu, 26 Apr 2018 22:46:26 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.22.4` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:365d6e3763e08cfd769c13f2740d28a4a4ed5a54ce122d0e27ffee79a35d85d6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204156200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fecd9bfe81d041879ca054db1a813e34f8ba550d90ce6b63ee3fc843d41b66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Mar 2018 17:24:26 GMT
ADD file:bcd41493879aaeeecb9c960b91c9954b1e0229e91b7a070cb6b2dfdadc8c52b8 in / 
# Wed, 14 Mar 2018 17:24:27 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 18:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:32:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:32:54 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 17:20:46 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 17:21:12 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 17:21:13 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 17:21:17 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 17:21:18 GMT
CMD ["node"]
# Tue, 03 Apr 2018 18:09:28 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 18:09:33 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 18:09:34 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 08:40:29 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 08:41:24 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 08:41:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 08:41:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 27 Apr 2018 09:14:12 GMT
ENV GHOST_VERSION=1.22.4
# Fri, 27 Apr 2018 09:15:57 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Fri, 27 Apr 2018 09:16:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Fri, 27 Apr 2018 09:20:18 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Fri, 27 Apr 2018 09:20:29 GMT
WORKDIR /var/lib/ghost
# Fri, 27 Apr 2018 09:20:30 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 27 Apr 2018 09:20:53 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Fri, 27 Apr 2018 09:20:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Apr 2018 09:20:54 GMT
EXPOSE 2368/tcp
# Fri, 27 Apr 2018 09:20:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21ccda36f02cc1214a990aa0c90bf9e705d50f6bf9844bffa71a8fbff898df30`  
		Last Modified: Wed, 14 Mar 2018 17:37:55 GMT  
		Size: 49.9 MB (49933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0a429742ffe0333a0070020d4aa3cfeaa1d0f87e652544b8b823ab168f1bd`  
		Last Modified: Wed, 14 Mar 2018 19:01:35 GMT  
		Size: 18.7 MB (18739890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63586fce2b79360f2899b20720f2e27aa341e7aadc0a15c96e68e3823f9704a7`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 4.4 KB (4414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc8c07863bd16bea098044bed1067f4cff1c67dcb8c2277e0ac929e47f7278`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 117.6 KB (117626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641f57e7df1914d159b6cc44e74272a61708d45911dd38659ed7a0bc8652cc0c`  
		Last Modified: Tue, 03 Apr 2018 17:44:50 GMT  
		Size: 14.7 MB (14726891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c99f90a2f0cf1c8de6b92bf7de39a380732bb3a57eb38e7f264cfaf03d55e68`  
		Last Modified: Tue, 03 Apr 2018 17:44:44 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dbd2b75e13cb287246e957f883f7fd160dbce4c9a09b16068447af044293e7`  
		Last Modified: Tue, 03 Apr 2018 18:22:31 GMT  
		Size: 468.7 KB (468695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea4b61c0d04f6207030b358953ed1e4e68e476a0507cf6eeb1631c3a3cca44`  
		Last Modified: Thu, 12 Apr 2018 08:49:33 GMT  
		Size: 16.2 MB (16184727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d7f6494548f90898a2d52bfd78e46701fbb3714ecc1ca975edcab447688d3e`  
		Last Modified: Fri, 27 Apr 2018 09:22:49 GMT  
		Size: 88.4 MB (88418844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab5dcc29fe315af7f8ef53411f43bbb652bcd0b92275277eba4067017856620`  
		Last Modified: Fri, 27 Apr 2018 09:22:15 GMT  
		Size: 14.5 MB (14500041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a11ab7a7ca0663ae27821e2c4c8cedec882e37fb388588153c4f20db1f01052`  
		Last Modified: Fri, 27 Apr 2018 09:22:10 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.22.4` - linux; 386

```console
$ docker pull ghost@sha256:b3001b000c2743b8ff351324c20904ab969514e75e5f6df488a5f3d154e785ad
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209528850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce0f03200c6e6899adf222c7102400d24ba98f7e08f54abcebcee3ce26defc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 10:39:32 GMT
ADD file:ce5174f2b2c155a2421fac3ff37a02d9551d5d79e31a541189bcfd2416a6903a in / 
# Sat, 28 Apr 2018 10:39:32 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:05:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 19:37:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 19:37:46 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 19:40:46 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 19:41:22 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 19:41:23 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 19:41:26 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 19:41:26 GMT
CMD ["node"]
# Sun, 29 Apr 2018 01:04:49 GMT
ENV GOSU_VERSION=1.10
# Sun, 29 Apr 2018 01:04:54 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 29 Apr 2018 01:04:54 GMT
ENV NODE_ENV=production
# Sun, 29 Apr 2018 01:04:54 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sun, 29 Apr 2018 01:05:16 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sun, 29 Apr 2018 01:05:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 29 Apr 2018 01:05:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 29 Apr 2018 01:05:17 GMT
ENV GHOST_VERSION=1.22.4
# Sun, 29 Apr 2018 01:05:56 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sun, 29 Apr 2018 01:05:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sun, 29 Apr 2018 01:07:53 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sun, 29 Apr 2018 01:07:53 GMT
WORKDIR /var/lib/ghost
# Sun, 29 Apr 2018 01:07:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 29 Apr 2018 01:07:53 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sun, 29 Apr 2018 01:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 29 Apr 2018 01:07:54 GMT
EXPOSE 2368/tcp
# Sun, 29 Apr 2018 01:07:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:05b419d667f793c8c2edf0ff0aec14fc4d66733cdb89957ac89e8bfbeaddd0fa`  
		Last Modified: Sat, 28 Apr 2018 10:44:20 GMT  
		Size: 54.5 MB (54486782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b9c3b7ebe34e933c240e5eb7f8620732974e6e15e2c5d17cb91ca2aefffa4`  
		Last Modified: Sat, 28 Apr 2018 12:41:22 GMT  
		Size: 19.9 MB (19866118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618a70cca8b81e7f688c7591ffb047d440d878e7c088b564e9e8611c1157dba5`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 4.4 KB (4394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2b5615162ffa8552b2e45aa789d255d2331fa388ef168bf3115fe546951502`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 117.6 KB (117613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaed2e884f6af6104db06b2e80bded57362da5e944d4989cfbeff5a34d9e92c`  
		Last Modified: Sat, 28 Apr 2018 19:49:36 GMT  
		Size: 14.3 MB (14261060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5257a1a666582990768f9724f4b53651529a7198d15c2c70284e376f9e365fc`  
		Last Modified: Sat, 28 Apr 2018 19:49:31 GMT  
		Size: 1.1 MB (1061027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f8e5a06d23067ba52decc6561352f68a27347a09f11ee293c7a77d17cfdd21`  
		Last Modified: Sun, 29 Apr 2018 01:14:28 GMT  
		Size: 480.6 KB (480570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae231f09a834d53c6c0d553571b32a5fe50227c6ed7d0a1f3bfc940d12f8bab7`  
		Last Modified: Sun, 29 Apr 2018 01:14:47 GMT  
		Size: 16.3 MB (16257053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd380884828285357ffcb654be990d63b59cba21329d7b0e86bb84c392f380d`  
		Last Modified: Sun, 29 Apr 2018 01:15:22 GMT  
		Size: 88.4 MB (88416045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc216f41b9ef5303ebabc6dbb110ebc7888185cc3f13ee1a8aa785d0ef87c87`  
		Last Modified: Sun, 29 Apr 2018 01:14:33 GMT  
		Size: 14.6 MB (14577619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb69e16e51ae732ae305f11738095bd7425a0f0acd139d0fb9512903c5bed5b`  
		Last Modified: Sun, 29 Apr 2018 01:14:28 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.22.4` - linux; ppc64le

```console
$ docker pull ghost@sha256:f56272ee3bec0ff565923fe3319939386bbe4848be8e233ccf5b4b7d1f87ddb2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206764570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2fc081e3183a1e5c400d2d8d3d5e1b26a9f841efce50d1afd6ce1a06b942f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 08:17:46 GMT
ADD file:6a4bd4ea54f669286e984ecf8178e1fa7c12c8b6fc0f96e4203ae7a6f99a2279 in / 
# Sat, 28 Apr 2018 08:17:47 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:49:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:49:27 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 16:06:30 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 16:07:44 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 16:07:46 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 16:07:54 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 16:07:55 GMT
CMD ["node"]
# Sat, 28 Apr 2018 20:25:42 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 20:25:47 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 20:25:51 GMT
ENV NODE_ENV=production
# Sat, 28 Apr 2018 20:25:52 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sat, 28 Apr 2018 20:26:21 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sat, 28 Apr 2018 20:26:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 28 Apr 2018 20:26:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 28 Apr 2018 20:26:26 GMT
ENV GHOST_VERSION=1.22.4
# Sat, 28 Apr 2018 20:27:39 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sat, 28 Apr 2018 20:27:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 28 Apr 2018 20:31:17 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sat, 28 Apr 2018 20:31:18 GMT
WORKDIR /var/lib/ghost
# Sat, 28 Apr 2018 20:31:19 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 28 Apr 2018 20:31:20 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 28 Apr 2018 20:31:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 20:31:22 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 20:31:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2668401c9f940b1d6b03e5f0086fa248cb957610ef9a7c79983d2fb0707ec76c`  
		Last Modified: Sat, 28 Apr 2018 08:24:36 GMT  
		Size: 53.4 MB (53392811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feb4c62e83f77f05ed3c1a72c453fce29bc8adee3ff31855937f28f0b9ad00`  
		Last Modified: Sat, 28 Apr 2018 10:38:43 GMT  
		Size: 17.6 MB (17571133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033729a6b8a78e4b13cad1f1d95e6f4ab8461fcb87c89fb4882c297de02fbad`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 4.4 KB (4438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd479c883acc5f45e3b06fe53ee3e824909480d7ee4035c57a3303a6058d3c1`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 117.7 KB (117651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5de8244112e4f1d6cb1f72cc7c9021d8f19e4df7a44412b636ab3b2dcc500d`  
		Last Modified: Sat, 28 Apr 2018 16:38:33 GMT  
		Size: 14.5 MB (14503944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbfc0285034d19463723dc2bed92d0074a197c39428886cf1bbe764a96829bd`  
		Last Modified: Sat, 28 Apr 2018 16:38:26 GMT  
		Size: 1.1 MB (1061054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106276b354e2e0c612a5a63f7f154018817cdf54431e5f43f5776c5e07ecbfeb`  
		Last Modified: Sat, 28 Apr 2018 20:35:58 GMT  
		Size: 469.8 KB (469843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874747483b33baf03454207a8496c6f1c13e7e1b2e2ed153e2ef152a446fc2c4`  
		Last Modified: Sat, 28 Apr 2018 20:36:04 GMT  
		Size: 16.3 MB (16257633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61761a09547322f759f585ad3a5e134158e4d86a38ca93bfeb01eebe4172601f`  
		Last Modified: Sat, 28 Apr 2018 20:36:24 GMT  
		Size: 88.4 MB (88416450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b047143f9c8053ed1d51a6cb0ba106e4b5eb48804b0361be72bdba4a2b2f49c1`  
		Last Modified: Sat, 28 Apr 2018 20:36:02 GMT  
		Size: 15.0 MB (14969044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5cdc26a555aab106ec7f00ffedbc2a1d5bd8a34ef6cb46ae3d485f3c63cdad`  
		Last Modified: Sat, 28 Apr 2018 20:35:58 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:1.22.4` - linux; s390x

```console
$ docker pull ghost@sha256:81f5f3c0951fad3eaf4783cfb506783cb58e4cb0b883bc1e12f276bc4e2bb63b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208458660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc7a15740f7dda893e38d7a798724139b63760ada2f2d7281fab8a109b9f9ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 11:42:31 GMT
ADD file:ac1cfec75c7e1898f2c9b7d17653da3684fdda7d14440ce16f1939bb66105cdc in / 
# Sat, 28 Apr 2018 11:42:31 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 13:13:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:13:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:27:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 13:27:15 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 17:51:04 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 17:51:18 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 17:51:18 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 17:51:20 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 17:51:21 GMT
CMD ["node"]
# Sat, 28 Apr 2018 21:23:28 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 21:23:31 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 21:23:31 GMT
ENV NODE_ENV=production
# Sat, 28 Apr 2018 21:23:31 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sat, 28 Apr 2018 21:23:58 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_VERSION=1.22.4
# Sat, 28 Apr 2018 21:24:34 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sat, 28 Apr 2018 21:24:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 28 Apr 2018 21:26:09 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sat, 28 Apr 2018 21:26:09 GMT
WORKDIR /var/lib/ghost
# Sat, 28 Apr 2018 21:26:09 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 28 Apr 2018 21:26:09 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 28 Apr 2018 21:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 21:26:10 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 21:26:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e0524893a6d25f3e36c190fea678ecf1845e7c0d2ba833b077a429d64b943e0a`  
		Last Modified: Sat, 28 Apr 2018 11:47:52 GMT  
		Size: 54.5 MB (54465857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331cf8e884c1052e19f6b80b3efb54a7163ab49bf54c631bd861332c232029f`  
		Last Modified: Sat, 28 Apr 2018 13:29:06 GMT  
		Size: 17.8 MB (17767296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1573c40a4e9e40c7d5639586badca4c9ac2080488a599636910b77ac19a689`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd78e74bc99cbd7061122cf0fe9a054fb495f9bef7ef1502f65f98935d869fb`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 117.6 KB (117619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffe8a451803f5c963bc7fe27269ca01a9b6c131bcd1e034753682cd9a541d8`  
		Last Modified: Sat, 28 Apr 2018 17:57:39 GMT  
		Size: 14.9 MB (14874582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a235333140b41b4b113ac11697676cd325aeb3a46bcc9b1fd3e651dabb7cecd`  
		Last Modified: Sat, 28 Apr 2018 17:57:35 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f537d58daec665e17610dcf1d6af3558ca76a008f6a2fdadf737f9325c7d3082`  
		Last Modified: Sat, 28 Apr 2018 21:28:52 GMT  
		Size: 486.8 KB (486818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a074f20bae5534585e5d7a6fe7d254e379da438972f46189a6a5875a54f57985`  
		Last Modified: Sat, 28 Apr 2018 21:28:57 GMT  
		Size: 16.3 MB (16257593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51badbc99b7366403d7cb169dcb78e5028627a527199373496307783407df534`  
		Last Modified: Sat, 28 Apr 2018 21:29:11 GMT  
		Size: 88.4 MB (88415393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f4480bd6e9f5b63057a66c4282d12c8100f94d143cb2d862714b3f2ac2936b`  
		Last Modified: Sat, 28 Apr 2018 21:28:55 GMT  
		Size: 15.0 MB (15007486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec20f88c0d9020e097835ab6d067f49ddeb0f0cc23f833f2285b91b22eed9e1`  
		Last Modified: Sat, 28 Apr 2018 21:28:51 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1.22.4-alpine`

```console
$ docker pull ghost@sha256:ef074eac4e70546ecf57e8f3042aff880f3ce980440616dec69cce29d3d0dd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:1.22.4-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1b1441e96a8c051febc161b66f6d3d8485d88f234bd3bece4a5cb562b8645fe5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128766560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeb3b8b07a4196ade26900d1ab511a701cb872fc996e237cddf5b0a31e69fc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jan 2018 21:12:40 GMT
ADD file:69848cb51056edaf120230b6f218a79968ac797295c2cef6728332e1801357be in / 
# Tue, 09 Jan 2018 21:12:40 GMT
CMD ["/bin/sh"]
# Tue, 03 Apr 2018 00:59:06 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:11:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Tue, 03 Apr 2018 01:11:15 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:11:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 03 Apr 2018 01:11:28 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:30:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 03 Apr 2018 03:30:26 GMT
RUN apk add --no-cache 		bash
# Tue, 03 Apr 2018 03:30:27 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 01:17:11 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 01:17:34 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 01:17:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 01:17:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Apr 2018 22:44:48 GMT
ENV GHOST_VERSION=1.22.4
# Thu, 26 Apr 2018 22:45:30 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Thu, 26 Apr 2018 22:45:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Thu, 26 Apr 2018 22:45:31 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Apr 2018 22:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Apr 2018 22:45:32 GMT
COPY file:fe4f8ce065580d78daf2ea3ae3ab9174f3edd7740df8b95889926dc1cdfe77b0 in /usr/local/bin 
# Thu, 26 Apr 2018 22:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Apr 2018 22:45:33 GMT
EXPOSE 2368/tcp
# Thu, 26 Apr 2018 22:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:81033e7c1d6a5b44a94bb6b40033a6e589f50fd6b61578da6fc809e61f83898d`  
		Last Modified: Tue, 09 Jan 2018 21:15:04 GMT  
		Size: 2.4 MB (2387570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209940bfc9f474ff72013592d16fc0ac86f853491445f1bf606be599b1dbcb00`  
		Last Modified: Tue, 03 Apr 2018 02:24:08 GMT  
		Size: 15.5 MB (15474763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa77586de2de2644543aefeb4063f73eada8e9f8a796defd6f52b933113ab498`  
		Last Modified: Tue, 03 Apr 2018 02:24:03 GMT  
		Size: 1.1 MB (1067448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f63a91c1a5067bc9ab0a4de592d46c41d6362a6197ff98c476a68c48e2d293`  
		Last Modified: Tue, 03 Apr 2018 04:22:20 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354ff75e983303ad1aaee1b5251e9bca04803485927e18f5db013f84c27484c`  
		Last Modified: Tue, 03 Apr 2018 04:22:26 GMT  
		Size: 1.1 MB (1119103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a42dd7600b77231b0d305d6ff58b8f9f7cf95fe2b7040cbca1834e62a7daaa`  
		Last Modified: Thu, 12 Apr 2018 01:54:20 GMT  
		Size: 16.2 MB (16183020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc03bba8924a27f1696b3bc7230ce49058db74bc2d1e4a5d1145cfb83a8f3b1`  
		Last Modified: Thu, 26 Apr 2018 22:48:45 GMT  
		Size: 92.5 MB (92525729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4dce88fcd1844118c10e13469b21a5533b329799a03cc0a7fef5323bc2b18b`  
		Last Modified: Thu, 26 Apr 2018 22:48:30 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1.22-alpine`

```console
$ docker pull ghost@sha256:ef074eac4e70546ecf57e8f3042aff880f3ce980440616dec69cce29d3d0dd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:1.22-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1b1441e96a8c051febc161b66f6d3d8485d88f234bd3bece4a5cb562b8645fe5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128766560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeb3b8b07a4196ade26900d1ab511a701cb872fc996e237cddf5b0a31e69fc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jan 2018 21:12:40 GMT
ADD file:69848cb51056edaf120230b6f218a79968ac797295c2cef6728332e1801357be in / 
# Tue, 09 Jan 2018 21:12:40 GMT
CMD ["/bin/sh"]
# Tue, 03 Apr 2018 00:59:06 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:11:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Tue, 03 Apr 2018 01:11:15 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:11:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 03 Apr 2018 01:11:28 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:30:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 03 Apr 2018 03:30:26 GMT
RUN apk add --no-cache 		bash
# Tue, 03 Apr 2018 03:30:27 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 01:17:11 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 01:17:34 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 01:17:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 01:17:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Apr 2018 22:44:48 GMT
ENV GHOST_VERSION=1.22.4
# Thu, 26 Apr 2018 22:45:30 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Thu, 26 Apr 2018 22:45:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Thu, 26 Apr 2018 22:45:31 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Apr 2018 22:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Apr 2018 22:45:32 GMT
COPY file:fe4f8ce065580d78daf2ea3ae3ab9174f3edd7740df8b95889926dc1cdfe77b0 in /usr/local/bin 
# Thu, 26 Apr 2018 22:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Apr 2018 22:45:33 GMT
EXPOSE 2368/tcp
# Thu, 26 Apr 2018 22:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:81033e7c1d6a5b44a94bb6b40033a6e589f50fd6b61578da6fc809e61f83898d`  
		Last Modified: Tue, 09 Jan 2018 21:15:04 GMT  
		Size: 2.4 MB (2387570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209940bfc9f474ff72013592d16fc0ac86f853491445f1bf606be599b1dbcb00`  
		Last Modified: Tue, 03 Apr 2018 02:24:08 GMT  
		Size: 15.5 MB (15474763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa77586de2de2644543aefeb4063f73eada8e9f8a796defd6f52b933113ab498`  
		Last Modified: Tue, 03 Apr 2018 02:24:03 GMT  
		Size: 1.1 MB (1067448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f63a91c1a5067bc9ab0a4de592d46c41d6362a6197ff98c476a68c48e2d293`  
		Last Modified: Tue, 03 Apr 2018 04:22:20 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354ff75e983303ad1aaee1b5251e9bca04803485927e18f5db013f84c27484c`  
		Last Modified: Tue, 03 Apr 2018 04:22:26 GMT  
		Size: 1.1 MB (1119103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a42dd7600b77231b0d305d6ff58b8f9f7cf95fe2b7040cbca1834e62a7daaa`  
		Last Modified: Thu, 12 Apr 2018 01:54:20 GMT  
		Size: 16.2 MB (16183020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc03bba8924a27f1696b3bc7230ce49058db74bc2d1e4a5d1145cfb83a8f3b1`  
		Last Modified: Thu, 26 Apr 2018 22:48:45 GMT  
		Size: 92.5 MB (92525729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4dce88fcd1844118c10e13469b21a5533b329799a03cc0a7fef5323bc2b18b`  
		Last Modified: Thu, 26 Apr 2018 22:48:30 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:1-alpine`

```console
$ docker pull ghost@sha256:ef074eac4e70546ecf57e8f3042aff880f3ce980440616dec69cce29d3d0dd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:1-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1b1441e96a8c051febc161b66f6d3d8485d88f234bd3bece4a5cb562b8645fe5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128766560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeb3b8b07a4196ade26900d1ab511a701cb872fc996e237cddf5b0a31e69fc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jan 2018 21:12:40 GMT
ADD file:69848cb51056edaf120230b6f218a79968ac797295c2cef6728332e1801357be in / 
# Tue, 09 Jan 2018 21:12:40 GMT
CMD ["/bin/sh"]
# Tue, 03 Apr 2018 00:59:06 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:11:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Tue, 03 Apr 2018 01:11:15 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:11:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 03 Apr 2018 01:11:28 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:30:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 03 Apr 2018 03:30:26 GMT
RUN apk add --no-cache 		bash
# Tue, 03 Apr 2018 03:30:27 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 01:17:11 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 01:17:34 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 01:17:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 01:17:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Apr 2018 22:44:48 GMT
ENV GHOST_VERSION=1.22.4
# Thu, 26 Apr 2018 22:45:30 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Thu, 26 Apr 2018 22:45:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Thu, 26 Apr 2018 22:45:31 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Apr 2018 22:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Apr 2018 22:45:32 GMT
COPY file:fe4f8ce065580d78daf2ea3ae3ab9174f3edd7740df8b95889926dc1cdfe77b0 in /usr/local/bin 
# Thu, 26 Apr 2018 22:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Apr 2018 22:45:33 GMT
EXPOSE 2368/tcp
# Thu, 26 Apr 2018 22:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:81033e7c1d6a5b44a94bb6b40033a6e589f50fd6b61578da6fc809e61f83898d`  
		Last Modified: Tue, 09 Jan 2018 21:15:04 GMT  
		Size: 2.4 MB (2387570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209940bfc9f474ff72013592d16fc0ac86f853491445f1bf606be599b1dbcb00`  
		Last Modified: Tue, 03 Apr 2018 02:24:08 GMT  
		Size: 15.5 MB (15474763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa77586de2de2644543aefeb4063f73eada8e9f8a796defd6f52b933113ab498`  
		Last Modified: Tue, 03 Apr 2018 02:24:03 GMT  
		Size: 1.1 MB (1067448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f63a91c1a5067bc9ab0a4de592d46c41d6362a6197ff98c476a68c48e2d293`  
		Last Modified: Tue, 03 Apr 2018 04:22:20 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354ff75e983303ad1aaee1b5251e9bca04803485927e18f5db013f84c27484c`  
		Last Modified: Tue, 03 Apr 2018 04:22:26 GMT  
		Size: 1.1 MB (1119103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a42dd7600b77231b0d305d6ff58b8f9f7cf95fe2b7040cbca1834e62a7daaa`  
		Last Modified: Thu, 12 Apr 2018 01:54:20 GMT  
		Size: 16.2 MB (16183020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc03bba8924a27f1696b3bc7230ce49058db74bc2d1e4a5d1145cfb83a8f3b1`  
		Last Modified: Thu, 26 Apr 2018 22:48:45 GMT  
		Size: 92.5 MB (92525729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4dce88fcd1844118c10e13469b21a5533b329799a03cc0a7fef5323bc2b18b`  
		Last Modified: Thu, 26 Apr 2018 22:48:30 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:alpine`

```console
$ docker pull ghost@sha256:ef074eac4e70546ecf57e8f3042aff880f3ce980440616dec69cce29d3d0dd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:alpine` - linux; amd64

```console
$ docker pull ghost@sha256:1b1441e96a8c051febc161b66f6d3d8485d88f234bd3bece4a5cb562b8645fe5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128766560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeb3b8b07a4196ade26900d1ab511a701cb872fc996e237cddf5b0a31e69fc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 09 Jan 2018 21:12:40 GMT
ADD file:69848cb51056edaf120230b6f218a79968ac797295c2cef6728332e1801357be in / 
# Tue, 09 Jan 2018 21:12:40 GMT
CMD ["/bin/sh"]
# Tue, 03 Apr 2018 00:59:06 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:11:15 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Tue, 03 Apr 2018 01:11:15 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:11:28 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Tue, 03 Apr 2018 01:11:28 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:30:23 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 03 Apr 2018 03:30:26 GMT
RUN apk add --no-cache 		bash
# Tue, 03 Apr 2018 03:30:27 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 01:17:11 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 01:17:34 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 01:17:35 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 01:17:35 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Apr 2018 22:44:48 GMT
ENV GHOST_VERSION=1.22.4
# Thu, 26 Apr 2018 22:45:30 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		su-exec node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	su-exec node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	su-exec node ghost config paths.contentPath "$GHOST_CONTENT"; 		su-exec node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Thu, 26 Apr 2018 22:45:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Thu, 26 Apr 2018 22:45:31 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Apr 2018 22:45:32 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Apr 2018 22:45:32 GMT
COPY file:fe4f8ce065580d78daf2ea3ae3ab9174f3edd7740df8b95889926dc1cdfe77b0 in /usr/local/bin 
# Thu, 26 Apr 2018 22:45:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Apr 2018 22:45:33 GMT
EXPOSE 2368/tcp
# Thu, 26 Apr 2018 22:45:33 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:81033e7c1d6a5b44a94bb6b40033a6e589f50fd6b61578da6fc809e61f83898d`  
		Last Modified: Tue, 09 Jan 2018 21:15:04 GMT  
		Size: 2.4 MB (2387570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209940bfc9f474ff72013592d16fc0ac86f853491445f1bf606be599b1dbcb00`  
		Last Modified: Tue, 03 Apr 2018 02:24:08 GMT  
		Size: 15.5 MB (15474763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa77586de2de2644543aefeb4063f73eada8e9f8a796defd6f52b933113ab498`  
		Last Modified: Tue, 03 Apr 2018 02:24:03 GMT  
		Size: 1.1 MB (1067448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f63a91c1a5067bc9ab0a4de592d46c41d6362a6197ff98c476a68c48e2d293`  
		Last Modified: Tue, 03 Apr 2018 04:22:20 GMT  
		Size: 8.4 KB (8365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e354ff75e983303ad1aaee1b5251e9bca04803485927e18f5db013f84c27484c`  
		Last Modified: Tue, 03 Apr 2018 04:22:26 GMT  
		Size: 1.1 MB (1119103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a42dd7600b77231b0d305d6ff58b8f9f7cf95fe2b7040cbca1834e62a7daaa`  
		Last Modified: Thu, 12 Apr 2018 01:54:20 GMT  
		Size: 16.2 MB (16183020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc03bba8924a27f1696b3bc7230ce49058db74bc2d1e4a5d1145cfb83a8f3b1`  
		Last Modified: Thu, 26 Apr 2018 22:48:45 GMT  
		Size: 92.5 MB (92525729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4dce88fcd1844118c10e13469b21a5533b329799a03cc0a7fef5323bc2b18b`  
		Last Modified: Thu, 26 Apr 2018 22:48:30 GMT  
		Size: 562.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ghost:latest`

```console
$ docker pull ghost@sha256:718305e66b49acc4b3baa55f5168b0b15e7b7e711bb7bc0b3c022230802fa4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ghost:latest` - linux; amd64

```console
$ docker pull ghost@sha256:e40c4bcc7eb80cf7dbf70b5da7c55318de86fb87c0915cc9c257d398ac128db6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.9 MB (203864383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ae45da9a3820b25a40b776e08a494dc9c54ed52c21f3b6ef00317821830898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Tue, 13 Mar 2018 21:57:21 GMT
ADD file:bc844c4763367b5f0ac7b9aebf7d43900d98f2aca101b886f185347b24973dbe in / 
# Tue, 13 Mar 2018 21:57:22 GMT
CMD ["bash"]
# Tue, 13 Mar 2018 23:39:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Mar 2018 23:39:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:03:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:03:53 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 01:31:24 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 01:31:50 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 01:31:51 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 01:31:55 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 01:31:55 GMT
CMD ["node"]
# Tue, 03 Apr 2018 03:16:20 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 03:16:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 03:16:26 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 00:58:56 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 00:59:18 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 00:59:19 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 00:59:19 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Thu, 26 Apr 2018 22:20:44 GMT
ENV GHOST_VERSION=1.22.4
# Thu, 26 Apr 2018 22:21:41 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Thu, 26 Apr 2018 22:21:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Thu, 26 Apr 2018 22:21:57 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Thu, 26 Apr 2018 22:21:58 GMT
WORKDIR /var/lib/ghost
# Thu, 26 Apr 2018 22:21:58 GMT
VOLUME [/var/lib/ghost/content]
# Thu, 26 Apr 2018 22:21:58 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Thu, 26 Apr 2018 22:21:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 Apr 2018 22:21:59 GMT
EXPOSE 2368/tcp
# Thu, 26 Apr 2018 22:22:00 GMT
CMD ["node" "current/index.js"]
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
	-	`sha256:c669d5da499dfc3f959bff647d84aa109d42bd9dc4a84cd1736607a9a193931e`  
		Last Modified: Thu, 15 Mar 2018 05:16:20 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e8ff4c87216eb5e2bdc5aeab7d50e312312df3b9358eac4f84cd10c0db8d7c`  
		Last Modified: Thu, 15 Mar 2018 05:16:18 GMT  
		Size: 117.6 KB (117624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d93f330ca2fc79c95fa142b121be257ae64491015b8997cd012096fbd113fb`  
		Last Modified: Tue, 03 Apr 2018 02:26:55 GMT  
		Size: 14.7 MB (14743833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5858a3ea9339b3a6db832ae2fbb00a02d8b6475f2af80f473668cd6e3f468e`  
		Last Modified: Tue, 03 Apr 2018 02:26:50 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b010a0bd596683d76af178e796e93e84e436e54c58dcc7ad9c45bc570397b991`  
		Last Modified: Tue, 03 Apr 2018 04:09:56 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7606873b40fac8eab3ac4b91312c121e6e805ae0e43240d3d8eab946e0017894`  
		Last Modified: Thu, 12 Apr 2018 01:35:39 GMT  
		Size: 16.2 MB (16182884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017a974e240a8939f895809f77d39022cae4b5948af764e43bdd2d3607be561d`  
		Last Modified: Thu, 26 Apr 2018 22:47:01 GMT  
		Size: 92.5 MB (92526922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408055898ca79d33a62bdc62b3c661f56ded6cc1ed390deec9dac794634fec4c`  
		Last Modified: Thu, 26 Apr 2018 22:46:27 GMT  
		Size: 6.9 MB (6851727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2d4b7c515fcfd6fac3c947eac8d79cfaf5dd0e6485adf1d1f1605862a8ea33`  
		Last Modified: Thu, 26 Apr 2018 22:46:26 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; arm64 variant v8

```console
$ docker pull ghost@sha256:365d6e3763e08cfd769c13f2740d28a4a4ed5a54ce122d0e27ffee79a35d85d6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204156200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7fecd9bfe81d041879ca054db1a813e34f8ba550d90ce6b63ee3fc843d41b66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Wed, 14 Mar 2018 17:24:26 GMT
ADD file:bcd41493879aaeeecb9c960b91c9954b1e0229e91b7a070cb6b2dfdadc8c52b8 in / 
# Wed, 14 Mar 2018 17:24:27 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 18:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 14 Mar 2018 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Mar 2018 05:32:46 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 15 Mar 2018 05:32:54 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 03 Apr 2018 17:20:46 GMT
ENV NODE_VERSION=6.14.1
# Tue, 03 Apr 2018 17:21:12 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Tue, 03 Apr 2018 17:21:13 GMT
ENV YARN_VERSION=1.5.1
# Tue, 03 Apr 2018 17:21:17 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Tue, 03 Apr 2018 17:21:18 GMT
CMD ["node"]
# Tue, 03 Apr 2018 18:09:28 GMT
ENV GOSU_VERSION=1.10
# Tue, 03 Apr 2018 18:09:33 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Tue, 03 Apr 2018 18:09:34 GMT
ENV NODE_ENV=production
# Thu, 12 Apr 2018 08:40:29 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Thu, 12 Apr 2018 08:41:24 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Thu, 12 Apr 2018 08:41:26 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Thu, 12 Apr 2018 08:41:27 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Fri, 27 Apr 2018 09:14:12 GMT
ENV GHOST_VERSION=1.22.4
# Fri, 27 Apr 2018 09:15:57 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Fri, 27 Apr 2018 09:16:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Fri, 27 Apr 2018 09:20:18 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Fri, 27 Apr 2018 09:20:29 GMT
WORKDIR /var/lib/ghost
# Fri, 27 Apr 2018 09:20:30 GMT
VOLUME [/var/lib/ghost/content]
# Fri, 27 Apr 2018 09:20:53 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Fri, 27 Apr 2018 09:20:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Apr 2018 09:20:54 GMT
EXPOSE 2368/tcp
# Fri, 27 Apr 2018 09:20:55 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:21ccda36f02cc1214a990aa0c90bf9e705d50f6bf9844bffa71a8fbff898df30`  
		Last Modified: Wed, 14 Mar 2018 17:37:55 GMT  
		Size: 49.9 MB (49933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c0a429742ffe0333a0070020d4aa3cfeaa1d0f87e652544b8b823ab168f1bd`  
		Last Modified: Wed, 14 Mar 2018 19:01:35 GMT  
		Size: 18.7 MB (18739890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63586fce2b79360f2899b20720f2e27aa341e7aadc0a15c96e68e3823f9704a7`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 4.4 KB (4414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc8c07863bd16bea098044bed1067f4cff1c67dcb8c2277e0ac929e47f7278`  
		Last Modified: Thu, 15 Mar 2018 05:42:26 GMT  
		Size: 117.6 KB (117626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641f57e7df1914d159b6cc44e74272a61708d45911dd38659ed7a0bc8652cc0c`  
		Last Modified: Tue, 03 Apr 2018 17:44:50 GMT  
		Size: 14.7 MB (14726891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c99f90a2f0cf1c8de6b92bf7de39a380732bb3a57eb38e7f264cfaf03d55e68`  
		Last Modified: Tue, 03 Apr 2018 17:44:44 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83dbd2b75e13cb287246e957f883f7fd160dbce4c9a09b16068447af044293e7`  
		Last Modified: Tue, 03 Apr 2018 18:22:31 GMT  
		Size: 468.7 KB (468695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea4b61c0d04f6207030b358953ed1e4e68e476a0507cf6eeb1631c3a3cca44`  
		Last Modified: Thu, 12 Apr 2018 08:49:33 GMT  
		Size: 16.2 MB (16184727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d7f6494548f90898a2d52bfd78e46701fbb3714ecc1ca975edcab447688d3e`  
		Last Modified: Fri, 27 Apr 2018 09:22:49 GMT  
		Size: 88.4 MB (88418844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab5dcc29fe315af7f8ef53411f43bbb652bcd0b92275277eba4067017856620`  
		Last Modified: Fri, 27 Apr 2018 09:22:15 GMT  
		Size: 14.5 MB (14500041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a11ab7a7ca0663ae27821e2c4c8cedec882e37fb388588153c4f20db1f01052`  
		Last Modified: Fri, 27 Apr 2018 09:22:10 GMT  
		Size: 572.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; 386

```console
$ docker pull ghost@sha256:b3001b000c2743b8ff351324c20904ab969514e75e5f6df488a5f3d154e785ad
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209528850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce0f03200c6e6899adf222c7102400d24ba98f7e08f54abcebcee3ce26defc4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 10:39:32 GMT
ADD file:ce5174f2b2c155a2421fac3ff37a02d9551d5d79e31a541189bcfd2416a6903a in / 
# Sat, 28 Apr 2018 10:39:32 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 12:05:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 12:05:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 19:37:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 19:37:46 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 19:40:46 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 19:41:22 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 19:41:23 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 19:41:26 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 19:41:26 GMT
CMD ["node"]
# Sun, 29 Apr 2018 01:04:49 GMT
ENV GOSU_VERSION=1.10
# Sun, 29 Apr 2018 01:04:54 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 29 Apr 2018 01:04:54 GMT
ENV NODE_ENV=production
# Sun, 29 Apr 2018 01:04:54 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sun, 29 Apr 2018 01:05:16 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sun, 29 Apr 2018 01:05:16 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sun, 29 Apr 2018 01:05:16 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sun, 29 Apr 2018 01:05:17 GMT
ENV GHOST_VERSION=1.22.4
# Sun, 29 Apr 2018 01:05:56 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sun, 29 Apr 2018 01:05:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sun, 29 Apr 2018 01:07:53 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sun, 29 Apr 2018 01:07:53 GMT
WORKDIR /var/lib/ghost
# Sun, 29 Apr 2018 01:07:53 GMT
VOLUME [/var/lib/ghost/content]
# Sun, 29 Apr 2018 01:07:53 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sun, 29 Apr 2018 01:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 29 Apr 2018 01:07:54 GMT
EXPOSE 2368/tcp
# Sun, 29 Apr 2018 01:07:54 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:05b419d667f793c8c2edf0ff0aec14fc4d66733cdb89957ac89e8bfbeaddd0fa`  
		Last Modified: Sat, 28 Apr 2018 10:44:20 GMT  
		Size: 54.5 MB (54486782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b9c3b7ebe34e933c240e5eb7f8620732974e6e15e2c5d17cb91ca2aefffa4`  
		Last Modified: Sat, 28 Apr 2018 12:41:22 GMT  
		Size: 19.9 MB (19866118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618a70cca8b81e7f688c7591ffb047d440d878e7c088b564e9e8611c1157dba5`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 4.4 KB (4394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2b5615162ffa8552b2e45aa789d255d2331fa388ef168bf3115fe546951502`  
		Last Modified: Sat, 28 Apr 2018 19:46:03 GMT  
		Size: 117.6 KB (117613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaed2e884f6af6104db06b2e80bded57362da5e944d4989cfbeff5a34d9e92c`  
		Last Modified: Sat, 28 Apr 2018 19:49:36 GMT  
		Size: 14.3 MB (14261060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5257a1a666582990768f9724f4b53651529a7198d15c2c70284e376f9e365fc`  
		Last Modified: Sat, 28 Apr 2018 19:49:31 GMT  
		Size: 1.1 MB (1061027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f8e5a06d23067ba52decc6561352f68a27347a09f11ee293c7a77d17cfdd21`  
		Last Modified: Sun, 29 Apr 2018 01:14:28 GMT  
		Size: 480.6 KB (480570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae231f09a834d53c6c0d553571b32a5fe50227c6ed7d0a1f3bfc940d12f8bab7`  
		Last Modified: Sun, 29 Apr 2018 01:14:47 GMT  
		Size: 16.3 MB (16257053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd380884828285357ffcb654be990d63b59cba21329d7b0e86bb84c392f380d`  
		Last Modified: Sun, 29 Apr 2018 01:15:22 GMT  
		Size: 88.4 MB (88416045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc216f41b9ef5303ebabc6dbb110ebc7888185cc3f13ee1a8aa785d0ef87c87`  
		Last Modified: Sun, 29 Apr 2018 01:14:33 GMT  
		Size: 14.6 MB (14577619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb69e16e51ae732ae305f11738095bd7425a0f0acd139d0fb9512903c5bed5b`  
		Last Modified: Sun, 29 Apr 2018 01:14:28 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; ppc64le

```console
$ docker pull ghost@sha256:f56272ee3bec0ff565923fe3319939386bbe4848be8e233ccf5b4b7d1f87ddb2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206764570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2fc081e3183a1e5c400d2d8d3d5e1b26a9f841efce50d1afd6ce1a06b942f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 08:17:46 GMT
ADD file:6a4bd4ea54f669286e984ecf8178e1fa7c12c8b6fc0f96e4203ae7a6f99a2279 in / 
# Sat, 28 Apr 2018 08:17:47 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 09:53:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 09:53:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 15:49:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 15:49:27 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 16:06:30 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 16:07:44 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 16:07:46 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 16:07:54 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 16:07:55 GMT
CMD ["node"]
# Sat, 28 Apr 2018 20:25:42 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 20:25:47 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 20:25:51 GMT
ENV NODE_ENV=production
# Sat, 28 Apr 2018 20:25:52 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sat, 28 Apr 2018 20:26:21 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sat, 28 Apr 2018 20:26:24 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 28 Apr 2018 20:26:25 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 28 Apr 2018 20:26:26 GMT
ENV GHOST_VERSION=1.22.4
# Sat, 28 Apr 2018 20:27:39 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sat, 28 Apr 2018 20:27:41 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 28 Apr 2018 20:31:17 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sat, 28 Apr 2018 20:31:18 GMT
WORKDIR /var/lib/ghost
# Sat, 28 Apr 2018 20:31:19 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 28 Apr 2018 20:31:20 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 28 Apr 2018 20:31:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 20:31:22 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 20:31:23 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:2668401c9f940b1d6b03e5f0086fa248cb957610ef9a7c79983d2fb0707ec76c`  
		Last Modified: Sat, 28 Apr 2018 08:24:36 GMT  
		Size: 53.4 MB (53392811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73feb4c62e83f77f05ed3c1a72c453fce29bc8adee3ff31855937f28f0b9ad00`  
		Last Modified: Sat, 28 Apr 2018 10:38:43 GMT  
		Size: 17.6 MB (17571133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b033729a6b8a78e4b13cad1f1d95e6f4ab8461fcb87c89fb4882c297de02fbad`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 4.4 KB (4438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd479c883acc5f45e3b06fe53ee3e824909480d7ee4035c57a3303a6058d3c1`  
		Last Modified: Sat, 28 Apr 2018 16:32:50 GMT  
		Size: 117.7 KB (117651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5de8244112e4f1d6cb1f72cc7c9021d8f19e4df7a44412b636ab3b2dcc500d`  
		Last Modified: Sat, 28 Apr 2018 16:38:33 GMT  
		Size: 14.5 MB (14503944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbfc0285034d19463723dc2bed92d0074a197c39428886cf1bbe764a96829bd`  
		Last Modified: Sat, 28 Apr 2018 16:38:26 GMT  
		Size: 1.1 MB (1061054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106276b354e2e0c612a5a63f7f154018817cdf54431e5f43f5776c5e07ecbfeb`  
		Last Modified: Sat, 28 Apr 2018 20:35:58 GMT  
		Size: 469.8 KB (469843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874747483b33baf03454207a8496c6f1c13e7e1b2e2ed153e2ef152a446fc2c4`  
		Last Modified: Sat, 28 Apr 2018 20:36:04 GMT  
		Size: 16.3 MB (16257633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61761a09547322f759f585ad3a5e134158e4d86a38ca93bfeb01eebe4172601f`  
		Last Modified: Sat, 28 Apr 2018 20:36:24 GMT  
		Size: 88.4 MB (88416450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b047143f9c8053ed1d51a6cb0ba106e4b5eb48804b0361be72bdba4a2b2f49c1`  
		Last Modified: Sat, 28 Apr 2018 20:36:02 GMT  
		Size: 15.0 MB (14969044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5cdc26a555aab106ec7f00ffedbc2a1d5bd8a34ef6cb46ae3d485f3c63cdad`  
		Last Modified: Sat, 28 Apr 2018 20:35:58 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ghost:latest` - linux; s390x

```console
$ docker pull ghost@sha256:81f5f3c0951fad3eaf4783cfb506783cb58e4cb0b883bc1e12f276bc4e2bb63b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.5 MB (208458660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc7a15740f7dda893e38d7a798724139b63760ada2f2d7281fab8a109b9f9ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node","current\/index.js"]`

```dockerfile
# Sat, 28 Apr 2018 11:42:31 GMT
ADD file:ac1cfec75c7e1898f2c9b7d17653da3684fdda7d14440ce16f1939bb66105cdc in / 
# Sat, 28 Apr 2018 11:42:31 GMT
CMD ["bash"]
# Sat, 28 Apr 2018 13:13:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Apr 2018 13:13:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Apr 2018 13:27:14 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 28 Apr 2018 13:27:15 GMT
RUN set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 28 Apr 2018 17:51:04 GMT
ENV NODE_VERSION=6.14.1
# Sat, 28 Apr 2018 17:51:18 GMT
RUN buildDeps='xz-utils'     && ARCH= && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch##*-}" in       amd64) ARCH='x64';;       ppc64el) ARCH='ppc64le';;       s390x) ARCH='s390x';;       arm64) ARCH='arm64';;       armhf) ARCH='armv7l';;       i386) ARCH='x86';;       *) echo "unsupported architecture"; exit 1 ;;     esac     && set -x     && apt-get update && apt-get install -y $buildDeps --no-install-recommends     && rm -rf /var/lib/apt/lists/*     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner     && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt     && apt-get purge -y --auto-remove $buildDeps     && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 28 Apr 2018 17:51:18 GMT
ENV YARN_VERSION=1.5.1
# Sat, 28 Apr 2018 17:51:20 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 28 Apr 2018 17:51:21 GMT
CMD ["node"]
# Sat, 28 Apr 2018 21:23:28 GMT
ENV GOSU_VERSION=1.10
# Sat, 28 Apr 2018 21:23:31 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sat, 28 Apr 2018 21:23:31 GMT
ENV NODE_ENV=production
# Sat, 28 Apr 2018 21:23:31 GMT
ENV GHOST_CLI_VERSION=1.7.1
# Sat, 28 Apr 2018 21:23:58 GMT
RUN npm install -g "ghost-cli@$GHOST_CLI_VERSION"
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_INSTALL=/var/lib/ghost
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_CONTENT=/var/lib/ghost/content
# Sat, 28 Apr 2018 21:23:59 GMT
ENV GHOST_VERSION=1.22.4
# Sat, 28 Apr 2018 21:24:34 GMT
RUN set -ex; 	mkdir -p "$GHOST_INSTALL"; 	chown node:node "$GHOST_INSTALL"; 		gosu node ghost install "$GHOST_VERSION" --db sqlite3 --no-prompt --no-stack --no-setup --dir "$GHOST_INSTALL"; 		cd "$GHOST_INSTALL"; 	gosu node ghost config --ip 0.0.0.0 --port 2368 --no-prompt --db sqlite3 --url http://localhost:2368 --dbpath "$GHOST_CONTENT/data/ghost.db"; 	gosu node ghost config paths.contentPath "$GHOST_CONTENT"; 		gosu node ln -s config.production.json "$GHOST_INSTALL/config.development.json"; 	readlink -f "$GHOST_INSTALL/config.development.json"; 		mv "$GHOST_CONTENT" "$GHOST_INSTALL/content.orig"; 	mkdir -p "$GHOST_CONTENT"; 	chown node:node "$GHOST_CONTENT"; 		"$GHOST_INSTALL/current/node_modules/knex-migrator/bin/knex-migrator" --version
# Sat, 28 Apr 2018 21:24:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/var/lib/ghost/current/node_modules/knex-migrator/bin
# Sat, 28 Apr 2018 21:26:09 GMT
RUN set -eux; 	cd "$GHOST_INSTALL/current"; 	sqlite3Version="$(npm view . optionalDependencies.sqlite3)"; 	if ! gosu node npm install "sqlite3@$sqlite3Version"; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends python make gcc g++ libc-dev; 		rm -rf /var/lib/apt/lists/*; 				gosu node npm install "sqlite3@$sqlite3Version" --build-from-source; 				apt-mark showmanual | xargs apt-mark auto > /dev/null; 		[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 		apt-get purge -y --auto-remove; 	fi
# Sat, 28 Apr 2018 21:26:09 GMT
WORKDIR /var/lib/ghost
# Sat, 28 Apr 2018 21:26:09 GMT
VOLUME [/var/lib/ghost/content]
# Sat, 28 Apr 2018 21:26:09 GMT
COPY file:ef6da72f41bc8f60c42fab63c9c2ffdee82253c6dd2110e3d50866e5445df15e in /usr/local/bin 
# Sat, 28 Apr 2018 21:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Apr 2018 21:26:10 GMT
EXPOSE 2368/tcp
# Sat, 28 Apr 2018 21:26:10 GMT
CMD ["node" "current/index.js"]
```

-	Layers:
	-	`sha256:e0524893a6d25f3e36c190fea678ecf1845e7c0d2ba833b077a429d64b943e0a`  
		Last Modified: Sat, 28 Apr 2018 11:47:52 GMT  
		Size: 54.5 MB (54465857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2331cf8e884c1052e19f6b80b3efb54a7163ab49bf54c631bd861332c232029f`  
		Last Modified: Sat, 28 Apr 2018 13:29:06 GMT  
		Size: 17.8 MB (17767296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1573c40a4e9e40c7d5639586badca4c9ac2080488a599636910b77ac19a689`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd78e74bc99cbd7061122cf0fe9a054fb495f9bef7ef1502f65f98935d869fb`  
		Last Modified: Sat, 28 Apr 2018 13:29:01 GMT  
		Size: 117.6 KB (117619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ffe8a451803f5c963bc7fe27269ca01a9b6c131bcd1e034753682cd9a541d8`  
		Last Modified: Sat, 28 Apr 2018 17:57:39 GMT  
		Size: 14.9 MB (14874582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a235333140b41b4b113ac11697676cd325aeb3a46bcc9b1fd3e651dabb7cecd`  
		Last Modified: Sat, 28 Apr 2018 17:57:35 GMT  
		Size: 1.1 MB (1061037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f537d58daec665e17610dcf1d6af3558ca76a008f6a2fdadf737f9325c7d3082`  
		Last Modified: Sat, 28 Apr 2018 21:28:52 GMT  
		Size: 486.8 KB (486818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a074f20bae5534585e5d7a6fe7d254e379da438972f46189a6a5875a54f57985`  
		Last Modified: Sat, 28 Apr 2018 21:28:57 GMT  
		Size: 16.3 MB (16257593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51badbc99b7366403d7cb169dcb78e5028627a527199373496307783407df534`  
		Last Modified: Sat, 28 Apr 2018 21:29:11 GMT  
		Size: 88.4 MB (88415393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f4480bd6e9f5b63057a66c4282d12c8100f94d143cb2d862714b3f2ac2936b`  
		Last Modified: Sat, 28 Apr 2018 21:28:55 GMT  
		Size: 15.0 MB (15007486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec20f88c0d9020e097835ab6d067f49ddeb0f0cc23f833f2285b91b22eed9e1`  
		Last Modified: Sat, 28 Apr 2018 21:28:51 GMT  
		Size: 569.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
