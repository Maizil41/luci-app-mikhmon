# SPDX-License-Identifier: Apache-2.0

include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-mikhmonv3
PKG_VERSION:=3.0
PKG_RELEASE:=1

PKG_LICENSE:=Apache-2.0
PKG_MAINTAINER:=Maizil41 <https://github.com/maizil41>
PKG_ARCH:=all

PHP_DEPENDS:=

ifneq ($(CONFIG_PACKAGE_php8-cli),)
	PHP_DEPENDS+= \
		+php8-cli \
		+php8-cgi \
		+php8-mod-xml \
		+php8-mod-filter \
		+php8-mod-curl
endif

ifneq ($(CONFIG_PACKAGE_php7-cli),)
	PHP_DEPENDS+= \
		+php7-cli \
		+php7-cgi \
		+php7-mod-xml \
		+php7-mod-filter \
		+php7-mod-curl
endif

include $(TOPDIR)/feeds/luci/luci.mk

LUCI_TITLE:=LuCI support for Mikhmon v3
LUCI_DESCRIPTION:=LuCI configuration pages for Mikhmon v3
LUCI_DEPENDS:=+luci $(PHP_DEPENDS)

# call BuildPackage - OpenWrt buildroot signature
