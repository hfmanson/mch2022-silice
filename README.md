# mch2022-silice
Silice designs for the MCH2022 badge

For setting up Silice please refer [to its repository](https://github.com/sylefeb/Silice).

The Silice `bin/` directory has to be in the path, as well as yosys and nextpnr-ice40 (using latest versions is recommended).

## Building something

Connect the badge, enter the project directory (for instance `lcd_test`) and type `make`. Enjoy!

> The `qpsram_loader` directory contains a project to upload and download data to PSRAM from memory that will not automatically program the badge.

## Credits:
- Thanks to the FPGA badge team for fun, guidance and inspiring projects https://github.com/badgeteam/mch2022-firmware-ice40
- Thanks to the badge team for an awesome badge https://github.com/badgeteam/
- Not forgetting the FPGA upload tool: https://github.com/badgeteam/mch2022-tools
