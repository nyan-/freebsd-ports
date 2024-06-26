PORTNAME=	mairix
DISTVERSION=	0.24
PORTREVISION=	1
CATEGORIES=	mail

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Indexing and searching in Maildir, MH, or mbox folders
WWW=		http://www.rc0.org.uk/mairix/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		bison compiler:c11 gmake ssl
USE_GITHUB=	yes
GH_ACCOUNT=	vandry

CONFIGURE_ARGS=	--prefix=${PREFIX} --mandir=${PREFIX}/share/man
HAS_CONFIGURE=	yes
PLIST_FILES=	bin/mairix \
		share/man/man1/mairix.1.gz \
		share/man/man5/mairixrc.5.gz

OPTIONS_DEFINE=	GZIP BZIP2 EXAMPLES DOCS
GZIP_DESC=	gzip compressed mbox support
BZIP2_DESC=	bzip2 compressed mbox support

GZIP_CONFIGURE_ENABLE=	gzip-mbox
BZIP2_CONFIGURE_ENABLE=	bzip-mbox

PORTDOCS=	NEWS README
PORTEXAMPLES=	dotmairixrc.eg

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/mairix
	@${MKDIR} ${STAGEDIR}/${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/NEWS ${WRKSRC}/README ${STAGEDIR}/${DOCSDIR}
	@${MKDIR} ${STAGEDIR}/${EXAMPLESDIR}
	${INSTALL_DATA} ${WRKSRC}/dotmairixrc.eg ${STAGEDIR}/${EXAMPLESDIR}

.include <bsd.port.mk>
