# can-hat

can hat design for raspberry pis

The canonical repo for this is hosted on tangled over at [`dunkirk.sh/can-hat`](https://tangled.org/dunkirk.sh/can-hat)

## BOM

| Component | LCSC # | Qty | Placement |
|---|---|---|---|
| MCP2518FDT-H/SL | C626759 | 3 | Hand solder |
| MCP2562FDT-E/SN | C511335 | 3 | Hand solder |
| OVETGLJANF-40MHZ | C295515 | 3 | Hand solder |
| AT24C32D-SSHM-T | search LCSC | 1 | Hand solder |
| 100nF 0603 X7R | basic | ~10 | PCBA |
| 10µF 0805 | basic | 2 | PCBA |
| 120Ω 0603 | basic | 3 | PCBA |
| 10kΩ 0603 | basic | 6 | PCBA |
| 3.9kΩ 0603 | basic | 2 | PCBA |
| 15EDGVC-3.5-02P (header) | search Degson | 3 | Hand solder |
| 15EDGKNM-3.5-02P (plug) | search Degson | 3 | Wire side |
| 2×20 stacking header | — | 1 | Hand solder |

The AT24C32D write-protect pin should have a jumper pad or test point so it can be pulled low to flash, then left pulled high permanently after.

<p align="center">
    <img src="https://raw.githubusercontent.com/taciturnaxolotl/carriage/main/.github/images/line-break.svg" />
</p>

<p align="center">
    <i><code>&copy; 2026-present <a href="https://dunkirk.sh">Kieran Klukas</a></code></i>
</p>

<p align="center">
    <a href="https://tangled.org/dunkirk.sh/can-hat/blob/main/LICENSE.md"><img src="https://img.shields.io/static/v1.svg?style=for-the-badge&label=License&message=CERN-OHL-S%20v2&logoColor=d9e0ee&colorA=363a4f&colorB=b7bdf8"/></a>
</p>
