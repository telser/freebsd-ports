# $FreeBSD$

PORTNAME=	SoapySDR
DISTVERSIONPREFIX=	soapy-sdr-
DISTVERSION=	0.6.1-71
DISTVERSIONSUFFIX=	-g69c16e9
CATEGORIES=	misc python 
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Vendor and platform neutral SDR support library (python binding)

LICENSE=	BSL
LICENSE_FILE=	${WRKSRC}/LICENSE_1_0.txt

BROKEN_FreeBSD_10=	error: redefinition of 'swig::traits<unsigned int>'

BUILD_DEPENDS=	swig3.0:devel/swig30
LIB_DEPENDS=	libSoapySDR.so:misc/soapysdr

USES=		cmake:outsource python
USE_GITHUB=	yes
GH_ACCOUNT=	pothosware
USE_PYTHON=	flavors

CMAKE_ARGS=	-DFREEBSD_PYTHON_VERSION:INTEGER=${PYTHON_VER:S/.//} \
		-DFREEBSD_PYTHON_VER2:STRING=${PYTHON_VER}
CMAKE_OFF=	ENABLE_DOCS

PLIST_FILES=	${PYTHON_SITELIBDIR}/SoapySDR.py \
		${PYTHON_SITELIBDIR}/_SoapySDR.so

post-install: # Until fixed, just delete libs: https://github.com/pothosware/SoapySDR/issues/169
	@cd ${STAGEDIR}${PREFIX} && ${RM} -r bin include lib/lib* libdata share

.include <bsd.port.mk>
