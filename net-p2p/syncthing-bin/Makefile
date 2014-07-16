# Created by: Kyle Williams
# $FreeBSD$

PORTNAME=	syncthing-bin
PORTVERSION=	0.8.17
PORTREVISION=	2
CATEGORIES=	net-p2p
MASTER_SITES= https://github.com/calmh/syncthing/releases/download/v${PORTVERSION}/
DISTFILES=	syncthing-freebsd-amd64-v${PORTVERSION}.tar.gz
ONLY_FOR_ARCHS= amd64

USE_RC_SUBR=	syncthingd

MAINTAINER=	kyle@1970jan1-epo.ch
COMMENT=	Encrypted P2P file synchronizer

WRKSRC= ${WRKDIR}/syncthing-freebsd-amd64-v${PORTVERSION}
PLIST_FILES=	bin/${PORTNAME}

NO_BUILD=

do-install:
	@${INSTALL_PROGRAM} ${WRKSRC}/syncthing ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
