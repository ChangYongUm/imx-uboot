# SPDX-License-Identifier: GPL-2.0+

dtb-$(CONFIG_ARCH_IMX8M) += \
	imx8mm-data-modul-edm-sbc.dtb \
	imx8mm-ddr4-evk.dtb \
	imx8mm-ddr4-ab2.dtb \
	imx8mm-evk.dtb \
	imx8mm-ab2.dtb \
	imx8mm-icore-mx8mm-ctouch2.dtb \
	imx8mm-icore-mx8mm-edimm2.2.dtb \
	imx8mm-kontron-bl.dtb \
	imx8mm-kontron-bl-osm-s.dtb \
	imx8mm-mx8menlo.dtb \
	imx8mm-phg.dtb \
	imx8mm-phyboard-polis-rdk.dtb \
	imx8mm-phygate-tauri-l.dtb \
	imx8mm-venice.dtb \
	imx8mm-venice-gw71xx-0x.dtb \
	imx8mm-venice-gw72xx-0x.dtb \
	imx8mm-venice-gw73xx-0x.dtb \
	imx8mm-venice-gw7901.dtb \
	imx8mm-venice-gw7902.dtb \
	imx8mm-venice-gw7903.dtb \
	imx8mm-venice-gw7904.dtb \
	imx8mm-venice-gw7905-0x.dtb \
	imx8mm-pico-pi.dtb \
	imx8mm-pico-wizard.dtb \
	imx8mm-edm-g-wb.dtb \
	imx8mm-verdin-wifi-dev.dtb \
	imx8mp-axon.dtb \
	imx8mp-beacon-kit.dtb \
	imx8mp-data-modul-edm-sbc.dtb \
	imx8mp-dhcom-som-overlay-rev100.dtbo \
	imx8mp-dhcom-som-overlay-eth1xfast.dtbo \
	imx8mp-dhcom-som-overlay-eth2xfast.dtbo \
	imx8mp-dhcom-pdk-overlay-eth2xfast.dtbo \
	imx8mp-debix-model-a.dtb \
	imx8mp-dhcom-pdk2.dtb \
	imx8mp-dhcom-pdk3.dtb \
	imx8mp-dhcom-pdk3-overlay-rev100.dtbo \
	imx8mp-edm-g.dtb \
	imx8mp-sc.dtb \
	imx8mp-tek.dtb \
	imx8mp-tep.dtb \
	imx8mp-ddr4-evk.dtb \
	imx8mp-evk.dtb \
	imx8mp-icore-mx8mp-edimm2.2.dtb \
	imx8mp-msc-sm2s.dtb \
	imx8mp-phyboard-pollux-rdk.dtb \
	imx8mp-venice.dtb \
	imx8mp-venice-gw71xx-2x.dtb \
	imx8mp-venice-gw72xx-2x.dtb \
	imx8mp-venice-gw73xx-2x.dtb \
	imx8mp-venice-gw74xx.dtb \
	imx8mp-venice-gw7905-2x.dtb \
	imx8mp-verdin-wifi-dev.dtb \
	imx8mp-navqp.dtb 


ifdef CONFIG_RCAR_64
DTC_FLAGS += -R 4 -p 0x1000
endif

dtb-$(CONFIG_TARGET_IMX8MM_CL_IOT_GATE) += imx8mm-cl-iot-gate.dtb \
					imx8mm-cl-iot-gate-ied.dtbo \
					imx8mm-cl-iot-gate-ied-adc0.dtbo \
					imx8mm-cl-iot-gate-ied-adc1.dtbo \
					imx8mm-cl-iot-gate-ied-can0.dtbo \
					imx8mm-cl-iot-gate-ied-can1.dtbo \
					imx8mm-cl-iot-gate-ied-tpm0.dtbo \
					imx8mm-cl-iot-gate-ied-tpm1.dtbo

dtb-$(CONFIG_TARGET_IMX8MM_CL_IOT_GATE_OPTEE) += imx8mm-cl-iot-gate-optee.dtb \
					imx8mm-cl-iot-gate-ied.dtbo \
					imx8mm-cl-iot-gate-ied-adc0.dtbo \
					imx8mm-cl-iot-gate-ied-adc1.dtbo \
					imx8mm-cl-iot-gate-ied-can0.dtbo \
					imx8mm-cl-iot-gate-ied-can1.dtbo \
					imx8mm-cl-iot-gate-ied-tpm0.dtbo \
					imx8mm-cl-iot-gate-ied-tpm1.dtbo

ifneq ($(CONFIG_TARGET_IMX8MP_RSB3720A1_4G)$(CONFIG_TARGET_IMX8MP_RSB3720A1_6G),)
dtb-y += imx8mp-rsb3720-a1.dtb
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
