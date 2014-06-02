ifeq ($(CONFIG_OF),y)

dtb-$(CONFIG_ARCH_OMAP2PLUS) += \
	omap3-beagle.dtb \
	omap3-beagle-xm.dtb \
	omap3-beagle-xm-ab.dtb \
	am335x-bone.dtb \
	am335x-boneblack.dtb

targets += dtbs dtbs_install
targets += $(dtb-y)
endif

# *.dtb used to be generated in the directory above. Clean out the
# old build results so people don't accidentally use them.
dtbs: $(addprefix $(obj)/, $(dtb-y))
	$(Q)rm -f $(obj)/../*.dtb

clean-files := *.dtb

dtbs_install: $(addsuffix _dtbinst_, $(dtb-y))
