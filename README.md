# PMG1S3DUAL BSP

## Overview

The PMG1S3DUAL BSP enables you to design and develop embedded USB-C Power Delivery (PD) applications for the PMG1-S3 device (CYPM1322-97BZXIT). The application note **AN235644 - USB PD DRP (dual-role power) schematics using EZ-PD™ PMG1 MCUs**  provides a detailed information to design products which can provide/consume a high voltage power to/from USB PD port.



To use code from the BSP, simply include a reference to `cybsp.h`.

## Features

### Key Features:

* USB PD 3.1 compliant DRP on both the ports.
* EPR (Extended Power Range) which can support up to 140W (28V, 5A) power on both ports.
* USB Type-C alternate mode support.
* USB bus powered operation.
* SWD based programming and debug interface.

## BSP Configuration

The BSP has a few hooks that allow its behavior to be configured. Some of these items are enabled by default while others must be explicitly enabled. Items enabled by default are specified in the PMG1S3DUAL.mk file. The items that are enabled can be changed by creating a custom BSP or by editing the application makefile.

Components:
* Device specific category reference (e.g.: CAT1) - This component, enabled by default, pulls in any device specific code for this board.

Defines:
* CYBSP_WIFI_CAPABLE - This define, disabled by default, causes the BSP to initialize the interface to an onboard wireless chip if it has one.
* CY_USING_HAL - This define, enabled by default, specifies that the HAL is intended to be used by the application. This will cause the BSP to include the applicable header file and to initialize the system level drivers.
* CYBSP_CUSTOM_SYSCLK_PM_CALLBACK - This define, disabled by default, causes the BSP to skip registering its default SysClk Power Management callback, if any, and instead to invoke the application-defined function `cybsp_register_custom_sysclk_pm_callback` to register an application-specific callback.

### Clock Configuration

| Clock    | Source    | Output Frequency |
|----------|-----------|------------------|
| CLK_HF   | CLK_IMO   | 48 MHz           |

### Power Configuration

* System Idle Power Mode: Deep Sleep
* VDDA Voltage: 3300 mV
* VDDD Voltage: 3300 mV

See the [BSP Setttings][settings] for additional board specific configuration settings.

## API Reference Manual

The PMG1S3DUAL Board Support Package provides a set of APIs to configure, initialize and use the board resources.

See the [BSP API Reference Manual][api] for the complete list of the provided interfaces.

## More information
* [PMG1S3DUAL BSP API Reference Manual][api]
* [PMG1S3DUAL Documentation](https://www.infineon.com/dgdl/Infineon-USB_PD_DRP_dual-role_power_schematics_using_EZ-PD_PMG1_MCUs-ApplicationNotes-v02_00-EN.pdf?fileId=8ac78c8c83cd30810183ea6518841d1e)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_PMG1S3DUAL/html/modules.html
[settings]: https://infineon.github.io/TARGET_PMG1S3DUAL/html/md_bsp_settings.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2019-2022.