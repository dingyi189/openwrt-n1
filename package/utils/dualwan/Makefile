# Copyright (C) 2018 DingYi <dingyi139@gmail.com>
#
# This is free software, licensed under the Apache License, Version 2.0 .
#

include $(TOPDIR)/rules.mk

PKG_NAME:=dualwan
PKG_VERSION:=1.0
PKG_RELEASE:=68
PKG_LICENSE:=GPLv3
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/dualwan
  SECTION:=luci
  CATEGORY:=LuCI
  TITLE:=LuCI support for Default Settings
  PKGARCH:=all
  DEPENDS:=+kmod-igb +luci-app-mwan3
endef

define Package/dualwan/description
	Language Support Packages.
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/dualwan/install
	$(INSTALL_DIR) $(1)/etc/uci-defaults
	$(INSTALL_BIN) ./files/zzz-default-settings $(1)/etc/uci-defaults/99-dualwan
endef

$(eval $(call BuildPackage,dualwan))
