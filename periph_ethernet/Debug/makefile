################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include example/src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: periph_ethernet.axf

# Tool invocations
periph_ethernet.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: MCU Linker'
	arm-none-eabi-gcc -nostdlib -L"C:\Users\B45511\Documents\MCUXpressoIDE_10.1.0_580_prc3\workspace\lpc_chip_40xx\Debug" -L"C:\Users\B45511\Documents\MCUXpressoIDE_10.1.0_580_prc3\workspace\lpc_board_ea_devkit_4088\Debug" -Xlinker -Map="periph_ethernet.map" -Xlinker --gc-sections -mcpu=cortex-m4 -mfpu=fpv4-sp-d16 -mfloat-abi=softfp -mthumb -T "periph_ethernet_Debug.ld" -o "periph_ethernet.axf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '
	$(MAKE) --no-print-directory post-build

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) periph_ethernet.axf
	-@echo ' '

post-build:
	-@echo 'Performing post-build steps'
	-arm-none-eabi-size "periph_ethernet.axf"; # arm-none-eabi-objcopy -v -O binary "periph_ethernet.axf" "periph_ethernet.bin" ; # checksum -p LPC4088 -d "periph_ethernet.bin";
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
