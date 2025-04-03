# SPDX-License-Identifier: GPL-2.0-only
#
# Copyright (C) 2025 OpenWrt.org

include $(TOPDIR)/rules.mk

ARCH:=aarch64
BOARD:=octeon-cn10k
BOARDNAME:=Marvell OCTEON 10 CN102
FEATURES:=ext4 targz pcie usb
SUBTARGETS:=generic

KERNEL_PATCHVER:=6.6

include $(INCLUDE_DIR)/target.mk

DEFAULT_PACKAGES += \
    kmod-gpio-button-hotplug \
    uboot-envtools \
    kmod-usb3 \
    kmod-pcie-octeon \
    e2fsprogs \
    ethtool

define Target/Description
    Build firmware images for Marvell OCTEON 10 CN102 (ARM Neoverse N2) based boards.
endef

$(eval $(call BuildTarget))
