# $FreeBSD$

PORTNAME=	pfSense-pkg-acme
PORTVERSION=	0.2.8
PORTREVISION=	2
CATEGORIES=	security
MASTER_SITES=	# empty
DISTFILES=	# empty
EXTRACT_ONLY=	# empty

MAINTAINER=	PiBa.NL.dev@gmail.com
COMMENT=	ACME package for pfSense

LICENSE=	APACHE20

RUN_DEPENDS=	${LOCALBASE}/bin/socat:net/socat
php56_RUN_DEPENDS=	php56-pecl-ssh2>=0.13:security/pecl-ssh2-0
php72_RUN_DEPENDS=	${PHP_PKGNAMEPREFIX}pecl-ssh2>=0:security/pecl-ssh2@${PHP_FLAVOR} \

USES=		php:flavors
IGNORE_WITH_PHP=	70 71
USE_PHP=	ftp

NO_BUILD=	yes
NO_MTREE=	yes

SUB_FILES=	pkg-install pkg-deinstall
SUB_LIST=	PORTNAME=${PORTNAME}

php72_PKGNAMESUFFIX=	${PHP_PKGNAMESUFFIX}

do-extract:
	${MKDIR} ${WRKSRC}

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${MKDIR} ${STAGEDIR}${PREFIX}/www/acme
	${MKDIR} ${STAGEDIR}/etc/inc/priv
	${MKDIR} ${STAGEDIR}${DATADIR}
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/pkg/acme.xml \
		${STAGEDIR}${PREFIX}/pkg
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/pkg/acme/acme.inc \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/acme.sh \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/pkg/acme/acme_sh.inc \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/acme_command.sh \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/pkg/acme/acme_gui.inc \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/pkg/acme/acme_htmllist.inc \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/pkg/acme/acme_serverconnectors.inc \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/pkg/acme/acme_utils.inc \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/pkg/acme/pkg_acme_tabs.inc \
		${STAGEDIR}${PREFIX}/pkg/acme
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_acmedns.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_ad.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_ali.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_autodns.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_aws.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_azure.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_cf.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_cloudns.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_cx.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_cyon.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_da.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_dgon.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_dnsimple.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_do.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_dp.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_dreamhost.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_duckdns.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_dyn.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_dynu.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_freedns.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_gandi_livedns.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_gd.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_he.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_infoblox.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_inwx.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_ispconfig.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_kinghost.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_knot.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_lexicon.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_linode.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_loopia.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_lua.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_me.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_myapi.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_namecom.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_namesilo.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_nsone.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_nsupdate.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_ovh.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_pdns.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_selectel.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_servercow.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_unoeuro.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_vscale.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_yandex.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_zilore.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_SCRIPT} ${FILESDIR}${PREFIX}/pkg/acme/dnsapi/dns_zonomi.sh \
		${STAGEDIR}${PREFIX}/pkg/acme/dnsapi
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/www/acme/acme_accountkeys.php \
		${STAGEDIR}${PREFIX}/www/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/www/acme/acme_accountkeys_edit.php \
		${STAGEDIR}${PREFIX}/www/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/www/acme/acme_certificates.php \
		${STAGEDIR}${PREFIX}/www/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/www/acme/acme_certificates_edit.php \
		${STAGEDIR}${PREFIX}/www/acme
	${INSTALL_DATA} ${FILESDIR}${PREFIX}/www/acme/acme_generalsettings.php \
		${STAGEDIR}${PREFIX}/www/acme
	${INSTALL_DATA} ${FILESDIR}/etc/inc/priv/acme.priv.inc \
		${STAGEDIR}/etc/inc/priv
	${INSTALL_DATA} ${FILESDIR}${DATADIR}/info.xml \
		${STAGEDIR}${DATADIR}
	@${REINPLACE_CMD} -i '' -e "s|%%PKGVERSION%%|${PKGVERSION}|" \
		${STAGEDIR}${DATADIR}/info.xml

.include <bsd.port.mk>
