# Created by: J.R. Oldroyd <fbsd@opal.com>
# $FreeBSD$

PORTNAME=	kaa-base
PORTVERSION=	0.6.0
PORTREVISION=	10
CATEGORIES=	multimedia python
MASTER_SITES=	SF/freevo/${PORTNAME}/${PORTVERSION}
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	fbsd@opal.com
COMMENT=	Kaa Media Repository

BUILD_DEPENDS=	${PYTHON_SITELIBDIR}/libxml2.py:textproc/py-libxml2@${PY_FLAVOR} \
		${PYTHON_SITELIBDIR}/pygame/__init__.py:devel/py-game@${PY_FLAVOR}
RUN_DEPENDS:=	${BUILD_DEPENDS}

USES=		python:2.7
USE_GNOME=	glib20
USE_PYTHON=	distutils autoplist
CFLAGS+=	-D_WANT_SEMUN

.include <bsd.port.mk>
