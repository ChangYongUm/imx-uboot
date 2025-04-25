# SPDX-License-Identifier: GPL-2.0+

dtb-$(CONFIG_ARCH_IMX8M) += \
	imx8mm-edm-g-wb.dtb \
	imx8mp-edm-g.dtb 


ifdef CONFIG_RCAR_64
DTC_FLAGS += -R 4 -p 0x1000
endif

include $(srctree)/scripts/Makefile.dts

targets += $(dtb-y)

# Add any required device tree compiler flags here
DTC_FLAGS += -a 0x8

DTC_FLAGS_imx8mp-dhcom-pdk3-overlay-rev100 += -Wno-avoid_default_addr_size -Wno-reg_format

PHONY += dtbs
dtbs: $(addprefix $(obj)/, $(dtb-y))
	@:

clean-files := *.dtb *.dtbo *_HS
