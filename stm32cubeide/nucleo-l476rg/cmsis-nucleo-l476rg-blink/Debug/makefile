################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L4xx_HAL_Driver/Src/subdir.mk
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

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
cmsis-nucleo-l476rg-blink.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
cmsis-nucleo-l476rg-blink.list \

OBJCOPY_BIN += \
cmsis-nucleo-l476rg-blink.bin \


# All Target
all: cmsis-nucleo-l476rg-blink.elf secondary-outputs

# Tool invocations
cmsis-nucleo-l476rg-blink.elf: $(OBJS) $(USER_OBJS) /home/orlando_floresti/ARMProjects/SourceCode/stm32cubeide/nucleo-l476rg/cmsis-nucleo-l476rg-blink/STM32L476RGTX_FLASH.ld
	arm-none-eabi-gcc -o "cmsis-nucleo-l476rg-blink.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/home/orlando_floresti/ARMProjects/SourceCode/stm32cubeide/nucleo-l476rg/cmsis-nucleo-l476rg-blink/STM32L476RGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="cmsis-nucleo-l476rg-blink.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

cmsis-nucleo-l476rg-blink.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "cmsis-nucleo-l476rg-blink.list"
	@echo 'Finished building: $@'
	@echo ' '

cmsis-nucleo-l476rg-blink.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "cmsis-nucleo-l476rg-blink.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
