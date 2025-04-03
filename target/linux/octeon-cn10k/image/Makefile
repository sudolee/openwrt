# SPDX-License-Identifier: GPL-2.0-only
#
# Copyright (C) 2025 OpenWrt.org

include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/image.mk

DEVICE_VARS += UBOOT_DEVICE_NAME

define Device/Default
  PROFILES := Default
  KERNEL_NAME := Image
  KERNEL := kernel-bin
  IMAGES := sysupgrade.bin
  DEVICE_DTS := marvell-cn102
endef

define Device/marvell_cn102
  DEVICE_VENDOR := Marvell
  DEVICE_MODEL := OCTEON 10 CN102
  DEVICE_PACKAGES := kmod-usb3 kmod-pcie-octeon
  SUPPORTED_DEVICES := marvell,cn102
  PAGESIZE := 2048
  BLOCKSIZE := 128k
  IMAGE_SIZE := 125829120 # 120MB
  KERNEL_SIZE := 16777216 # 16MB
endef
TARGET_DEVICES += marvell_cn102

$(eval $(call BuildImage))
