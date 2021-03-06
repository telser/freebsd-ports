# $FreeBSD$

PORTNAME=	kmail
DISTVERSION=	${KDE_APPLICATIONS_VERSION}
CATEGORIES=	deskutils kde kde-applications

MAINTAINER=	kde@FreeBSD.org
COMMENT=	KDE mail client

LICENSE=	LGPL21

LIB_DEPENDS=	libassuan.so:security/libassuan \
		libgpg-error.so:security/libgpg-error \
		libgpgme.so:security/gpgme \
		libgpgmepp.so:security/gpgme-cpp \
		libqgpgme.so:security/gpgme-qt5

RUN_DEPENDS=	accountwizard:deskutils/kmail-account-wizard \
		akonadiimportwizard:deskutils/akonadi-import-wizard \
		mboximporter:deskutils/mbox-importer \
		sieveeditor:deskutils/pim-sieve-editor

USES=		cmake:outsource compiler:c++11-lib gettext kde:5 tar:xz
USE_KDE=	auth bookmarks codecs completion config configwidgets \
		coreaddons crash dbusaddons ecm guiaddons i18n iconthemes \
		itemmodels itemviews jobwidgets kcmutils kdelibs4support kio \
		notifications notifyconfig parts service solid sonnet \
		syntaxhighlighting texteditor textwidgets unitconversion wallet \
		widgetsaddons windowsystem xmlgui
# pim components
USE_KDE+=	akonadi akonadicontacts akonadimime akonadisearch calendarcore \
		calendarutils contacts gravatar kdepim-apps-libs \
		identitymanagement libkdepim libkleo libksieve \
		kontactinterface ldap mailcommon mailtransport messagelib \
		mime pimcommon pimtextedit tnef
USE_QT5=	core dbus gui location network printsupport qml quick \
		webchannel webengine widgets xml \
		buildtools_build qmake_build
USE_LDCONFIG=	yes

DESCR=		${.CURDIR:H:H}/deskutils/kdepim/pkg-descr


.include <bsd.port.mk>
