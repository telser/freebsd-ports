# Created by: alonso@
# $FreeBSD$

PORTNAME=	libkscreen
PORTVERSION=	1.0.5
PORTREVISION=	5
CATEGORIES=	graphics kde
MASTER_SITES=	KDE/stable/${PORTNAME}/${PORTVERSION}/src

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KDE screen management library

LIB_DEPENDS=	libqjson.so:devel/qjson@qt4 \
		libxcb.so:x11/libxcb \
		libxcb-image.so:x11/xcb-util-image \
		libxcb-render-util.so:x11/xcb-util-renderutil

USES=		cmake:outsource kde:4 pkgconfig tar:xz
USE_KDE=	kdelibs automoc4
USE_QT4=	corelib dbus gui script \
		moc_build qmake_build rcc_build uic_build
USE_LDCONFIG=	yes

PLIST_SUB+=	PORTVERSION="${PORTVERSION}"

pre-configure:
	${REINPLACE_CMD} -e 's,$${LIB_INSTALL_DIR}/pkgconfig,libdata/pkgconfig,' \
		${WRKSRC}/src/CMakeLists.txt

.include <bsd.port.mk>
