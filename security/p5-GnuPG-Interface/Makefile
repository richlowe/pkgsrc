# $NetBSD: Makefile,v 1.18 2012/10/23 18:16:45 asau Exp $
#

DISTNAME=		GnuPG-Interface-0.45
PKGNAME=		p5-${DISTNAME}
PKGREVISION=		1
CATEGORIES=		security perl5
MASTER_SITES=		${MASTER_SITE_PERL_CPAN:=GnuPG/}

MAINTAINER=		pkgsrc-users@NetBSD.org
#HOMEPAGE=		http://gnupg-interface.sourceforge.net/
HOMEPAGE=		http://search.cpan.org/dist/GnuPG-Interface/
COMMENT=		Perl interface to GnuPG
LICENSE=		${PERL5_LICENSE}

DEPENDS+=		gnupg>=1.2.3:../../security/gnupg
DEPENDS+=		p5-Any-Moose>=0.04:../../devel/p5-Any-Moose

PERL5_PACKLIST=		auto/GnuPG/Interface/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
