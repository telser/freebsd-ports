# Created by: Olivier Duchateau
# $FreeBSD$

PORTNAME=	liblxqt
PORTVERSION=	0.13.0
CATEGORIES=	devel
MASTER_SITES=	LXQT

MAINTAINER=	jesper@schmitz.computer
COMMENT=	Shared library for LXQt applications

LICENSE=	LGPL21+
LIB_DEPENDS=	libpolkit-qt5-core-1.so:sysutils/polkit-qt@qt5

BROKEN_aarch64=		fails to compile: lxqtplugininfo.cpp:107:14: expected expression

USES=	cmake:outsource compiler:c++11-lib gettext kde:5 lxqt \
	pkgconfig tar:xz
USE_QT5=	buildtools_build qmake_build dbus core gui linguisttools \
	svg widgets x11extras xml
USE_KDE=	windowsystem
USE_LXQT=	buildtools qtxdg
USE_XORG=	x11 xscrnsaver

.include <bsd.port.mk>
