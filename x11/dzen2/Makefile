# Created by: Morten Slot Kristensen
# Modified by: Kyle Williams
# $FreeBSD$

PORTNAME=	dzen2
PORTVERSION=	1.0
PORTREVISION=	2
CATEGORIES=	x11

USE_GITHUB=	yes
GH_ACCOUNT=	robm
GH_PROJECT=	dzen
GH_TAGNAME=	${GH_COMMIT}
GH_COMMIT=	f7907da

WRKSRC= ${WRKDIR}/${GH_ACCOUNT}-${GH_PROJECT}-${GH_COMMIT}

MAINTAINER=	kyle@1970jan1-epo.ch
COMMENT=	General purpose messaging, notification and menuing program for X11

USE_XORG=	x11

PLIST_FILES=	bin/${PORTNAME}

OPTIONS_DEFINE=	XPM XINERAMA XFT
OPTIONS_DEFAULT=	XPM XINERAMA XFT

LDFLAGS=	-L${LOCALBASE}/lib
CFLAGS=		-I${LOCALBASE}/include
XPM_USE=	XORG=xpm
XPM_CFLAGS=	-DDZEN_XPM
XPM_LDFLAGS=	-lXpm
XINERAMA_USE=	XORG=xinerama
XINERAMA_LDFLAGS=	-lXinerama
XINERAMA_CLAGS=	-DDZEN_XINERAMA
XFT_USE=	XORG=xft
XFT_CFLAGS=	-DDZEN_XFT -D_THREAD_SAFE -I/usr/local/include  -I/usr/local/include/freetype2  
XFT_LDFLAGS=	-L/usr/local/lib -lXft
XFT_LIB_DEPENDS=	libXft.so:${PORTSDIR}/x11-fonts/libXft

MAKE_ARGS=	LDFLAGS="${LDFLAGS} \$${LIBS}" \
		CFLAGS="${CFLAGS} ${INCS} -DVERSION=\\\"\$${VERSION}\\\""

.include <bsd.port.mk>
