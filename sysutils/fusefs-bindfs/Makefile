PORTNAME=	bindfs
DISTVERSION=	1.17.6
PORTREVISION=	1
CATEGORIES=	sysutils
MASTER_SITES=	https://bindfs.org/downloads/
PKGNAMEPREFIX=	fusefs-

MAINTAINER=	doralitze@chaotikum.org
COMMENT=	FUSE based bindfs implementation way more powerful than nullfs
WWW=		https://bindfs.org/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		fuse:3 localbase:ldflags pkgconfig
GNU_CONFIGURE=	yes
GNU_CONFIGURE_MANPREFIX=	${PREFIX}/share

PLIST_FILES=	bin/bindfs \
		share/man/man1/bindfs.1.gz

.include <bsd.port.pre.mk>

.if ${LIBFUSE_VER} == 3
FUSEPKG=	fuse3
CONFIGURE_ENV+=	FUSE_CFLAGS="-I${LOCALBASE}/include/fuse3" \
		FUSE_LIBS="-L${LOCALBASE}/lib -lfuse3"
LDFLAGS+=	-lthr
.endif

FUSE_VERSION=	"`pkgconf --modversion ${FUSEPKG} | \
		${SED} -E 's,^([0-9]+)\.([0-9]+)\..*,\1\2,'`"

.include <bsd.port.post.mk>
