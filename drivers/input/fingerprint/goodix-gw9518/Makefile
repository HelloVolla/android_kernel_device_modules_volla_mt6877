#
# Makefile for the fingerprint device.
#

# Each configuration option enables a list of files.
#include $(srctree)/drivers/misc/mediatek/Makefile.custom

# for microtrust tee start
ifneq ($(filter y m, $(CONFIG_MICROTRUST_TEE_SUPPORT)),)
ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/spi/mediatek/$(MTK_PLATFORM)
ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/misc/mediatek/include/mt-plat
ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/misc/mediatek/include/mt-plat/$(MTK_PLATFORM)/include
subdir-ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/misc/mediatek/include
subdir-ccflags-y += -I$(DEVICE_MODULES_PATH)drivers/spi/mediatek/$(MTK_PLATFORM)
ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/gpu/drm/mediatek/mediatek_v2/
# ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/tee/teei/
include $(DEVICE_MODULES_PATH)/drivers/tee/teei/Makefile.include
endif
# for microtrust tee end

# for trustkernel tee start
ifeq ($(filter y m, $(CONFIG_TRUSTKERNEL_TEE_SUPPORT)),)
ccflags-y += -DCONFIG_FINGERPRINT_FOCALTECH_SPI_SUPPORT
ccflags-y += -DCONFIG_FINGERPRINT_FOCALTECH_SPICLK_SUPPORT
ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/misc/mediatek/tkcore/include/
endif
# for trustkernel tee end

# for trustonic tee start
ifneq ($(filter y m, $(CONFIG_TRUSTONIC_TEE_SUPPORT)),)

endif
# for trustonic tee end

obj-$(CONFIG_MTK_FINGERPRINT_SUPPORT_GW95XX)	+= gf_tee.o
#gf_tee-y := gf_spi_tee.o gf_spi_factory.o
gf_tee-y := gf_spi_tee.o
