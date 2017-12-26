dtb-$(CONFIG_ARCH_THUNDER) += thunder-88xx.dtb
dtb-$(CONFIG_ARCH_VEXPRESS) += rtsm_ve-aemv8a.dtb foundation-v8.dtb
dtb-$(CONFIG_ARCH_XGENE) += apm-mustang.dtb
dtb-$(CONFIG_SOC_EXYNOS8890) += exynos8890-espresso8890.dtb exynos8890-espresso8890_rev01.dtb exynos8890-universal8890.dtb exynos8890-smdk8890.dtb
dtb-$(CONFIG_SOC_EXYNOS8890) += exynos8890-evt1-smdk8890.dtb
dtb-$(CONFIG_SOC_EXYNOS7870) += exynos7870-j7y17lte_sea_open_00.dts exynos7870-j7y17lte_sea_open_01.dts exynos7870-j7y17lte_sea_open_02.dts exynos7870-j7y17lte_sea_open_03.dts exynos7870-j7y17lte_sea_open_04.dts exynos7870-j7y17lte_sea_open_05.dts exynos7870-j7y17lte_sea_open_06.dts

targets += dtbs

DTB_NAMES := $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES))
ifneq ($(DTB_NAMES),)
DTB_LIST := $(addsuffix .dtb,$(DTB_NAMES))
else
DTB_LIST := $(dtb-y)
endif
targets += $(DTB_LIST)

dtbs: $(addprefix $(obj)/, $(DTB_LIST))

clean-files := dts/*.dtb *.dtb
