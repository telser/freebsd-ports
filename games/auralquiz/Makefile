# Created by: Dmitry Marakasov <amdmi3@FreeBSD.org>
# $FreeBSD$

PORTNAME=	auralquiz
PORTVERSION=	1.0.0
DISTVERSIONPREFIX=	v
PORTREVISION=	1
CATEGORIES=	games
MASTER_SITES=	SAVANNAH

MAINTAINER=	amdmi3@FreeBSD.org
COMMENT=	Simple music quiz game using your own music files

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libtag.so:audio/taglib

USES=		qmake
USE_GL=		gl
USE_QT5=	core gui widgets phonon4 qmake_build buildtools_build

PORTDOCS=	CHANGELOG README TODO

OPTIONS_DEFINE=	DOCS

post-patch:
	@${REINPLACE_CMD} -e 's|%%PREFIX%%|${PREFIX}|; \
		s|%%MAN6PREFIX%%|${MAN6PREFIX}|' \
		${WRKSRC}/Auralquiz.pro

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
.for f in ${PORTDOCS}
	${INSTALL_DATA} ${WRKSRC}/${f} ${STAGEDIR}${DOCSDIR}/
.endfor

.include <bsd.port.mk>
