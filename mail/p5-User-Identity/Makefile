# $NetBSD: Makefile,v 1.16 2012/10/08 12:19:25 asau Exp $

DISTNAME=	User-Identity-0.93
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	3
CATEGORIES=	mail perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=User/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://perl.overmeer.net/userid/
#HOMEPAGE=	http://search.cpan.org/dist/User-Identity/
COMMENT=	Helps maintaining user information from various sources
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-Geography-Countries>=1.4:../../geography/p5-Geography-Countries
BUILD_DEPENDS+=	p5-Test-Pod>=1.0:../../devel/p5-Test-Pod

PKG_INSTALLATION_TYPES=	overwrite pkgviews

PERL5_PACKLIST=	auto/User/Identity/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
