

# **Release Notes for STM32F7xx CMSIS**
Copyright &copy; 2019 STMicroelectronics\

[![ST logo](_htmresc/st_logo_2020.png)](https://www.st.com)



# __Update History__

<label for="collapse-section1_2_11" aria-hidden="true">__V1.2.11 / 27-October-2026__</label>
<div>

- Set default VTOR to the internal Flash base address if 'USER_VECT_TAB_ADDRESS' is not defined to ensure correct IRQ dispatch.
- Update the bit definitions for TSSO and TSTTR fields in the ETH PTPTSSR register.

</div>

<label for="collapse-section1_2_10" aria-hidden="true">__V1.2.10 / 25-April-2025__</label>
<div>

- Allow redefinition of the macro 'VECT_TAB_OFFSET' externally from the IDE, makefile, or command line.
- Fix Capture Compare register TIMx_CCR5 defintion.

</div>

<label for="collapse-section1_2_9" aria-hidden="true">__V1.2.9 / 10-May-2024__</label>
<div>

- Update GCC start-up files to call SystemInit() API @Reset_Handler step: alignment with EWARM and MDK-ARM start-up files.
- Update ETH bit definitions : Add CRC stripping for Type frames bit definition (CSFT).

</div>

<label for="collapse-section1_2_8" aria-hidden="true">__V1.2.8 / 29-April-2022__</label>
<div>

## Main Changes
- General updates to fix known defects and enhancements implementation.
- Update gcc start-up files to remove duplication for DMA2_Stream4_IRQHandler.

</div>

<label for="collapse-section1_2_7" aria-hidden="true">__V1.2.7 / 22-November-2021__</label>
<div>

## Main Changes
- General updates to fix known defects and enhancements implementation.
- All source files: update disclaimer to add reference to the new license agreement.

- **Headline**
  - Add new atomic register access macros in stm32f7xx.h file.
  - Add LSI maximum startup time datasheet value: LSI_STARTUP_TIME.
  - __FPU_PRESENT defined with 1U instead of 1 to avoid compilation warning.
  - Add "PTPPPSCR" register definition for Ethernet Peripheral.

</div>

<label for="collapse-section1_2_6" aria-hidden="true">__V1.2.6 / 12-February-2021__</label>
<div>

## Main Changes
  - Improved GCC startup files robustness.
  - Protect Vector table modification following SRAM or FLASH preprocessor directive by a generic preprocessor directive : USER_VECT_TAB_ADDRESS.
  - Added License.md and Readme.md files required for GitHub publication.
</div>

<label for="collapse-section1_2_5" aria-hidden="true">__V1.2.5 / 13-February-2020__</label>
<div>

## Main Changes
   - Add ADC missing calibration address for Vref and Temperature sensor.
   - Align GPIO Bits Definitions to use _POS and _MSK.
   - Add IS_UART_WAKEUP_FROMSTOP_INSTANCE macro for STM32F765xx, STM32F767xx, STM32F769xx,STM32F777xx and STM32F779xx devices.
   - Add missing USART Bits Definitions in USART_CR1, USART_CR3, USART_ISR and USART_ICR registers for STM32F765xx, STM32F767xx, STM32F769xx,STM32F777xx and STM32F779xx devices.
   - Add USB missing Bit Definition in USB_OTG_GUSBCFG register for STM32F722xx and STM32F732xx devices
   - Remove dublicated Bits Definitions for OTG register
   - Remove IS_TIM_SYNCHRO_INSTANCE macro.
</div>


<label for="collapse-section1_2_4" aria-hidden="true">__V1.2.4 / 08-February-2019__</label>
<div>

## Main Changes
- CRYP
   - Update CMSIS devices with correct CRYP data input register name: DIN instead of DR   
- SAI
   -Fix frame length in SAI_xFRCR_FSALL & SAI_xFRCR_FRL bits description
- USB
   - Add missing Bits Definitions in USB_OTG_DOEPMSK register
      - USB_OTG_DOEPMSK_AHBERRM
      - USB_OTG_DOEPMSK_OTEPSPRM
      - USB_OTG_DOEPMSK_BERRM
      - USB_OTG_DOEPMSK_NAKM
      - USB_OTG_DOEPMSK_NYETM
   - Add missing Bits Definitions in USB_OTG_DIEPINT register
      - USB_OTG_DIEPINT_INEPNM
      - USB_OTG_DIEPINT_AHBERR
      - USB_OTG_DOEPINT_OUTPKTERR
      -  USB_OTG_DOEPINT_NAK
      - USB_OTG_DOEPINT_STPKTRX
   - Add missing Bits Definitions in USB_OTG_DCFG register
      - USB_OTG_DCFG_XCVRDLY
      - USB_OTG_DCFG_ERRATIM
   - Add IS_PCD_ALL_INSTANCE() and IS_HCD_ALL_INSTANCE() defines
   - Remove GADPCTL parameter from USB_OTG_GlobalTypeDef() structure
   - Remove GPWRDN parameter from USB_OTG_GlobalTypeDef5° STRUCTURE
- DFSDM
   - Align Bit naming for DFSDM_FLTICR register: DFSDM_FLTICR_CLRSCSDF--> DFSDM_FLTICR_CLRSCDF
- CEC
   - Align Bit naming for CEC_RXDR register: CEC_TXDR_RXD--> CEC_RXDR_RXD
- QSPI
   - Update FLEVEL field in QuadSPI Status register definition to be compliant with user manual

</div>



<label for="collapse-section1_2_3" aria-hidden="true">__V1.2.3 / 29-June-2018__</label>
<div>

## Main Changes

- Add the support of __STM32F730xx and  STM32F750xx__  devices
    - Add "stm32f730xx.h" and "stm32f750xx.h" header files
    - Add startup files "startup_stm32f730xx.s" and "startup_stm32f750xx.s" for EWARM, MDK-ARM and SW4STM32 toolchains
    - Add Linker files "stm32f730xx_flash.icf", "stm32f730xx_sram.icf" and "stm32f730xx_ITCM_flash.icf" used within EWARM Workspaces
    - Add Linker files "stm32f750xx_flash.icf", "stm32f750xx_sram.icf" and "stm32f750xx_ITCM_flash.icf" used within EWARM Workspaces

</div>


<label for="collapse-section1_2_2" aria-hidden="true">__V1.2.2 / 26-December-2017__</label>
<div>

## Main Changes

- Update bits definition for USBPHYC_PLL1 and USBPHYC_LDO registers to be inline with products documentation.


</div>


<label for="collapse-section1_2_1" aria-hidden="true">__V1.2.1 / 25-August-2017__</label>
<div>

## Main Changes

- Update FLASHSIZE_BASE and UID_BASE defined values for STM32F72x and STM32F73x devices.
- Update stm32f7xx.h to include stm32f7xx_hal.h file instead of stm32f7xx_hal_conf.h file
- Remove Date and Version from header files


</div>


<label for="collapse-section1_2_0" aria-hidden="true">__V1.2.0 / 30-December-2016__</label>
<div>

## Main Changes

- Add the support of __STM32F722xx, STM32F723xx, STM32F732xx and STM32F733xx__ devices
   - Add "stm32f722xx.h", "stm32f723xx.h", "stm32f732xx.h" and "stm32f733xx.h" header files
   - Add startup files "startup_stm32f722xx.s", "startup_stm32f723xx.s", "startup_stm32f732xx.s" and "startup_stm32f733xx.s" for EWARM, MDK-ARM and SW4STM32 toolchains
   - Add Linker files "stm32f722xx_flash.icf", "stm32f722xx_sram.icf" and "stm32f722xx_ITCM_flash.icf" used within EWARM Workspaces
   - Add Linker files "stm32f723xx_flash.icf", "stm32f723xx_sram.icf" and "stm32f723xx_ITCM_flash.icf" used within EWARM Workspaces
   - Add Linker files "stm32f732xx_flash.icf", "stm32f732xx_sram.icf" and "stm32f732xx_ITCM_flash.icf" used within EWARM Workspaces
   - Add Linker files "stm32f733xx_flash.icf", "stm32f733xx_sram.icf" and "stm32f733xx_ITCM_flash.icf" used within EWARM Workspaces
- All devices header files
   - Use _Pos and _Mask macro for all Bit Definitions
   - Use DAC1 instance instead of DAC
   - Add IS_SMBUS_ALL_INSTANCE macro
   - Add ADC123_COMMON instance
   - Add DMA_SxPAR_PA, DMA_SxM0AR_M0A and DMA_SxM1AR_M1A registers Bits Definition
   - Add DBGMCU_APB1_FZ_DBG_LPTIM1_STOP and DBGMCU_APB1_FZ_DBG_I2C4_SMBUS_TIMEOUT Bits Definition
   - Add FLASH_OTP_BASE and FLASH_OTP_END defines
   - Add MACDBGR register Bits Definition
   - Add GPIO_AFRL and GPIO_AFRH registers Bits Definition 
   - Add TIM2_OR, TIM5_OR and TIM11_OR registers Bits Definition
   - Add TIM1_AF1_BKINP Bit Definition for TIM1_AF1 register
   - Add IS_TIM_32B_COUNTER_INSTANCE, IS_TIM_BREAK_INSTANCE, IS_TIM_BREAKSOURCE_INSTANCE and IS_TIM_BKIN2_INSTANCE, IS_TIM_CLOCK_DIVISION_INSTANCE, IS_TIM_REPETITION_COUNTER_INSTANCE, IS_TIM_CLOCKSOURCE_ETRMODE1_INSTANCE, IS_TIM_CLOCKSOURCE_ETRMODE2_INSTANCE, IS_TIM_HALL_SENSOR_INTERFACE_INSTANCE and IS_TIM_COMMUTATION_EVENT_INSTANCE macros
   - Add IS_USART_AUTOBAUDRATE_DETECTION_INSTANCE, IS_UART_HALFDUPLEX_INSTANCE and IS_UART_LIN_INSTANCE macros
   - Remove TIM_SMCR_OCCS Bit Definition for TIM_SMCR register
   - Remove USART_ISR_WUF and USART_ISR_REACK Bits Definition from USART_ISR register
   - Rename USART_CR1_M_0 / USART_CR1_M_1 defines to USART_CR1_M0 / USART_CR1_M1
   - Rename PACKAGESIZE_BASE define to PACKAGE_BASE
   - Rename RTC_OR_ALARMTYPE Bit Definition to RTC_OR_ALARMOUTTYPE
   - Rename RTC_CR_BCK Bit Definition to RTC_CR_BKP in RTC_CR register


</div>

<label for="collapse-section1_1_1" aria-hidden="true">__V1.1.1 / 01-July-2016__</label>
<div>

## Main Changes

- stm32f7xx.h
   - update to respectively associate STM32F778xx and STM32F768xx devices to STM32F779xx and STM32F769xx devices


</div>

<label for="collapse-section1_1_0" aria-hidden="true">__V1.1.0 / 22-April-2016__</label>
<div>

## Main Changes

- Add the support of __STM32F765xx, STM32F767xx, STM32F768xx, STM32F769xx, STM32F777xx, STM32F778xx and STM32F779xx__ devices
   - Add "stm32f765xx.h", "stm32f767xx.h", "stm32f769xx.h", "stm32f777xx.h" and "stm32f779xx.h" header files
   - Add startup files "startup_stm32f765xx.s", "startup_stm32f767xx.s", "startup_stm32f769xx.s", "startup_stm32f777xx.s" and "startup_stm32f779xx.s" for EWARM, MDK-ARM and SW4STM32 toolchains
   - Add Linker files "stm32f765xx_flash.icf", "stm32f765xx_sram.icf" and "stm32f765xx_ITCM_flash.icf" used within EWARM Workspaces
   - Add Linker files "stm32f767xx_flash.icf", "stm32f767xx_sram.icf" and "stm32f767xx_ITCM_flash.icf" used within EWARM Workspaces
   - Add Linker files "stm32f769xx_flash.icf", "stm32f769xx_sram.icf" and "stm32f769xx_ITCM_flash.icf" used within EWARM Workspaces
   - Add Linker files "stm32f777xx_flash.icf", "stm32f777xx_sram.icf" and "stm32f777xx_ITCM_flash.icf" used within EWARM Workspaces
   - Add Linker files "stm32f779xx_flash.icf", "stm32f779xx_sram.icf" and "stm32f779xx_ITCM_flash.icf" used within EWARM Workspaces
   - STM32F768xx cmsis files are associated with STM32F767xx ones, as there is no difference between these devices on HAL side
   - STM32F778xx cmsis files are associated with STM32F777xx ones, as there is no difference between these devices on HAL side
- All devices header files
   - Update Bit Definition names in DCMI_RISR / DCMI_IER registers
   - Update Bit Definition names in DMA2D_CR / DMA2D_FGPFCCR / DMA2D_BGPFCCR / DMA2D_OPFCCR registers
   - Update QUADSPI_CR_FTHRES Bit Definition in QUADSPI_CR register
   - Rename SAI_xFRCR_FSPO to SAI_xFRCR_FSPOL in SAI_xFRCR register
   - Rename ADC_CSR_DOVRx Bit Definition to ADC_CSR_OVRx in ADC_CSR register
   - Rename LTDC_GCR_DTEN Bit Definition to LTDC_GCR_DEN in LTDC_GCR register
   - Rename PWR_CSR1_UDSWRDY Bit Definition to PWR_CSR1_UDRDY in PWR_CSR1 register
   - Rename RTC_TAMPCR_TAMPx_TRG Bit Definition to RTC_TAMPCR_TAMPxTRG in RTC_TAMPCR register
   - Rename USART_ISR_LBD Bit Definition to USART_ISR_LBDF in USART_ISR register
   - Rename IS_SAI_BLOCK_PERIPH macro to IS_SAI_ALL_INSTANCE
   - Rename DCMI_ICR_OVF_ISC Bit Definition to DCMI_ICR_OVR_ISC
   - Rename DMA2D_IFSR register to DMA2D_IFCR
   - Rename EXTI_IMR_MRx Bit Definition to EXTI_IMR_IM0x
   - Rename EXTI_EMR_MRx Bit Definition to EXTI_EMR_EMx
   - Fix LPTIM_CR_SNGSTRT Bit Definition value in LPTIM_CR register
   - Fix mask incorrect naming in DBGMCU_APB2_FZ register
   - Fix Bits Definition for SYSCFG_EXTICR4_EXTI13_PI and SYSCFG_EXTICR4_EXTI13_PJ
   - Add DAC_CR_DMAUDRIEx Bit Definition in DAC_CR register
   - Add a new mask EXTI_IMR_IM in EXTI bits definition: Interrupt Mask All
   - Add UID_BASE define for Unique ID register base address
   - Add FLASHSIZE_BASE define for register base address
   - Add PACKAGESIZE_BASE define for register base address
   - Add FLASH_SECTOR_TOTAL define for total Flash sector number
   - Add Bits Definition for DCMI_ESCR, DCMI_ESUR, DCMI_CWSTRT, DCMI_CWSIZE and DCMI_DR registers
   - Add PWR_CSR1_EIWUP Bit Definition in PWR_CSR1 register
   - Add IP version define for QSPI: QSPI_V1_0
   - Add IS_UART_DRIVER_ENABLE_INSTANCE macro
   - Apply an 'U' suffix to all constants of 'unsigned' type (MISRA-C 2004 rule 10.6)
   - Remove uint32_t cast in all defines
   - Remove DMA_SxCR_ACK Bit Definition in DMA_SxCR register
   - Remove I2C_CR1_SWRST / I2C_CR1_WUPEN Bit Definitions in I2C_CR1 register
   - Keep the same DCMI register names (RISR, MISR, CWSTRTR and CWSIZER) as F4 family
- system_stm32f7xx.c/.h files
   - Remove external memories configuration from the system_stm32f7xx.c common file (moved to Template Projects)
   - Add declaration of AHBPrescTable / APBPrescTable constant tables
- stm32f7xx.h
   - Rename __STM32F7xx_CMSIS_DEVICE_VERSION_xx defines to __STM32F7_CMSIS_VERSION_xx (MISRA-C 2004 rule 5.1)


</div>

<label for="collapse-section1_0_3" aria-hidden="true">__V1.0.3 / 13-November-2015__</label>
<div>

## Main Changes

- stm32f745xx.h, stm32f746xx.h and stm32f756xx.h files
   - update __CM7_REV with proper Cortex M7 core revision
   - update SAI_xCR2_CPL bit definition
   - update WWDG bits naming to be aligned with reference manual
   - rename I2C_CR1_DFN bit to I2C_CR1_DNF
   - remove OR register definition from LPTIM_TypeDef structure
- system_stm32f7xx.c
   - update SystemInit_ExtMemCtl() function implementation to allow simultaneous use of SDRAM and SRAM external memories


</div>



<label for="collapse-section1_0_2" aria-hidden="true">__V1.0.2 / 21-September-2015__</label>
<div>

## Main Changes

- stm32f745xx.h, stm32f746xx.h and stm32f756xx.h files
   - add new define USB_OTG_DOEPMSK_OTEPSPRM
   - add new define USB_OTG_DOEPINT_OTEPSPR


</div>

<label for="collapse-section1_0_1" aria-hidden="true">__V1.0.1 / 25-June-2015__</label>
<div>

## Main Changes

- stm32f745xx.h, stm32f746xx.h and stm32f756xx.h files
   - update IDR field declaration in CRC_TypeDef sructure
   - add I2C Own address 2 mask bits defininition in the I2C_OAR2 register
   - update SAI_xSR_FLVL_2 bit definition
- stm32f756xx.h file
   - rename HASH_STR_NBWx bits definition to HASH_STR_NBLWx
   - rename HASH_IMR_DINIM bit definition to HASH_IMR_DINIE
   - rename HASH_IMR_DCIM bit definition to HASH_IMR_DCIE


</div>



<label for="collapse-section1_0_0" aria-hidden="true">__V1.0.0 / 12-April-2019__</label>
<div>

## Main Changes

### First release

First official release for __STM32F756xx/746xx/745xx__ devices


</div>


For complete documentation on STM32 Microcontrollers </mark> ,
visit: http://www.st.com/stm32
*This release note uses up to date web standards and, for this reason, should not be opened with Internet
Explorer but preferably with popular browsers such as Google Chrome, Mozilla Firefox, Opera or Microsoft
Edge.*