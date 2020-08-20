################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
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
UART_tutorial.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
UART_tutorial.list \

OBJCOPY_BIN += \
UART_tutorial.bin \


# All Target
all: UART_tutorial.elf secondary-outputs

# Tool invocations
UART_tutorial.elf: $(OBJS) $(USER_OBJS)
	arm-none-eabi-gcc -o "UART_tutorial.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 --specs=nosys.specs -Wl,-Map="UART_tutorial.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

UART_tutorial.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "UART_tutorial.list"
	@echo 'Finished building: $@'
	@echo ' '

UART_tutorial.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "UART_tutorial.bin"
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
