################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
canfilter.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
canfilter.list \

OBJCOPY_BIN += \
canfilter.bin \


# All Target
all: canfilter.elf secondary-outputs

# Tool invocations
canfilter.elf: $(OBJS) $(USER_OBJS) /home/eko/STM32CubeIDE/workspace_1.2.0/canfilter/STM32F105RBTX_FLASH.ld
	arm-none-eabi-gcc -o "canfilter.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/eko/STM32CubeIDE/workspace_1.2.0/canfilter/STM32F105RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="canfilter.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

canfilter.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "canfilter.list"
	@echo 'Finished building: $@'
	@echo ' '

canfilter.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "canfilter.bin"
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
