# $NetBSD: Makefile,v 1.8 2012/10/23 19:50:54 asau Exp $
#

DISTNAME=	cdrkit-1.1.9
PKGREVISION=	1
CATEGORIES=	sysutils
MASTER_SITES=	http://cdrkit.org/releases/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://cdrkit.org/
COMMENT=	Portable command-line CD/DVD recorder software

CONFLICTS=	cdrtools-[0-9]*

USE_CMAKE=	yes
USE_TOOLS+=	perl:run
USE_LANGUAGES=	c c++
CMAKE_ARGS+=	-DMANSUBDIR=${PKGMANDIR}

REPLACE_PERL=	3rd-party/dirsplit/dirsplit

.include "../../mk/oss.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
