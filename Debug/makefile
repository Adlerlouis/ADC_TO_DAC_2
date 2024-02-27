################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (11.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Practica9_FIR_STM32F429
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Practica9_FIR_STM32F429.elf \

MAP_FILES += \
Practica9_FIR_STM32F429.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Practica9_FIR_STM32F429.list \

OBJCOPY_HEX += \
Practica9_FIR_STM32F429.hex \


# All Target
all: main-build

# Main-build Target
main-build: Practica9_FIR_STM32F429.elf secondary-outputs

# Tool invocations
Practica9_FIR_STM32F429.elf Practica9_FIR_STM32F429.map: $(OBJS) $(USER_OBJS) /media/adler/SSD2/Axel\ 8I\ SEMESTRE\ UAA/CONTROL\ DISCRETO/ADC_TO_DAC_2/ADC_TO_DAC/Practica9_FIR_STM32F429/STM32F429ZITX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Practica9_FIR_STM32F429.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/media/adler/SSD2/Axel 8I SEMESTRE UAA/CONTROL DISCRETO/ADC_TO_DAC_2/ADC_TO_DAC/Practica9_FIR_STM32F429/STM32F429ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Practica9_FIR_STM32F429.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Practica9_FIR_STM32F429.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Practica9_FIR_STM32F429.list"
	@echo 'Finished building: $@'
	@echo ' '

Practica9_FIR_STM32F429.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "Practica9_FIR_STM32F429.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Practica9_FIR_STM32F429.elf Practica9_FIR_STM32F429.hex Practica9_FIR_STM32F429.list Practica9_FIR_STM32F429.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
