# $FreeBSD$

PORTNAME=	plasma-sdk
DISTVERSION=	${KDE_PLASMA_VERSION}
CATEGORIES=	devel kde kde-plasma

MAINTAINER=	kde@FreeBSD.org
COMMENT=	Plasma5 applications useful for Plasma development

USES=		cmake:outsource compiler:c++11-lib cpe gettext kde:5 tar:xz
USE_KDE=	archive attica auth codecs completion config configwidgets \
		coreaddons dbusaddons ecm i18n iconthemes itemmodels \
		jobwidgets kdeclarative kio kirigami2 newstuff package parts \
		plasma-framework service sonnet texteditor textwidgets \
		widgetsaddons windowsystem xmlgui
USE_QT5=	concurrent core dbus gui network qml quick webkit widgets x11extras xml \
		buildtools_build qmake_build

.include <bsd.port.mk>
