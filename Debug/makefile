################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include drivers/Src/subdir.mk
-include drivers/Inc/subdir.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
stm32f103xx_drivers.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
stm32f103xx_drivers.list \

OBJCOPY_HEX += \
stm32f103xx_drivers.hex \


# All Target
all: stm32f103xx_drivers.elf secondary-outputs

# Tool invocations
stm32f103xx_drivers.elf: $(OBJS) $(USER_OBJS) C:\Users\Metisai_02\STM32CubeIDE\workspace_1.0.2\stm32f103xx_drivers\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "stm32f103xx_drivers.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Metisai_02\STM32CubeIDE\workspace_1.0.2\stm32f103xx_drivers\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="stm32f103xx_drivers.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

stm32f103xx_drivers.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "stm32f103xx_drivers.list"
	@echo 'Finished building: $@'
	@echo ' '

stm32f103xx_drivers.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "stm32f103xx_drivers.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
