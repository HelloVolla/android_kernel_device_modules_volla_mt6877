#makefile
subdir-ccflags-y += -I$(DEVICE_MODULES_PATH)/sound/soc/mediatek/common

# debugging support (also enables trace_printk)
ccflags-y += -I$(DEVICE_MODULES_PATH)/sound/soc/codecs/tfa98xx/inc
ccflags-y += -DDEBUG -DTFA_NON_DSP_SOLUTION
ccflags-y += -Werror
ccflags-y += $(call cc-option,-Wno-date-time,)
snd-soc-aw883xx-objs +=  aw883xx.o aw883xx_monitor.o aw883xx_bin_parse.o aw883xx_device.o aw883xx_init.o aw883xx_calib.o aw883xx_spin.o aw883xx_pid_2049_init.o aw883xx_pid_2066_init.o aw883xx_pid_2183_init.o
obj-$(CONFIG_SND_SOC_AW883XX) += snd-soc-aw883xx.o

