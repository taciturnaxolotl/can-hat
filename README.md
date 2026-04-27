# CANopy

![the main schematic](https://cdn.hackclub.com/019dc829-20e5-78ac-9db8-4ea4736f9ba4/CANopy.svg)
![the branch schematic](https://cdn.hackclub.com/019dc829-1d3c-7ace-a1cf-2922d84d61cc/CANopy_branch.svg)

The canonical repo for this is hosted on tangled over at [`dunkirk.sh/CANopy`](https://tangled.org/dunkirk.sh/CANopy)

## BOM

| Name | Purpose | Quantity | Total Cost (USD) | Distributor |
|---|---|---|---|---|
| [2×20 40-pin stacking female header](https://www.amazon.com/dp/B0827THC7R) | 15-16mm pin length to clear Pi 5 active cooler, hand solder | 1 | $9.90 | Amazon |
| [10kΩ 0603](https://www.lcsc.com/product-detail/C25803.html) | MCP2518FD RESET pull-up and MCP2562FD STBY pull-down, PCBA | 100 | $0.18 | LCSC |
| [1kΩ 0603](https://www.lcsc.com/product-detail/C21190.html) | EEPROM write-protect pull-up to 3.3V, PCBA | 100 | $0.16 | LCSC |
| [3.9kΩ 0603](https://www.lcsc.com/product-detail/C23196.html) | EEPROM SDA/SCL pull-ups to 3.3V, PCBA | 100 | $0.16 | LCSC |
| [120Ω 0603](https://www.lcsc.com/product-detail/C25879.html) | CAN bus termination resistors, one per channel, PCBA | 100 | $0.09 | LCSC |
| [10µF 0805](https://www.lcsc.com/product-detail/C15850.html) | Bulk caps for 3.3V and 5V rails, PCBA | 20 | $0.43 | LCSC |
| [1µF 0603 X5R](https://www.lcsc.com/product-detail/C15849.html) | Decoupling caps for all ICs, PCBA | 100 | $0.56 | LCSC |
| [15EDGRC-3.5-02P (plug & header)](https://www.lcsc.com/product-detail/C5632692.html) | PCB-side right-angle pluggable terminal block, 3.5mm pitch, 2-pin, hand solder | 10 | $3.21 | LCSC |
| [AT24C32D-SSHM-T](https://www.lcsc.com/product-detail/C60583.html) | 32Kbit I2C EEPROM for HAT ID, SOIC-8, hand solder | 5 | $1.48 | LCSC |
| [OVETGLJANF-40MHZ](https://www.lcsc.com/product-detail/C295515.html) | 40MHz active oscillator, 3.3V, SMD5032-4P, hand solder | 11 | $6.14 | LCSC |
| [MCP2562FDT-E/SN](https://www.lcsc.com/product-detail/C511335.html) | CAN FD transceiver with VIO pin, SOIC-8, hand solder | 11 | $12.87 | LCSC |
| [MCP2518FDT-H/SL](https://www.lcsc.com/product-detail/C626759.html) | CAN FD SPI controller, SOIC-14, hand solder | 11 | $27.07 | LCSC |

For use with the SystemCore the RSL can be emulated via the following

```python
# pseudocode
gpio = /sys/class/gpio/gpioXX/value
while True:
  enabled = read("/sys/kernel/can_heartbeat/enabledro")
  gpio.write(enabled)
  # add blink pattern logic for disabled state
  sleep(0.05)
```

### todo

- [ ] add testpoints on i2c and can rx/tx 0.1" header
- [ ] add termination resister jumper (dip switch block)
- [ ] add rsl mosfet switching ground
- [ ] [5v 5a pololu](https://www.pololu.com/product/2851)
- [ ] new screw blocks [DEGSON DG500-5.08-02P-14-00A(H)](https://www.lcsc.com/product-detail/C691859.html)

<p align="center">
    <img src="https://raw.githubusercontent.com/taciturnaxolotl/carriage/main/.github/images/line-break.svg" />
</p>

<p align="center">
    <i><code>&copy; 2026-present <a href="https://dunkirk.sh">Kieran Klukas</a></code></i>
</p>

<p align="center">
    <a href="https://tangled.org/dunkirk.sh/CANopy/blob/main/LICENSE.md"><img src="https://img.shields.io/static/v1.svg?style=for-the-badge&label=License&message=CERN-OHL-S%20v2&logoColor=d9e0ee&colorA=363a4f&colorB=b7bdf8"/></a>
</p>
