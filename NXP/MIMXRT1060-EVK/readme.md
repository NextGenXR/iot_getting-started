---
page_type: sample
description: Connecting an NXP MIMXRT1060-EVK device to Azure IoT using Azure RTOS
languages:
- c
products:
- azure-iot
- azure-iot-pnp
- azure-rtos
- azure-iot-central
---

# Connect an NXP MIMXRT1060-EVK Evaluation kit to Azure IoT

[![Quickstart article](../../docs/media/docs-link-buttons/azure-quickstart.svg)](https://learn.microsoft.com/azure/iot-develop/quickstart-devkit-nxp-mimxrt1060-evk-iot-hub)
[![Documentation](../../docs/media/docs-link-buttons/azure-documentation.svg)](https://docs.microsoft.com/azure/iot-develop/)

The **Quickstart** button above provides the complete steps for creating an IoT Hub application and then configuring, building and flashing the device.

For guidance on connecting additional devices, see [Get started with IoT device development](https://learn.microsoft.com/azure/iot-develop/about-getting-started-device-development).

## What you need

* The [NXP MIMXRT1060-EVK Evaluation kit](https://www.nxp.com/design/development-boards/i-mx-evaluation-and-development-boards/mimxrt1060-evk-i-mx-rt1060-evaluation-kit:MIMXRT1060-EVK)
* USB 2.0 A male to Micro USB male cable
* Wired Ethernet access
* Ethernet cable

## Steps

1. Recursively clone the repository:
    ```shell
    git clone --recursive https://github.com/azure-rtos/getting-started.git
    ```

1. Install the development tools:

    *getting-started\tools\get-toolchain.bat*

1. Add Azure IoT configuration to the config file:
    
    *getting-started\NXP\MIMXRT1060-EVK\app\azure_config.h*
    
1. Build the binary image:

    *getting-started\NXP\MIMXRT106-EVK\tools\rebuild.bat*

1. Flash the image to the device by copying the image file to the **RT1060-EVK** drive:

    *getting-started\NXP\MIMXRT106-EVK\build\app\mimxrt1060_azure_iot.bin*

1. Configure a serial port app at baud rate **115,200** to monitor the device output.
