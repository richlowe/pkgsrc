# $NetBSD: Makefile,v 1.11 2012/10/31 11:18:01 asau Exp $

DISTNAME=	Devel-PPPort-3.20
PKGNAME=	p5-${DISTNAME:S/_/./}
PKGREVISION=	1
CATEGORIES=	devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=../../authors/id/M/MH/MHX/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/Devel-PPPort/
COMMENT=	Perl5 module to bring newer features to older perl
LICENSE=	${PERL5_LICENSE}

USE_LANGUAGES=	c
PERL5_PACKLIST=	auto/Devel/PPPort/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
