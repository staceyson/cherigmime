#
# $FreeBSD$
#

.include <bsd.own.mk>

GMIME_DISTDIR?= ${.CURDIR}/../../../contrib/gmime-2.6

LIB=	gmime-2.6	

.PATH:		${GMIME_DISTDIR}/gmime
SRCS=		\
		gmime-certificate.c		\
		gmime-charset.c		\
		gmime-common.c		\
		gmime-content-type.c		\
		gmime-crypto-context.c		\
		gmime-data-wrapper.c		\
		gmime-disposition.c		\
		gmime-encodings.c		\
		gmime-events.c		\
		gmime-filter-basic.c		\
		gmime-filter-best.c		\
		gmime-filter-charset.c		\
		gmime-filter-crlf.c		\
		gmime-filter-enriched.c		\
		gmime-filter-from.c		\
		gmime-filter-gzip.c		\
		gmime-filter-html.c		\
		gmime-filter-md5.c		\
		gmime-filter-strip.c		\
		gmime-filter-windows.c		\
		gmime-filter-yenc.c		\
		gmime-filter.c		\
		gmime-gpg-context.c		\
		gmime-header.c		\
		gmime-iconv-utils.c		\
		gmime-iconv.c		\
		gmime-message-part.c		\
		gmime-message-partial.c		\
		gmime-message.c		\
		gmime-multipart-encrypted.c		\
		gmime-multipart-signed.c		\
		gmime-multipart.c		\
		gmime-object.c		\
		gmime-param.c		\
		gmime-parse-utils.c		\
		gmime-parser.c		\
		gmime-part-iter.c		\
		gmime-part.c		\
		gmime-pkcs7-context.c		\
		gmime-signature.c		\
		gmime-stream-buffer.c		\
		gmime-stream-cat.c		\
		gmime-stream-file.c		\
		gmime-stream-filter.c		\
		gmime-stream-fs.c		\
		gmime-stream-gio.c		\
		gmime-stream-mem.c		\
		gmime-stream-mmap.c		\
		gmime-stream-null.c		\
		gmime-stream-pipe.c		\
		gmime-stream.c		\
		gmime-utils.c		\
		gmime.c		\
		internet-address.c

WARNFLAGS=	-Wall -Wstrict-prototypes				\
		-Werror=implicit-function-declaration -Werror=init-self \
		-Werror=format-security -Werror=missing-include-dirs -Wno-error

OPTIONS=	-DHAVE_CONFIG_H -DG_LOG_DOMAIN=\"gmime\"		\
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
