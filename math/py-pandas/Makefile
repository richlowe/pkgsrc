# $NetBSD: Makefile,v 1.1 2012/11/22 00:15:13 bad Exp $

DISTNAME=	pandas-0.9.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	math graphics python
MASTER_SITES=	http://pypi.python.org/packages/source/p/pandas/

MAINTAINER=	bad@NetBSD.org
HOMEPAGE=	http://pandas.pydata.org/
COMMENT=	Python Data Analysis Library
LICENSE=	modified-bsd

DEPENDS+=	${PYPKGPREFIX}-dateutil>=1.5:../../time/py-dateutil
DEPENDS+=	${PYPKGPREFIX}-pytz>=1.5:../../time/py-pytz
DEPENDS+=	${PYPKGPREFIX}-scipy>=0.7:../../math/py-scipy

PYDISTUTILSPKG=	yes
PLIST_SUBST+=   PYPKGPREFIX=${PYPKGPREFIX}
USE_LANGUAGES+=	c c++

# XXX Avoid picking up other compilers when installed
.include "../../mk/compiler.mk"

.include "../../lang/python/egg.mk"
.include "../../math/py-numpy/buildlink3.mk"
.include "../../graphics/py-matplotlib/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
