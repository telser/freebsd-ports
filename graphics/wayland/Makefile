# Created by: kwm@FreeBSD.org
# $FreeBSD$

PORTNAME=	wayland
PORTVERSION=	1.14.0
CATEGORIES=	graphics wayland
MASTER_SITES=	http://wayland.freedesktop.org/releases/

MAINTAINER=	x11@FreeBSD.org
COMMENT=	Wayland composite "server"

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

BROKEN_powerpc64=	fails to compile: tests/test-runner.c:349: undefined reference to prctl

LIB_DEPENDS=	libexpat.so:textproc/expat2 \
		libffi.so:devel/libffi \
		libepoll-shim.so:devel/libepoll-shim

CFLAGS+=	"-I${LOCALBASE}/include/libepoll-shim"

WITH_DEBUG=	1

USES=		autoreconf gmake libtool localbase pathfix pkgconfig tar:xz
USE_GNOME=	libxslt:build
USE_LDCONFIG=	yes
GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--disable-documentation
CONFIGURE_ENV=	ac_cv_func_posix_fallocate=no # EINVAL for many FS on 12.0
INSTALL_TARGET=	install-strip

.include <bsd.port.mk>
