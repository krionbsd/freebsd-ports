# $FreeBSD$

PORTNAME=	jasper
PORTVERSION=	1.900.1
DISTVERSIONSUFFIX=	-22.el6
PORTREVISION=	5
CATEGORIES=	graphics linux
PKGNAMESUFFIX=	-libs

MAINTAINER=	emulation@FreeBSD.org
COMMENT=	JPEG-2000 reference implementation (Linux CentOS ${LINUX_DIST_VER})

USES=		linux:c6
USE_LDCONFIG=	yes
USE_LINUX=	jpeg
USE_LINUX_RPM=	yes

LIB_DISTNAMES=	${PORTNAME}${PKGNAMESUFFIX}-${DISTVERSIONFULL}

DESCR=		${.CURDIR}/../${PORTNAME}/pkg-descr

.include <bsd.port.mk>
