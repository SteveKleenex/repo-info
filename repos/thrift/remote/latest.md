## `thrift:latest`

```console
$ docker pull thrift@sha256:3c66feffd184900df184c578ee5a3079d8873e54dc364339bdc6fc95e3d88f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `thrift:latest` - linux; amd64

```console
$ docker pull thrift@sha256:3a79992063f57245aff101e318df4689d9b50b21e52292e70ea5772851bbcb10
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51411553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93147e289c66c3df52a5328295fd02f7f4d7db2d8f8716d79225504f86e8a98c`
-	Default Command: `["thrift"]`

```dockerfile
# Tue, 13 Mar 2018 22:31:05 GMT
ADD file:fc9ba15f087e646a9d3b72e742eb1233132a118ecfa998e2497b724f3ff84061 in / 
# Tue, 13 Mar 2018 22:31:06 GMT
CMD ["bash"]
# Wed, 14 Mar 2018 04:41:54 GMT
LABEL authors=Adam Hawkins <hi@ahawkins.me>
# Wed, 14 Mar 2018 04:41:54 GMT
ENV THRIFT_VERSION=0.11.0
# Wed, 14 Mar 2018 04:44:32 GMT
RUN buildDeps=" 		automake 		bison 		curl 		flex 		g++ 		libboost-dev 		libboost-filesystem-dev 		libboost-program-options-dev 		libboost-system-dev 		libboost-test-dev 		libevent-dev 		libssl-dev 		libtool 		make 		pkg-config 	"; 	apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& curl -sSL "http://apache.mirrors.spacedump.net/thrift/$THRIFT_VERSION/thrift-$THRIFT_VERSION.tar.gz" -o thrift.tar.gz 	&& mkdir -p /usr/src/thrift 	&& tar zxf thrift.tar.gz -C /usr/src/thrift --strip-components=1 	&& rm thrift.tar.gz 	&& cd /usr/src/thrift 	&& ./configure  --without-python --without-cpp 	&& make 	&& make install 	&& cd / 	&& rm -rf /usr/src/thrift 	&& curl -k -sSL "https://storage.googleapis.com/golang/go1.4.linux-amd64.tar.gz" -o go.tar.gz 	&& tar xzf go.tar.gz 	&& rm go.tar.gz 	&& cp go/bin/gofmt /usr/bin/gofmt 	&& rm -rf go 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 14 Mar 2018 04:44:33 GMT
CMD ["thrift"]
```

-	Layers:
	-	`sha256:4269eaa217cc08668f088a9719d43c993c4644a73eda4eb55921f031a4311060`  
		Last Modified: Tue, 13 Mar 2018 22:58:14 GMT  
		Size: 38.1 MB (38111490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007b75ba5bffb966c34f0bf3c107e68164e03aef295933877a86cdcf74125017`  
		Last Modified: Wed, 14 Mar 2018 04:46:25 GMT  
		Size: 13.3 MB (13300063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
