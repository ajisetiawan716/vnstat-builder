#
# Copyright (C) 2008-2023 OpenWrt.org
# This is free software, licensed under the GPL 2 license.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=vnstat
PKG_VERSION:=2.12
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://humdi.net/vnstat/
PKG_HASH:=a7f99486b9c5cc172ec2dd9ce13c7f2bb9897030e58e703994dd4b3c56444c25

PKG_MAINTAINER:=OpenWrt team
PKG_LICENSE:=GPL-2.0-or-later

PKG_BUILD_PARALLEL:=1
PKG_INSTALL:=1
PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk

define Package/vnstat
  SECTION:=net
  CATEGORY:=Network
  TITLE:=Network traffic monitor
  URL:=https://humdi.net/vnstat/
  DEPENDS:=+libpthread +libsqlite3 +libpng +zlib
endef

define Package/vnstat/description
  vnStat is a console-based network traffic monitor.
endef

define Package/vnstat/install
	$(MAKE) -C $(PKG_BUILD_DIR) DESTDIR=$(1) install
endef

  $(eval $(call BuildPackage,vnstat))
  
