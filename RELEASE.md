### PMG1S3DUAL BSP
The PMG1S3DUAL BSP enables you to design and develop embedded USB-C Power Delivery (PD) applications for the PMG1-S3 device (CYPM1322-97BZXIT). The application note **AN235644 - USB PD DRP (dual-role power) schematics using EZ-PD™ PMG1 MCUs**  provides a detailed information to design products which can provide/consume a high voltage power to/from USB PD port.

NOTE: BSPs are versioned by family. This means that version 1.2.0 of any BSP in a family (eg: PSoC™ 6) will have the same software maturity level. However, not all updates are necessarily applicable for each BSP in the family so not all version numbers will exist for each board. Additionally, new BSPs may not start at version 1.0.0. In the event of adding a common feature across all BSPs, the libraries are assigned the same version number. For example if BSP_A is at v1.3.0 and BSP_B is at v1.2.0, the event will trigger a version update to v1.4.0 for both BSP_A and BSP_B. This allows the common feature to be tracked in a consistent way.

### What's Included?
The PMG1S3DUAL library includes the following:
* BSP specific makefile to configure the build process for the board
* cybsp.c/h files to initialize the board and any system peripherals
* cybsp_types.h file describing basic board setup
* Linker script & startup code for GCC, IAR, and ARM toolchains
* Configurator design files (and generated code) to setup board specific peripherals
* .lib file references for all dependent libraries
* API documentation

### What Changed?
#### v3.2.0
* Added functionality to enable BSP Assistant chip flow
* Added capabilities to match BSPS created by BSP Assistant chip flow
#### v3.1.0
* Add macro `CYBSP_USER_BTN_DRIVE` indicating the drive mode that should be used for user buttons
#### v3.0.0
Note: This revision is only compatible with ModusToolbox Tools 3.0 and newer.
* Removed default dependency on HAL and CAPSENSE™ middleware. If either is needed they can be added to the application using the library manager.
* Updated recipe-make, core-make, and PDL to new major versions
* Regenerated code with Configurators from ModusToolbox™ v3.0.0
* Renamed top level board makefile to bsp.mk
* Removed version.xml file in favor of new props.json
#### v2.0.0
* Updated to HAL dependency to v2.0.0
* Updated CAPSENSE™ dependency to v3.0.0
* Regenerated code with Configurators from ModusToolbox™ v2.4.0
#### v1.2.0
* Added SysClk power management callback
* Minor branding updates
#### v1.1.0
* Updated configuration to include power settings
* Minor documentation updates
#### v1.0.0
* Initial production release
#### v0.5.0
* Initial pre-production release

### Supported Software and Tools
This version of the PMG1S3DUAL BSP was validated for compatibility with the following Software and Tools:

| Software and Tools                        | Version |
| :---                                      | :----:  |
| ModusToolbox™ Software Environment        | 3.1.0   |
| GCC Compiler                              | 12.2.1  |
| IAR Compiler                              | 9.30.1  |
| ARM Compiler                              | 6.16    |

Minimum required ModusToolbox™ Software Environment: v3.0.0

### More information
* [PMG1S3DUAL BSP API Reference Manual][api]
* [PMG1S3DUAL Documentation](https://www.infineon.com/dgdl/Infineon-USB_PD_DRP_dual-role_power_schematics_using_EZ-PD_PMG1_MCUs-ApplicationNotes-v02_00-EN.pdf?fileId=8ac78c8c83cd30810183ea6518841d1e)
* [Cypress Semiconductor, an Infineon Technologies Company](http://www.cypress.com)
* [Infineon GitHub](https://github.com/infineon)
* [ModusToolbox™](https://www.cypress.com/products/modustoolbox-software-environment)

[api]: https://infineon.github.io/TARGET_PMG1S3DUAL/html/modules.html

---
© Cypress Semiconductor Corporation (an Infineon company) or an affiliate of Cypress Semiconductor Corporation, 2019-2022.