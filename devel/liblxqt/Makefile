PORTNAME=	liblxqt
PORTVERSION=	1.4.0
CATEGORIES=	devel
MASTER_SITES=	LXQT

MAINTAINER=	jsm@FreeBSD.org
COMMENT=	Shared library for LXQt applications
WWW=		https://github.com/lxqt/liblxqt

LICENSE=	LGPL21+

LIB_DEPENDS=	libpolkit-qt5-core-1.so:sysutils/polkit-qt-1@qt5

USES=	cmake compiler:c++14-lang gnome kde:5 lxqt \
	pkgconfig qt:5 tar:xz xorg
USE_GNOME=	glib20
USE_QT=		buildtools:build qmake:build dbus core gui \
		svg widgets x11extras xml
USE_KDE=	windowsystem
USE_LXQT=	buildtools qtxdg
USE_XORG=	x11 xscrnsaver
USE_LDCONFIG=	yes

.include <bsd.port.mk>
