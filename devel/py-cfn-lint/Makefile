# $FreeBSD$

PORTNAME=	cfn-lint
PORTVERSION=	0.21.5
CATEGORIES=	devel python textproc
MASTER_SITES=	CHEESESHOP
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	nork@ninth-nine.com
COMMENT=	AWS CloudFormation Linter

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}yaml>0:devel/py-yaml@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}six>=1.11:devel/py-six@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}requests>=2.15.0:www/py-requests@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}aws-sam-translator>=1.10.0:devel/py-aws-sam-translator@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}jsonpatch>0:devel/py-jsonpatch@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}jsonschema>=3.0:devel/py-jsonschema@${PY_FLAVOR} \
		${PY_PATHLIB}

USES=		python
USE_PYTHON=	autoplist concurrent distutils

NO_ARCH=	yes

.include <bsd.port.mk>
