<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:0.11`](#kong011)
-	[`kong:0.11.2`](#kong0112)
-	[`kong:0.11.2-alpine`](#kong0112-alpine)
-	[`kong:0.11-alpine`](#kong011-alpine)
-	[`kong:0.12`](#kong012)
-	[`kong:0.12.3`](#kong0123)
-	[`kong:0.12.3-alpine`](#kong0123-alpine)
-	[`kong:0.12.3-centos`](#kong0123-centos)
-	[`kong:0.12-alpine`](#kong012-alpine)
-	[`kong:0.12-centos`](#kong012-centos)
-	[`kong:0.13`](#kong013)
-	[`kong:0.13.1`](#kong0131)
-	[`kong:0.13.1-alpine`](#kong0131-alpine)
-	[`kong:0.13.1-centos`](#kong0131-centos)
-	[`kong:0.13-centos`](#kong013-centos)
-	[`kong:latest`](#konglatest)

## `kong:0.11`

```console
$ docker pull kong@sha256:9b387840f7e72d028f2acdad8275d64cc7856d7ac5148a01199fa4fc0b664839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.11` - linux; amd64

```console
$ docker pull kong@sha256:89e326840286df0d5ae28bc0fe74fb04cadb6206369fff3e894be7565e71d7c8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122028638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6474ea2e304a6456d01598db80a3b22a912d5cd907065b0aaeeb4f0bc4a4847f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Fri, 06 Apr 2018 21:01:50 GMT
ADD file:f755805244a649eccae3a3e63be291048deeb23e1c5a500d2f92b4eedc452322 in / 
# Fri, 06 Apr 2018 21:01:50 GMT
LABEL org.label-schema.schema-version== 1.0     org.label-schema.name=CentOS Base Image     org.label-schema.vendor=CentOS     org.label-schema.license=GPLv2     org.label-schema.build-date=20180402
# Fri, 06 Apr 2018 21:01:51 GMT
CMD ["/bin/bash"]
# Fri, 06 Apr 2018 22:56:06 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Fri, 06 Apr 2018 23:18:31 GMT
ENV KONG_VERSION=0.11.2
# Fri, 06 Apr 2018 23:19:25 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=centos/7/kong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Fri, 06 Apr 2018 23:19:26 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Fri, 06 Apr 2018 23:19:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Apr 2018 23:19:26 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Fri, 06 Apr 2018 23:19:26 GMT
STOPSIGNAL [SIGTERM]
# Fri, 06 Apr 2018 23:19:27 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:469cfcc7a4b3947a4fa549c68cf4f8570be53779725f0c19f3d33d1520b08db0`  
		Last Modified: Fri, 06 Apr 2018 21:19:02 GMT  
		Size: 73.2 MB (73167580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62893a76f44ec8a489d67c58724b153068978e10e0382d81eaef3f071f024a5`  
		Last Modified: Fri, 06 Apr 2018 23:22:03 GMT  
		Size: 48.9 MB (48860735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d030d765c1fc7ff1b6b364398994838a0075eaa710d1aca58cd33ddcd8fe1a2e`  
		Last Modified: Fri, 06 Apr 2018 23:21:57 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.11.2`

```console
$ docker pull kong@sha256:9b387840f7e72d028f2acdad8275d64cc7856d7ac5148a01199fa4fc0b664839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.11.2` - linux; amd64

```console
$ docker pull kong@sha256:89e326840286df0d5ae28bc0fe74fb04cadb6206369fff3e894be7565e71d7c8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122028638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6474ea2e304a6456d01598db80a3b22a912d5cd907065b0aaeeb4f0bc4a4847f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Fri, 06 Apr 2018 21:01:50 GMT
ADD file:f755805244a649eccae3a3e63be291048deeb23e1c5a500d2f92b4eedc452322 in / 
# Fri, 06 Apr 2018 21:01:50 GMT
LABEL org.label-schema.schema-version== 1.0     org.label-schema.name=CentOS Base Image     org.label-schema.vendor=CentOS     org.label-schema.license=GPLv2     org.label-schema.build-date=20180402
# Fri, 06 Apr 2018 21:01:51 GMT
CMD ["/bin/bash"]
# Fri, 06 Apr 2018 22:56:06 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Fri, 06 Apr 2018 23:18:31 GMT
ENV KONG_VERSION=0.11.2
# Fri, 06 Apr 2018 23:19:25 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=centos/7/kong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Fri, 06 Apr 2018 23:19:26 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Fri, 06 Apr 2018 23:19:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Apr 2018 23:19:26 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Fri, 06 Apr 2018 23:19:26 GMT
STOPSIGNAL [SIGTERM]
# Fri, 06 Apr 2018 23:19:27 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:469cfcc7a4b3947a4fa549c68cf4f8570be53779725f0c19f3d33d1520b08db0`  
		Last Modified: Fri, 06 Apr 2018 21:19:02 GMT  
		Size: 73.2 MB (73167580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62893a76f44ec8a489d67c58724b153068978e10e0382d81eaef3f071f024a5`  
		Last Modified: Fri, 06 Apr 2018 23:22:03 GMT  
		Size: 48.9 MB (48860735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d030d765c1fc7ff1b6b364398994838a0075eaa710d1aca58cd33ddcd8fe1a2e`  
		Last Modified: Fri, 06 Apr 2018 23:21:57 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.11.2-alpine`

```console
$ docker pull kong@sha256:0bf9d37aac28aa98336ca8041639512e975d359586334421da20384472d61e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.11.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:9aef09089b458ea181f9b87836e814b05cf7da6b722de03ecd96de31a2760d79
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30032442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaa9cf26b6af4cda25abc86b91f680b0f79122f57467bbcada859b77d8567a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 01:26:18 GMT
LABEL maintainer=Marco Palladino, marco@mashape.com
# Wed, 10 Jan 2018 01:27:04 GMT
ENV KONG_VERSION=0.11.2
# Wed, 10 Jan 2018 01:27:04 GMT
ENV KONG_SHA256=10f7f0f5d1bf52afaaf9278f2ef8f7867fec6eb1ce2273ebe6032fa976496011
# Wed, 10 Jan 2018 01:27:17 GMT
RUN apk add --no-cache --virtual .build-deps wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps
# Wed, 10 Jan 2018 01:27:17 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 10 Jan 2018 01:27:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jan 2018 01:27:18 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 10 Jan 2018 01:27:18 GMT
STOPSIGNAL [SIGTERM]
# Wed, 10 Jan 2018 01:27:18 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b03f8754199ad4a2666ff8d835cb1d5ed0261855f7ace9adc6946ab0f732a3d`  
		Last Modified: Wed, 10 Jan 2018 01:28:15 GMT  
		Size: 28.0 MB (28040372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4e0ff8ed8f8845910f93b2df44787de2ffba26e22611b10527b9d45de381cc`  
		Last Modified: Wed, 10 Jan 2018 01:28:10 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.11-alpine`

```console
$ docker pull kong@sha256:0bf9d37aac28aa98336ca8041639512e975d359586334421da20384472d61e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.11-alpine` - linux; amd64

```console
$ docker pull kong@sha256:9aef09089b458ea181f9b87836e814b05cf7da6b722de03ecd96de31a2760d79
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (30032442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaa9cf26b6af4cda25abc86b91f680b0f79122f57467bbcada859b77d8567a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 01:26:18 GMT
LABEL maintainer=Marco Palladino, marco@mashape.com
# Wed, 10 Jan 2018 01:27:04 GMT
ENV KONG_VERSION=0.11.2
# Wed, 10 Jan 2018 01:27:04 GMT
ENV KONG_SHA256=10f7f0f5d1bf52afaaf9278f2ef8f7867fec6eb1ce2273ebe6032fa976496011
# Wed, 10 Jan 2018 01:27:17 GMT
RUN apk add --no-cache --virtual .build-deps wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps
# Wed, 10 Jan 2018 01:27:17 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 10 Jan 2018 01:27:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Jan 2018 01:27:18 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 10 Jan 2018 01:27:18 GMT
STOPSIGNAL [SIGTERM]
# Wed, 10 Jan 2018 01:27:18 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b03f8754199ad4a2666ff8d835cb1d5ed0261855f7ace9adc6946ab0f732a3d`  
		Last Modified: Wed, 10 Jan 2018 01:28:15 GMT  
		Size: 28.0 MB (28040372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4e0ff8ed8f8845910f93b2df44787de2ffba26e22611b10527b9d45de381cc`  
		Last Modified: Wed, 10 Jan 2018 01:28:10 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.12`

```console
$ docker pull kong@sha256:54c1bdd7bde34316adb3178c058654b3ffdba9b94a1cbf2eba16a4d66c6d35d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.12` - linux; amd64

```console
$ docker pull kong@sha256:c6a50deb441727071876c3e02ac0c643c564dbbd2f32b76cc52023b2f9899728
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123480793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a1970f52e686840a1fba4f86bc9612a538fe3c9db5c157eb3021f7afd3b8b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Fri, 06 Apr 2018 21:01:50 GMT
ADD file:f755805244a649eccae3a3e63be291048deeb23e1c5a500d2f92b4eedc452322 in / 
# Fri, 06 Apr 2018 21:01:50 GMT
LABEL org.label-schema.schema-version== 1.0     org.label-schema.name=CentOS Base Image     org.label-schema.vendor=CentOS     org.label-schema.license=GPLv2     org.label-schema.build-date=20180402
# Fri, 06 Apr 2018 21:01:51 GMT
CMD ["/bin/bash"]
# Fri, 06 Apr 2018 22:56:06 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Fri, 06 Apr 2018 23:14:20 GMT
ENV KONG_VERSION=0.12.3
# Fri, 06 Apr 2018 23:17:57 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=centos/7/kong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Fri, 06 Apr 2018 23:17:57 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Fri, 06 Apr 2018 23:17:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Apr 2018 23:17:58 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Fri, 06 Apr 2018 23:17:58 GMT
STOPSIGNAL [SIGTERM]
# Fri, 06 Apr 2018 23:17:59 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:469cfcc7a4b3947a4fa549c68cf4f8570be53779725f0c19f3d33d1520b08db0`  
		Last Modified: Fri, 06 Apr 2018 21:19:02 GMT  
		Size: 73.2 MB (73167580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162958f76c071dfa90da8688167cd054f2cf24302824076c481ce17e1038f48`  
		Last Modified: Fri, 06 Apr 2018 23:20:31 GMT  
		Size: 50.3 MB (50312890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d023d89e842d0aedb45bff4bfc0bcd64650ebe62046138fa722bea156c6e90a3`  
		Last Modified: Fri, 06 Apr 2018 23:20:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.12.3`

```console
$ docker pull kong@sha256:54c1bdd7bde34316adb3178c058654b3ffdba9b94a1cbf2eba16a4d66c6d35d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.12.3` - linux; amd64

```console
$ docker pull kong@sha256:c6a50deb441727071876c3e02ac0c643c564dbbd2f32b76cc52023b2f9899728
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123480793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a1970f52e686840a1fba4f86bc9612a538fe3c9db5c157eb3021f7afd3b8b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Fri, 06 Apr 2018 21:01:50 GMT
ADD file:f755805244a649eccae3a3e63be291048deeb23e1c5a500d2f92b4eedc452322 in / 
# Fri, 06 Apr 2018 21:01:50 GMT
LABEL org.label-schema.schema-version== 1.0     org.label-schema.name=CentOS Base Image     org.label-schema.vendor=CentOS     org.label-schema.license=GPLv2     org.label-schema.build-date=20180402
# Fri, 06 Apr 2018 21:01:51 GMT
CMD ["/bin/bash"]
# Fri, 06 Apr 2018 22:56:06 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Fri, 06 Apr 2018 23:14:20 GMT
ENV KONG_VERSION=0.12.3
# Fri, 06 Apr 2018 23:17:57 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=centos/7/kong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Fri, 06 Apr 2018 23:17:57 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Fri, 06 Apr 2018 23:17:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Apr 2018 23:17:58 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Fri, 06 Apr 2018 23:17:58 GMT
STOPSIGNAL [SIGTERM]
# Fri, 06 Apr 2018 23:17:59 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:469cfcc7a4b3947a4fa549c68cf4f8570be53779725f0c19f3d33d1520b08db0`  
		Last Modified: Fri, 06 Apr 2018 21:19:02 GMT  
		Size: 73.2 MB (73167580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162958f76c071dfa90da8688167cd054f2cf24302824076c481ce17e1038f48`  
		Last Modified: Fri, 06 Apr 2018 23:20:31 GMT  
		Size: 50.3 MB (50312890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d023d89e842d0aedb45bff4bfc0bcd64650ebe62046138fa722bea156c6e90a3`  
		Last Modified: Fri, 06 Apr 2018 23:20:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.12.3-alpine`

```console
$ docker pull kong@sha256:838b012cc9c001eb065e120f159652effdc06887e1f2bfc049d811da1adeafa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.12.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:f16750526362d9e4209ebc3143cb7049d8ef90902da41bd1bb4537796acf79a0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30796479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f3ef766cb665cc8d55ab87bdd219d819b116359026a31238c112b1c1582aea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 01:26:18 GMT
LABEL maintainer=Marco Palladino, marco@mashape.com
# Tue, 13 Mar 2018 00:08:47 GMT
ENV KONG_VERSION=0.12.3
# Tue, 13 Mar 2018 00:08:47 GMT
ENV KONG_SHA256=e7750f4987b7bff485387a0bc95eb51609f7abc5faea76c9598a16f1da023faa
# Tue, 13 Mar 2018 00:08:58 GMT
RUN apk add --no-cache --virtual .build-deps wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps
# Tue, 13 Mar 2018 00:08:59 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Tue, 13 Mar 2018 00:08:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Mar 2018 00:08:59 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Tue, 13 Mar 2018 00:08:59 GMT
STOPSIGNAL [SIGTERM]
# Tue, 13 Mar 2018 00:09:00 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e653a3ca5b95110e88b30ac36b71fc8d8ec8b80b632da09ac8272d9af367aa`  
		Last Modified: Tue, 13 Mar 2018 00:11:17 GMT  
		Size: 28.8 MB (28804407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bc798e333806ac96de0410820a7e624b56b12d4a62002fbedccbf3a8f81506`  
		Last Modified: Tue, 13 Mar 2018 00:11:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.12.3-centos`

```console
$ docker pull kong@sha256:54c1bdd7bde34316adb3178c058654b3ffdba9b94a1cbf2eba16a4d66c6d35d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.12.3-centos` - linux; amd64

```console
$ docker pull kong@sha256:c6a50deb441727071876c3e02ac0c643c564dbbd2f32b76cc52023b2f9899728
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123480793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a1970f52e686840a1fba4f86bc9612a538fe3c9db5c157eb3021f7afd3b8b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Fri, 06 Apr 2018 21:01:50 GMT
ADD file:f755805244a649eccae3a3e63be291048deeb23e1c5a500d2f92b4eedc452322 in / 
# Fri, 06 Apr 2018 21:01:50 GMT
LABEL org.label-schema.schema-version== 1.0     org.label-schema.name=CentOS Base Image     org.label-schema.vendor=CentOS     org.label-schema.license=GPLv2     org.label-schema.build-date=20180402
# Fri, 06 Apr 2018 21:01:51 GMT
CMD ["/bin/bash"]
# Fri, 06 Apr 2018 22:56:06 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Fri, 06 Apr 2018 23:14:20 GMT
ENV KONG_VERSION=0.12.3
# Fri, 06 Apr 2018 23:17:57 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=centos/7/kong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Fri, 06 Apr 2018 23:17:57 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Fri, 06 Apr 2018 23:17:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Apr 2018 23:17:58 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Fri, 06 Apr 2018 23:17:58 GMT
STOPSIGNAL [SIGTERM]
# Fri, 06 Apr 2018 23:17:59 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:469cfcc7a4b3947a4fa549c68cf4f8570be53779725f0c19f3d33d1520b08db0`  
		Last Modified: Fri, 06 Apr 2018 21:19:02 GMT  
		Size: 73.2 MB (73167580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162958f76c071dfa90da8688167cd054f2cf24302824076c481ce17e1038f48`  
		Last Modified: Fri, 06 Apr 2018 23:20:31 GMT  
		Size: 50.3 MB (50312890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d023d89e842d0aedb45bff4bfc0bcd64650ebe62046138fa722bea156c6e90a3`  
		Last Modified: Fri, 06 Apr 2018 23:20:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.12-alpine`

```console
$ docker pull kong@sha256:838b012cc9c001eb065e120f159652effdc06887e1f2bfc049d811da1adeafa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.12-alpine` - linux; amd64

```console
$ docker pull kong@sha256:f16750526362d9e4209ebc3143cb7049d8ef90902da41bd1bb4537796acf79a0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 MB (30796479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f3ef766cb665cc8d55ab87bdd219d819b116359026a31238c112b1c1582aea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 01:26:18 GMT
LABEL maintainer=Marco Palladino, marco@mashape.com
# Tue, 13 Mar 2018 00:08:47 GMT
ENV KONG_VERSION=0.12.3
# Tue, 13 Mar 2018 00:08:47 GMT
ENV KONG_SHA256=e7750f4987b7bff485387a0bc95eb51609f7abc5faea76c9598a16f1da023faa
# Tue, 13 Mar 2018 00:08:58 GMT
RUN apk add --no-cache --virtual .build-deps wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps
# Tue, 13 Mar 2018 00:08:59 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Tue, 13 Mar 2018 00:08:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Mar 2018 00:08:59 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Tue, 13 Mar 2018 00:08:59 GMT
STOPSIGNAL [SIGTERM]
# Tue, 13 Mar 2018 00:09:00 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e653a3ca5b95110e88b30ac36b71fc8d8ec8b80b632da09ac8272d9af367aa`  
		Last Modified: Tue, 13 Mar 2018 00:11:17 GMT  
		Size: 28.8 MB (28804407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bc798e333806ac96de0410820a7e624b56b12d4a62002fbedccbf3a8f81506`  
		Last Modified: Tue, 13 Mar 2018 00:11:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.12-centos`

```console
$ docker pull kong@sha256:54c1bdd7bde34316adb3178c058654b3ffdba9b94a1cbf2eba16a4d66c6d35d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.12-centos` - linux; amd64

```console
$ docker pull kong@sha256:c6a50deb441727071876c3e02ac0c643c564dbbd2f32b76cc52023b2f9899728
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123480793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a1970f52e686840a1fba4f86bc9612a538fe3c9db5c157eb3021f7afd3b8b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Fri, 06 Apr 2018 21:01:50 GMT
ADD file:f755805244a649eccae3a3e63be291048deeb23e1c5a500d2f92b4eedc452322 in / 
# Fri, 06 Apr 2018 21:01:50 GMT
LABEL org.label-schema.schema-version== 1.0     org.label-schema.name=CentOS Base Image     org.label-schema.vendor=CentOS     org.label-schema.license=GPLv2     org.label-schema.build-date=20180402
# Fri, 06 Apr 2018 21:01:51 GMT
CMD ["/bin/bash"]
# Fri, 06 Apr 2018 22:56:06 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Fri, 06 Apr 2018 23:14:20 GMT
ENV KONG_VERSION=0.12.3
# Fri, 06 Apr 2018 23:17:57 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=centos/7/kong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Fri, 06 Apr 2018 23:17:57 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Fri, 06 Apr 2018 23:17:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Apr 2018 23:17:58 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Fri, 06 Apr 2018 23:17:58 GMT
STOPSIGNAL [SIGTERM]
# Fri, 06 Apr 2018 23:17:59 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:469cfcc7a4b3947a4fa549c68cf4f8570be53779725f0c19f3d33d1520b08db0`  
		Last Modified: Fri, 06 Apr 2018 21:19:02 GMT  
		Size: 73.2 MB (73167580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9162958f76c071dfa90da8688167cd054f2cf24302824076c481ce17e1038f48`  
		Last Modified: Fri, 06 Apr 2018 23:20:31 GMT  
		Size: 50.3 MB (50312890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d023d89e842d0aedb45bff4bfc0bcd64650ebe62046138fa722bea156c6e90a3`  
		Last Modified: Fri, 06 Apr 2018 23:20:24 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.13`

```console
$ docker pull kong@sha256:625281350f36a6cd4a0986a56f119273664740e1ffa5bc056c257f4a10f2dff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.13` - linux; amd64

```console
$ docker pull kong@sha256:19c74f52023caeb4a396186744c1538ec51122bf8183ade252a66f74f4e799ad
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33373706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dbcf499414ac8d76c75c8843d726018bc964d07b4fd386a5038435dab5dfb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 01:26:18 GMT
LABEL maintainer=Marco Palladino, marco@mashape.com
# Wed, 25 Apr 2018 20:28:00 GMT
ENV KONG_VERSION=0.13.1
# Wed, 25 Apr 2018 20:28:01 GMT
ENV KONG_SHA256=caf119ce7a367b9d9cd1ace55c4b6a499ff3c4693f80ea25129ebf2da0373fcc
# Wed, 25 Apr 2018 20:28:13 GMT
RUN apk add --no-cache --virtual .build-deps wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata curl 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps
# Wed, 25 Apr 2018 20:28:13 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 25 Apr 2018 20:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Apr 2018 20:28:14 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 25 Apr 2018 20:28:14 GMT
STOPSIGNAL [SIGTERM]
# Wed, 25 Apr 2018 20:28:15 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48d98b461a894e8e34ae6e02823f600aa4aafedc2208c8b99fb88d806c1911a`  
		Last Modified: Wed, 25 Apr 2018 20:30:31 GMT  
		Size: 31.4 MB (31381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae397bafae3c36fbbea4f1de87ef6bb81a0e0f7173b0f4f94f67718e00dd786`  
		Last Modified: Wed, 25 Apr 2018 20:30:25 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.13.1`

```console
$ docker pull kong@sha256:625281350f36a6cd4a0986a56f119273664740e1ffa5bc056c257f4a10f2dff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.13.1` - linux; amd64

```console
$ docker pull kong@sha256:19c74f52023caeb4a396186744c1538ec51122bf8183ade252a66f74f4e799ad
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33373706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dbcf499414ac8d76c75c8843d726018bc964d07b4fd386a5038435dab5dfb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 01:26:18 GMT
LABEL maintainer=Marco Palladino, marco@mashape.com
# Wed, 25 Apr 2018 20:28:00 GMT
ENV KONG_VERSION=0.13.1
# Wed, 25 Apr 2018 20:28:01 GMT
ENV KONG_SHA256=caf119ce7a367b9d9cd1ace55c4b6a499ff3c4693f80ea25129ebf2da0373fcc
# Wed, 25 Apr 2018 20:28:13 GMT
RUN apk add --no-cache --virtual .build-deps wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata curl 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps
# Wed, 25 Apr 2018 20:28:13 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 25 Apr 2018 20:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Apr 2018 20:28:14 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 25 Apr 2018 20:28:14 GMT
STOPSIGNAL [SIGTERM]
# Wed, 25 Apr 2018 20:28:15 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48d98b461a894e8e34ae6e02823f600aa4aafedc2208c8b99fb88d806c1911a`  
		Last Modified: Wed, 25 Apr 2018 20:30:31 GMT  
		Size: 31.4 MB (31381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae397bafae3c36fbbea4f1de87ef6bb81a0e0f7173b0f4f94f67718e00dd786`  
		Last Modified: Wed, 25 Apr 2018 20:30:25 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.13.1-alpine`

```console
$ docker pull kong@sha256:625281350f36a6cd4a0986a56f119273664740e1ffa5bc056c257f4a10f2dff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.13.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:19c74f52023caeb4a396186744c1538ec51122bf8183ade252a66f74f4e799ad
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33373706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dbcf499414ac8d76c75c8843d726018bc964d07b4fd386a5038435dab5dfb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 01:26:18 GMT
LABEL maintainer=Marco Palladino, marco@mashape.com
# Wed, 25 Apr 2018 20:28:00 GMT
ENV KONG_VERSION=0.13.1
# Wed, 25 Apr 2018 20:28:01 GMT
ENV KONG_SHA256=caf119ce7a367b9d9cd1ace55c4b6a499ff3c4693f80ea25129ebf2da0373fcc
# Wed, 25 Apr 2018 20:28:13 GMT
RUN apk add --no-cache --virtual .build-deps wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata curl 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps
# Wed, 25 Apr 2018 20:28:13 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 25 Apr 2018 20:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Apr 2018 20:28:14 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 25 Apr 2018 20:28:14 GMT
STOPSIGNAL [SIGTERM]
# Wed, 25 Apr 2018 20:28:15 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48d98b461a894e8e34ae6e02823f600aa4aafedc2208c8b99fb88d806c1911a`  
		Last Modified: Wed, 25 Apr 2018 20:30:31 GMT  
		Size: 31.4 MB (31381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae397bafae3c36fbbea4f1de87ef6bb81a0e0f7173b0f4f94f67718e00dd786`  
		Last Modified: Wed, 25 Apr 2018 20:30:25 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.13.1-centos`

```console
$ docker pull kong@sha256:edac0478c25552a9bb860e1bd8e6fc08272fdf65cf5ca61cfd9c41eed894279d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.13.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:fe41e857c0def0d09f00909a18242bf07b0f08296b9e4ad6bf5744bcf8c0e937
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126452680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6aa0652e34d6cec7c5450eeb65f73b2840a976eb19f49cacc2a20591c17e09b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Fri, 06 Apr 2018 21:01:50 GMT
ADD file:f755805244a649eccae3a3e63be291048deeb23e1c5a500d2f92b4eedc452322 in / 
# Fri, 06 Apr 2018 21:01:50 GMT
LABEL org.label-schema.schema-version== 1.0     org.label-schema.name=CentOS Base Image     org.label-schema.vendor=CentOS     org.label-schema.license=GPLv2     org.label-schema.build-date=20180402
# Fri, 06 Apr 2018 21:01:51 GMT
CMD ["/bin/bash"]
# Fri, 06 Apr 2018 22:56:06 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 25 Apr 2018 20:28:35 GMT
ENV KONG_VERSION=0.13.1
# Wed, 25 Apr 2018 20:29:39 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=centos/7/kong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 25 Apr 2018 20:29:40 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 25 Apr 2018 20:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Apr 2018 20:29:41 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 25 Apr 2018 20:29:41 GMT
STOPSIGNAL [SIGTERM]
# Wed, 25 Apr 2018 20:29:41 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:469cfcc7a4b3947a4fa549c68cf4f8570be53779725f0c19f3d33d1520b08db0`  
		Last Modified: Fri, 06 Apr 2018 21:19:02 GMT  
		Size: 73.2 MB (73167580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed724412946befa09137058f16ffe397e6c4d861f8613d26e43eaa1f0c9d98fb`  
		Last Modified: Wed, 25 Apr 2018 20:32:08 GMT  
		Size: 53.3 MB (53284779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb28156789d440abfe444ce805ab26b7e43efff49b549586f7839cc5dc45e77`  
		Last Modified: Wed, 25 Apr 2018 20:32:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:0.13-centos`

```console
$ docker pull kong@sha256:edac0478c25552a9bb860e1bd8e6fc08272fdf65cf5ca61cfd9c41eed894279d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:0.13-centos` - linux; amd64

```console
$ docker pull kong@sha256:fe41e857c0def0d09f00909a18242bf07b0f08296b9e4ad6bf5744bcf8c0e937
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126452680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6aa0652e34d6cec7c5450eeb65f73b2840a976eb19f49cacc2a20591c17e09b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Fri, 06 Apr 2018 21:01:50 GMT
ADD file:f755805244a649eccae3a3e63be291048deeb23e1c5a500d2f92b4eedc452322 in / 
# Fri, 06 Apr 2018 21:01:50 GMT
LABEL org.label-schema.schema-version== 1.0     org.label-schema.name=CentOS Base Image     org.label-schema.vendor=CentOS     org.label-schema.license=GPLv2     org.label-schema.build-date=20180402
# Fri, 06 Apr 2018 21:01:51 GMT
CMD ["/bin/bash"]
# Fri, 06 Apr 2018 22:56:06 GMT
MAINTAINER Marco Palladino, marco@mashape.com
# Wed, 25 Apr 2018 20:28:35 GMT
ENV KONG_VERSION=0.13.1
# Wed, 25 Apr 2018 20:29:39 GMT
RUN yum install -y wget https://bintray.com/kong/kong-community-edition-rpm/download_file?file_path=centos/7/kong-community-edition-$KONG_VERSION.el7.noarch.rpm &&     yum clean all
# Wed, 25 Apr 2018 20:29:40 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 25 Apr 2018 20:29:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Apr 2018 20:29:41 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 25 Apr 2018 20:29:41 GMT
STOPSIGNAL [SIGTERM]
# Wed, 25 Apr 2018 20:29:41 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:469cfcc7a4b3947a4fa549c68cf4f8570be53779725f0c19f3d33d1520b08db0`  
		Last Modified: Fri, 06 Apr 2018 21:19:02 GMT  
		Size: 73.2 MB (73167580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed724412946befa09137058f16ffe397e6c4d861f8613d26e43eaa1f0c9d98fb`  
		Last Modified: Wed, 25 Apr 2018 20:32:08 GMT  
		Size: 53.3 MB (53284779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb28156789d440abfe444ce805ab26b7e43efff49b549586f7839cc5dc45e77`  
		Last Modified: Wed, 25 Apr 2018 20:32:01 GMT  
		Size: 321.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:625281350f36a6cd4a0986a56f119273664740e1ffa5bc056c257f4a10f2dff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:19c74f52023caeb4a396186744c1538ec51122bf8183ade252a66f74f4e799ad
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33373706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9dbcf499414ac8d76c75c8843d726018bc964d07b4fd386a5038435dab5dfb9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["\/usr\/local\/openresty\/nginx\/sbin\/nginx","-c","\/usr\/local\/kong\/nginx.conf","-p","\/usr\/local\/kong\/"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:38 GMT
ADD file:6edc55fb54ec9fc3658c8f5176a70e792103a516154442f94fed8e0290e4960e in / 
# Tue, 09 Jan 2018 21:10:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 01:26:18 GMT
LABEL maintainer=Marco Palladino, marco@mashape.com
# Wed, 25 Apr 2018 20:28:00 GMT
ENV KONG_VERSION=0.13.1
# Wed, 25 Apr 2018 20:28:01 GMT
ENV KONG_SHA256=caf119ce7a367b9d9cd1ace55c4b6a499ff3c4693f80ea25129ebf2da0373fcc
# Wed, 25 Apr 2018 20:28:13 GMT
RUN apk add --no-cache --virtual .build-deps wget tar ca-certificates 	&& apk add --no-cache libgcc openssl pcre perl tzdata curl 	&& wget -O kong.tar.gz "https://bintray.com/kong/kong-community-edition-alpine-tar/download_file?file_path=kong-community-edition-$KONG_VERSION.apk.tar.gz" 	&& echo "$KONG_SHA256 *kong.tar.gz" | sha256sum -c - 	&& tar -xzf kong.tar.gz -C /tmp 	&& rm -f kong.tar.gz 	&& cp -R /tmp/usr / 	&& rm -rf /tmp/usr 	&& cp -R /tmp/etc / 	&& rm -rf /tmp/etc 	&& apk del .build-deps
# Wed, 25 Apr 2018 20:28:13 GMT
COPY file:0ce55305f95ddcb78ffb96b9502c795c4dd1040025f4ec7c3e19e4b889022b90 in /docker-entrypoint.sh 
# Wed, 25 Apr 2018 20:28:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Apr 2018 20:28:14 GMT
EXPOSE 8000/tcp 8001/tcp 8443/tcp 8444/tcp
# Wed, 25 Apr 2018 20:28:14 GMT
STOPSIGNAL [SIGTERM]
# Wed, 25 Apr 2018 20:28:15 GMT
CMD ["/usr/local/openresty/nginx/sbin/nginx" "-c" "/usr/local/kong/nginx.conf" "-p" "/usr/local/kong/"]
```

-	Layers:
	-	`sha256:605ce1bd3f3164f2949a30501cc596f52a72de05da1306ab360055f0d7130c32`  
		Last Modified: Tue, 09 Jan 2018 21:13:17 GMT  
		Size: 2.0 MB (1991747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48d98b461a894e8e34ae6e02823f600aa4aafedc2208c8b99fb88d806c1911a`  
		Last Modified: Wed, 25 Apr 2018 20:30:31 GMT  
		Size: 31.4 MB (31381636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae397bafae3c36fbbea4f1de87ef6bb81a0e0f7173b0f4f94f67718e00dd786`  
		Last Modified: Wed, 25 Apr 2018 20:30:25 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
