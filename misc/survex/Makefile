# $FreeBSD$

PORTNAME=	survex
DISTVERSION=	1.2.38
PORTREVISION=	1
CATEGORIES=	misc
MASTER_SITES=	https://survex.com/software/${DISTVERSION}/

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Cave survey software

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

DEPRECATED=	Can not build with graphics/proj
EXPIRATION_DATE=2019-09-27

LIB_DEPENDS=	libavcodec.so:multimedia/ffmpeg \
		libproj.so:graphics/proj5

USES=		compiler:c++11-lang desktop-file-utils gl gmake gnome pkgconfig shared-mime-info
GNU_CONFIGURE=	yes
USE_WX=		3.0
USE_XORG=	xxf86vm
USE_GL=		gl glu
INSTALLS_ICONS=	yes # because wxWidgets-3.0 is gtk/gnome based

MAKE_ENV=	WX_CONFIG=${WX_CONFIG}

OPTIONS_DEFINE=	DOCS

PORTDOCS=	*

.include <bsd.port.mk>
