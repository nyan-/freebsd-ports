PORTNAME=		liblug
PORTVERSION=		1.0.6
PORTREVISION=		5
CATEGORIES=		graphics
MASTER_SITES=		SUNSITE/libs/graphics

MAINTAINER=		bofh@FreeBSD.org
COMMENT=		Multi-format graphics manipulation library

LICENSE=		LGPL20
LICENSE_FILE=	${WRKSRC}/LICENSE

DEPRECATED=	SUNSITE is no longer maintained
EXPIRATION_DATE=2024-04-05

LIB_DEPENDS=		libtiff.so:graphics/tiff

USES=			xorg
USE_LDCONFIG=		yes
USE_XORG=		x11

MAKEFILE=		Makefile.linux

CFLAGS+=		-Wno-return-type

WRKSRC=			${WRKDIR}/lug

PLIST_FILES=		lib/liblug.a

.include <bsd.port.pre.mk>

.if ${OPSYS} == FreeBSD && ( ${OSVERSION} >= 1400079 || ( ${OSVERSION} >= 1302505 && ${OSVERSION} < 1400000 ))
CFLAGS+=	-Wno-error=int-conversion
.endif

post-patch:
	@${REINPLACE_CMD} -e 's|-DiTIFF|-DiTIFF -DTIFF_VERSION=TIFF_VERSION_CLASSIC|' \
		${WRKSRC}/Makefile.linux

.include <bsd.port.post.mk>
