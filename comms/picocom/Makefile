PORTNAME=	picocom
DISTVERSION=	3.1
PORTREVISION=	1
CATEGORIES=	comms

MAINTAINER=	rmm1.bob@gmail.com
COMMENT=	Dumb Terminal Emulator
WWW=		https://github.com/npat-efault/picocom

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

USES=		cpe
CPE_VENDOR=	${PORTNAME}_project
USE_GITHUB=	yes
GH_ACCOUNT=	npat-efault

PLIST_FILES=	bin/picocom share/man/man1/picocom.1.gz

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/${PORTNAME}.1 ${STAGEDIR}${PREFIX}/share/man/man1

.include <bsd.port.mk>
