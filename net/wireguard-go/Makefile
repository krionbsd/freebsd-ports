# $FreeBSD$

PORTNAME=	wireguard-go
PORTVERSION=	0.0.20190517
CATEGORIES=	net
MASTER_SITES=	https://git.zx2c4.com/wireguard-go/snapshot/
DISTFILES=	${PORTNAME}-${PORTVERSION}${EXTRACT_SUFX}

MAINTAINER=	decke@FreeBSD.org
COMMENT=	WireGuard implementation in Go

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		gmake go:modules,no_targets tar:xz

USE_GITHUB=	nodefault
GH_TUPLE=	golang:crypto:b7391e95e576:crypto/vendor/golang.org/x/crypto \
		golang:net:1272bf9dcd53:net/vendor/golang.org/x/net \
		golang:sys:f7bb7a8bee54:sys/vendor/golang.org/x/sys

MAKE_ENV+=	GOFLAGS="${GO_BUILDFLAGS}"

PLIST_FILES=	bin/${PORTNAME}

.include <bsd.port.mk>
