PORTNAME=	gitlab-fog-azure-rm
PORTVERSION=	1.8.0
CATEGORIES=	net rubygems
MASTER_SITES=	RG

MAINTAINER=	mfechner@FreeBSD.org
COMMENT=	Stripped-down fork that enables Azure Blob Storage
WWW=		https://gitlab.com/gitlab-org/gitlab-fog-azure-rm

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE.md

RUN_DEPENDS=	rubygem-azure-storage-blob>=2.0<3:devel/rubygem-azure-storage-blob \
		rubygem-azure-storage-common>=2.0<3:devel/rubygem-azure-storage-common \
		rubygem-fog-core>=2.1.0:devel/rubygem-fog-core \
		rubygem-fog-json>=1.2.0<1.3:devel/rubygem-fog-json \
		rubygem-mime-types>=0:misc/rubygem-mime-types

USES=		gem

NO_ARCH=	yes

.include <bsd.port.mk>
