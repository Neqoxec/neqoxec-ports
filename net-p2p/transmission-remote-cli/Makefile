# Created by: Kyle Williams
# $FreeBSD$

PORTNAME=	transmission-remote-cli
PORTVERSION=	20140721
PORTREVISION=	1
CATEGORIES=	net-p2p

USE_GITHUB=	yes
GH_ACCOUNT=	fagga
GH_PROJECT=	${PORTNAME}
GH_TAGNAME=	${GH_COMMIT}
GH_COMMIT=	32b82fe

WRKSRC= ${WRKDIR}/${GH_ACCOUNT}-${GH_PROJECT}-${GH_COMMIT}
NO_BUILD=
USE_PYTHON=

MAINTAINER=	kyle@1970jan1-epo.ch
COMMENT=	Curses client for Transmission RPC

PLIST_FILES=	bin/${PORTNAME}

#Optional modules:
#  GeoIP: Guess what country a peer is in
#  adns: Resolve IPs to host names

do-install:
	@${INSTALL_SCRIPT} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
