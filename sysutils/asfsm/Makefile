PORTNAME=	asfsm
DISTVERSION=	1.0pre15
PORTREVISION=	4
CATEGORIES=	sysutils afterstep
MASTER_SITES=	http://tigr.net/afterstep/download/asfsm/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	File-system monitor for the AfterStep window manager

LICENSE=	GPLv2

USES=		xorg
USE_XORG=	ice sm x11 xaw xext xpm xt
GNU_CONFIGURE=	yes

SUB_FILES=	pkg-message

PLIST_FILES=	bin/asfsm share/man/man1/asfsm.1.gz

post-build:
	@${LN} -sf asfsm.man ${WRKSRC}/asfsm.1

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/asfsm ${STAGEDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/asfsm.man ${STAGEDIR}${PREFIX}/share/man/man1/asfsm.1

.include <bsd.port.mk>
