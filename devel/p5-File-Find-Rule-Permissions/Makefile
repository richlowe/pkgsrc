# $NetBSD: Makefile,v 1.6 2012/10/31 11:18:10 asau Exp $

DISTNAME=	File-Find-Rule-Permissions-2.0
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	3
CATEGORIES=	devel perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=File/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://search.cpan.org/dist/File-Find-Rule-Permissions/
COMMENT=	Rule to match on file permissions and user access
LICENSE=	${PERL5_LICENSE}

PKG_INSTALLATION_TYPES=	overwrite pkgviews

DEPENDS+=	p5-Devel-CheckOS>=1:../../devel/p5-Devel-CheckOS
DEPENDS+=	p5-File-Find-Rule>=0.10:../../devel/p5-File-Find-Rule

PERL5_PACKLIST=		auto/File/Find/Rule/Permissions/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
