# Created by: Yuri Victorovich <yuri@rawbw.com>
# $FreeBSD$

PORTNAME=	emptyepsilon
DISTVERSIONPREFIX=	EE-
DISTVERSION=	2019.05.21
CATEGORIES=	games

PATCH_SITES=	https://github.com/${GH_ACCOUNT}/${GH_PROJECT}/commit/
PATCHFILES=	bbdf350f103a0b680f2053c94d8e91403260357e.patch:-p1

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Spaceship bridge simulator game

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libsfml-system.so:devel/sfml

USES=		cmake compiler:c++11-lib gl
USE_GITHUB=	yes
GH_ACCOUNT=	daid
GH_PROJECT=	EmptyEpsilon SeriousProton:sproton
USE_GL=		gl glu
CMAKE_ARGS=	-DSERIOUS_PROTON_DIR="${WRKSRC_sproton}/"

post-patch:
	@${REINPLACE_CMD} -e 's|basepath + |"${DATADIR}/" + basepath + |' \
		${WRKSRC_sproton}/src/resources.cpp
	@${REINPLACE_CMD} -e 's|loadFromFile("resources/"|loadFromFile("${DATADIR}/resources/"|' \
		${WRKSRC_sproton}/src/postProcessManager.cpp

post-install:
	@${MV} ${STAGEDIR}${PREFIX}/bin/EmptyEpsilon ${STAGEDIR}${PREFIX}/bin/emptyepsilon

.include <bsd.port.mk>
