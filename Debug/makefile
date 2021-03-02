################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
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

BUILD_ARTIFACT_NAME := DENEME_0028_USART_NEXTION_USING
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX := 
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME).$(BUILD_ARTIFACT_EXTENSION)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
DENEME_0028_USART_NEXTION_USING.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
DENEME_0028_USART_NEXTION_USING.list \

OBJCOPY_BIN += \
DENEME_0028_USART_NEXTION_USING.bin \


# All Target
all: main-build

# Main-build Target
main-build: DENEME_0028_USART_NEXTION_USING.elf secondary-outputs

# Tool invocations
DENEME_0028_USART_NEXTION_USING.elf: $(OBJS) $(USER_OBJS) D:\workspace_1.5.0\DENEME_0028_USART_NEXTION_USING\STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "DENEME_0028_USART_NEXTION_USING.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\workspace_1.5.0\DENEME_0028_USART_NEXTION_USING\STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="DENEME_0028_USART_NEXTION_USING.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

DENEME_0028_USART_NEXTION_USING.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "DENEME_0028_USART_NEXTION_USING.list"
	@echo 'Finished building: $@'
	@echo ' '

DENEME_0028_USART_NEXTION_USING.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "DENEME_0028_USART_NEXTION_USING.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents fail-specified-linker-script-missing warn-no-linker-script-specified
.SECONDARY:

-include ../makefile.targets
