#
# Makefile for the <t-base trusted UI driver
#

GUD_ROOT_FOLDER := drivers/gud-htc/

# add our modules to kernel.
obj-$(CONFIG_TRUSTONIC_TRUSTED_UI) += t-base-tui.o

t-base-tui-y := main.o tlcTui.o tui-hal.o

# Release mode by default
ccflags-y += -DNDEBUG
ccflags-y += -Wno-declaration-after-statement

ccflags-$(CONFIG_TRUSTONIC_TEE_DEBUG) += -DDEBUG

# MobiCore Driver includes
ccflags-y += -I$(GUD_ROOT_FOLDER)/MobiCoreDriver/public

# MobiCore TlcTui required includes
ccflags-y += -I$(GUD_ROOT_FOLDER)/TlcTui/inc \
             -I$(GUD_ROOT_FOLDER)/TlcTui/public
