# $FreeBSD$

PORTNAME=	kollision
DISTVERSION=	${KDE_APPLICATIONS_VERSION}
PORTREVISION=	1
CATEGORIES=	games kde kde-applications

MAINTAINER=	kde@FreeBSD.org
COMMENT=	${${PORTNAME}_DESC}

USES=		cmake:outsource gettext kde:5 tar:xz
USE_KDE=	auth codecs config configwidgets coreaddons crash dbusaddons \
		ecm i18n kio libkdegames newstuff notifyconfig textwidgets \
		widgetsaddons xmlgui
USE_QT5=	core dbus gui network phonon4 qml quick svg widgets xml \
		buildtools_build qmake_build

.include <${.CURDIR}/../kdegames/Makefile.common>
.include <bsd.port.mk>
