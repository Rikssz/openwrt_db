include $(TOPDIR)/rules.mk

PKG_NAME:=sdb
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git@github.com:Rikssz/student_db.git
PKG_SOURCE_DATE:=2024-12-23
PKG_SOURCE_VERSION:=dd326f4c
PKG_MIRROR_HASH:=skip

PKG_MAINTAINER:=Riks Sipovics <rikssipovich2@gmail.com>

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=RTU
	CATEGORY:=RTU
	DEPENDS:=+libc
	TITLE:=Student database read/write app
endef

define Package/$(PKG_NAME)/description
CLI application which allows to enter student
data and read that afterwise.
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/student_db $(1)/usr/bin/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
