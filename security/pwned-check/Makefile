PORTNAME=	pwned-check
PORTVERSION=	2.2
PORTREVISION=	2
PORTEPOCH=	1
CATEGORIES=	security
MASTER_SITES=	#
DISTFILES=	#

MAINTAINER=	se@FreeBSD.org
COMMENT=	Check whether password is known to have been exposed in a data breach
WWW=		https://haveibeenpwned.com/

LICENSE=	BSD2CLAUSE

SUB_FILES=	pkg-message
SUB_LIST=	PORTNAME=${PORTNAME}

NO_ARCH=	yes
NO_BUILD=	yes
WRKSRC=		${WRKDIR}/src

SRC=		${.CURDIR}/src

SUB_FILES=	${PORTNAME}.sh ${PORTNAME}.1 pkg-message

do-install:
	${INSTALL_SCRIPT} ${WRKDIR}/${PORTNAME}.sh ${STAGEDIR}${PREFIX}/bin/${PORTNAME}
	${INSTALL_DATA} ${FILESDIR}/${PORTNAME}.conf.sample ${STAGEDIR}${PREFIX}/etc
	${INSTALL_MAN} ${WRKDIR}/${PORTNAME}.1 ${STAGEDIR}${PREFIX}/share/man/man1
	${MKDIR} ${STAGEDIR}/var/db/${PORTNAME}

.include <bsd.port.mk>
