ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/misc/mediatek/leds/$(MTK_PLATFORM)
ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/misc/mediatek/video/include
ccflags-y += -I$(DEVICE_MODULES_PATH)/drivers/misc/mediatek/imgsensor/inc/

obj-m 	+= prize_dual_camera.o
obj-y	+= gc032a.o
obj-y	+= gc0310.o
obj-y	+= gc6133.o
obj-y	+= bf2257cs.o
ccflags-y += $(addprefix -DPRIZE_MB_, $(shell echo $(CONFIG_PRIZE_BOARD) | tr a-z A-Z))