# $NetBSD: Makefile,v 1.46 2012/10/06 14:11:01 asau Exp $

DISTNAME=	jpegsrc.v8d
PKGNAME=	${DISTNAME:S/src.v/-/}
CATEGORIES=	graphics
MASTER_SITES=	http://www.ijg.org/files/

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.ijg.org/
COMMENT=	IJG's jpeg compression utilities

CONFLICTS=		libjpeg-turbo-[0-9]*

PKG_INSTALLATION_TYPES=	overwrite pkgviews

WRKSRC=			${WRKDIR}/${PKGNAME_NOREV}
USE_LIBTOOL=		yes
GNU_CONFIGURE=		yes
CONFIGURE_ARGS+=	--disable-ld-version-script

INSTALLATION_DIRS=	bin include share/doc/jpeg

TEST_TARGET=		test

post-extract:
	${CP} ${FILESDIR}/jpegexiforient.c ${WRKSRC}

post-install:
	${INSTALL_SCRIPT} ${FILESDIR}/exifautotran ${DESTDIR}${PREFIX}/bin
	${INSTALL_DATA} ${WRKSRC}/jpegint.h ${DESTDIR}${PREFIX}/include
	${INSTALL_DATA} ${WRKSRC}/*.txt ${DESTDIR}${PREFIX}/share/doc/jpeg

.include "../../mk/bsd.pkg.mk"
