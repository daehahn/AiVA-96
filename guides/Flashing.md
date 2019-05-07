---
title: AiVA 96 Mezzanine Guides
permalink: /documentation/mezzanine/aiva-96/guides/
---

# AiVA-96 Firmware Flashing Guide

# 1) Introduction

WizeIoT AiVA-96 mezzanine board for DragonBoard 410c and 96Boards using the XMOS XVF3000 voice processor. It may need to update of it's firmware later. This document provides general guide for how to flash your firmware.

# 2) Prerequisites

You will need:
- [XMOS's xTAG (JTAG) debug adapter](https://www.digikey.com/product-detail/en/xmos/XA-XTAG/XA-XTAG-ND/2183686)
- [XMOS's xTIMEcomposer 14.3.3 or later](https://www.xmos.com/software/tools)
- AiVA-96's xTAG connector, included in AiVA-96

<img src="../images/xTag-Adaptor.png?raw=true" data-canonical-src="../images/xTag-Adaptor.png?raw=true"/>

# 3) Hardware Setup

- Connect xTAG debugger to AiVA-96 xTAG adadtor.
- Place AiVA-96 board on top of a DragonBoard 410c (or any 96Boards).
- Place xTAG debugger into AiVA-96's xTAG connector.

<img src="../images/AiVA-xTag.png?raw=true" data-canonical-src="../images/AiVA-xTag.png?raw=true"/>

- Connector power into DragonBoard 410c
- Connector micro usb into xTAG debuuger from your computer.


# 4) Write Firmware

- Open 'Run SetEnv.command' (MacOS)

<img src="../images/xTimecomposer.png?raw=true" data-canonical-src="../images/xTimecomposer.png?raw=true"/>

- xTAG connectivity testing

    ```
    $ xflash -l
    ```

<img src="../images/SetEnv-command.png?raw=true" data-canonical-src=".../images/SetEnv-command.png?raw=true"/>

- Firmware flashing

    ```
    $ xflash --no-compression <filename>.xe
    ```