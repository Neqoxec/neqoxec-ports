# Created by: Kyle Williams
# $FreeBSD$

PORTNAME=	llpp
PORTVERSION=	1.0
PORTREVISION=	1
CATEGORIES=	graphics
MASTER_SITES= http://repo.or.cz/w/llpp.git/snapshot/
DISTFILES= 902143de64d86b5714b3a59d2cc7085083b87249.tar.gz #Jun-09-2014

MAINTAINER=	kyle@1970jan1-epo.ch
COMMENT=	Keyboard-friendly lightweight PDF reader based on MuPDF

USE_XORG=	xmu xdmcp xau x11
USE_BZIP2=	yes
USE_OCAML=	yes

BUILD_DEPENDS=	${LOCALBASE}/bin/mupdf:${PORTSDIR}/graphics/mupdf \
					${LOCALBASE}/bin/xsel:${PORTSDIR}/x11/xsel \
					${LOCALBASE}/bin/jbig2dec:${PORTSDIR}/graphics/jbig2dec 
					${LOCALBASE}/asdfasdf:${PORTSDIR}/lang/ocaml \
					${LOCALBASE}/asdfasdf:${PORTSDIR}/lang/ocaml-lablgl 

LIB_DEPENDS=	libfreetype.so:${PORTSDIR}/print/freetype \
					libXcm.so:${PORTSDIR}/x11/libXcm \
					libopenjpeg.so:${PORTSDIR}/graphics/openjpeg

do-build:
	(cd ${WRKSRC} && ${OMAKE} ${OMARGS})

do-install:
	@${INSTALL_BIN} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
