#
# $FreeBSD$
#

.include <bsd.own.mk>

GMIME_DISTDIR?= ${.CURDIR}/../../../contrib/gmime-2.6

LIB=	util	

.PATH:		${GMIME_DISTDIR}/util
SRCS=		\
		cache.c		\
		gtrie.c		\
		list.c		\
		md5-utils.c	\
		url-scanner.c

WARNFLAGS=	-Wall -Wstrict-prototypes				\
		-Werror=implicit-function-declaration -Werror=init-self \
		-Werror=format-security -Werror=missing-include-dirs -Wno-error

OPTIONS=	-DHAVE_CONFIG_H -DG_LOG_DOMAIN=\"util\"			\
		-DLIBICONV_PLUG

CFLAGS+=	-I${.CURDIR}						\
		-I${.CURDIR}/..						\
		-I${GMIME_DISTDIR}					\
		-I${GMIME_DISTDIR}/util					\
		-I/usr/local/include/glib-2.0				\
		-I/usr/local/include					\
		${OPTIONS} ${WARNFLAGS} -pthread 

.include <bsd.lib.mk>
.include <bsd.subdir.mk>
