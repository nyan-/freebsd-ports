PORTNAME=	osv-scanner
DISTVERSIONPREFIX=	v
DISTVERSION=	1.6.1
PORTREVISION=	2
CATEGORIES=	security

MAINTAINER=	lcook@FreeBSD.org
COMMENT=	Vulnerability scanner written in Go which uses the OSV database
WWW=		https://github.com/google/osv-scanner

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:1.21,modules

_BUILD_VERSION=	${DISTVERSION}
_BUILD_COMMIT=	f6b0443
_BUILD_DATE=	$$(date +%Y-%m-%d)

GO_MODULE=	github.com/google/${PORTNAME}
GO_TARGET=	./cmd/${PORTNAME}
GO_BUILDFLAGS=	-ldflags "\
		-s -w \
		-X main.version=${_BUILD_VERSION} \
		-X main.date=${_BUILD_DATE} \
		-X main.commit=${_BUILD_COMMIT}"

PORTDOCS=	README.md
PLIST_FILES=	${GO_TARGET:C/.\/cmd/bin/}

OPTIONS_DEFINE=	DOCS

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${WRKSRC}/${PORTDOCS} \
		${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
