
include $(TOPDIR)/rules.mk

PKG_NAME:=yaml-cpp
PKG_VERSION:=0.3.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=master
PKG_SOURCE_URL:=https://github.com/Kapp4/yaml-cpp.git
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz

#PKG_BUILD_DEPENDS:=boost-test
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-master

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk


define Package/libyaml-cpp
  SECTION:=agocontrol
  CATEGORY:=AgoControl
  TITLE:=YAML parser and emitter in C++
  URL:=http://code.google.com/p/yaml-cpp
endef

define Build/InstallDev
	mkdir -p $(1)/usr/include/yaml-cpp/
	$(CP) $(PKG_INSTALL_DIR)/usr/include/yaml-cpp/* $(1)/usr/include/yaml-cpp/
	mkdir -p $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/* $(1)/usr/lib/
endef


define Package/libyaml-cpp/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libyaml-cpp))
