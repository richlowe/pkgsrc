# $NetBSD: Makefile,v 1.5 2012/10/06 14:11:21 asau Exp $

DISTNAME=	silgraphite-2.3.1
PKGNAME=	${DISTNAME:S/silgraphite/silgraphite-ft/}
PKGREVISION=	1
CATEGORIES=	graphics
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=silgraphite/}

MAINTAINER=	minskim@NetBSD.org
HOMEPAGE=	http://silgraphite.sourceforge.net/
COMMENT=	FreeType wrapper for SIL Graphite

GNU_CONFIGURE=	yes
USE_LIBTOOL=	yes
USE_TOOLS+=	pkg-config
USE_LANGUAGES=	c c++
WRKSRC=		${WRKDIR}/${DISTNAME}/wrappers/freetype

PKGCONFIG_OVERRIDE+=	silgraphite-ft.pc
INSTALLATION_DIRS+=	lib/pkgconfig

.include "../../graphics/freetype2/buildlink3.mk"
.include "../../graphics/silgraphite/buildlink3.mk"

post-install:
	${INSTALL_DATA} ${WRKSRC}/silgraphite-ft.pc \
		${DESTDIR}${PREFIX}/lib/pkgconfig

.include "../../mk/bsd.pkg.mk"
