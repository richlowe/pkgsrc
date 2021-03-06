# $NetBSD: Makefile,v 1.32 2012/12/03 13:04:24 ryoon Exp $

DISTNAME=	OpenCV-2.4.3
PKGNAME=	${DISTNAME:S/a$//:tl}
CATEGORIES=	graphics devel
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=opencvlibrary/}
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	anthony.mallet@laas.fr
HOMEPAGE=	http://code.opencv.org/projects/OpenCV/wiki/WikiStart
COMMENT=	Library for computer vision problems
LICENSE=	modified-bsd

USE_CMAKE=		yes
USE_LANGUAGES=		c c++
USE_LIBTOOL=		yes
USE_PKGLOCALEDIR=	yes
USE_TOOLS+=		gmake pkg-config

INSTALLATION_DIRS+=	share/doc/opencv/papers
INSTALLATION_DIRS+=	share/doc/opencv/ref/pics
INSTALLATION_DIRS+=	share/OpenCV/haarcascades

PKGCONFIG_OVERRIDE+=	opencv.pc.cmake.in

REPLACE_PYTHON+=	samples/python/*.py

WRKSRC=		${WRKDIR}/${DISTNAME:S/a$//}

# includes configure output and paths to gmake etc.
CHECK_WRKREF_SKIP=	${PREFIX}/lib/libopencv_core.*

.include "options.mk"

.include "../../devel/zlib/buildlink3.mk"
.include "../../graphics/jasper/buildlink3.mk"
.include "../../graphics/openexr/buildlink3.mk"
.include "../../graphics/png/buildlink3.mk"
.include "../../graphics/tiff/buildlink3.mk"
.if ${OPSYS} != "Darwin"
.include "../../x11/gtk2/buildlink3.mk"
.endif
.include "../../mk/jpeg.buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
