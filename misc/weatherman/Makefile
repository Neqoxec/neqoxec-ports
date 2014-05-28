# Created by: Kyle Williams
# $FreeBSD$

PORTNAME=	weatherman
PORTVERSION=	1.2.2
PORTREVISION=	1
CATEGORIES=	misc

USE_GITHUB=	yes
GH_ACCOUNT=	subrosa
GH_PROJECT=	weatherman
GH_TAGNAME=	${GH_COMMIT}
GH_COMMIT=	0fe94cb

WRKSRC= ${WRKDIR}/${GH_ACCOUNT}-${GH_PROJECT}-${GH_COMMIT}
NO_BUILD= 

MAINTAINER=	kyle@1970jan1-epo.ch
COMMENT=	Weather forecasts on the CLI via weatherbug.com

PLIST_FILES=	bin/${PORTNAME}

RUN_DEPENDS=	${LOCALBASE}/bin/curl:${PORTSDIR}/ftp/curl \
					${LOCALBASE}/bin/bash:${PORTSDIR}/shells/bash

do-install:
	@${INSTALL_SCRIPT} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}
	@${INSTALL_MAN} ${WRKSRC}/${PORTNAME}.1.gz ${STAGEDIR}${MANPREFIX}/man/man1/${PORTNAME}.1.gz

.include <bsd.port.mk>
