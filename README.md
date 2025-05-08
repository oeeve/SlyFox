<a name="readme-top"></a>

<div align="center">
  <a href="https://github.com/oeeve/SlyFox">
    <img src="media/Fox_b.webp" alt="Logo" width="450"> </a> <br>
    <a href="https://doi.org/10.5281/zenodo.15364530"><img src="https://zenodo.org/badge/979958196.svg" alt="DOI"></a>
  </a>
<br><br>
  <p align="center">
    <a href="#about"><strong>About</strong></a>
    ·
    <a href="#download"><strong>Download & Use</strong></a>
    ·
    <a href="#schematic"><strong>Schematic & Layout</strong></a>
    ·
    <a href="#renders"><strong>Renders</strong></a>
    ·
    <a href="#Software"><strong>Software</strong></a>
  </p>
</div>




<!-- ABOUT -->
<a name="about"></a>
## SlyFox IoT Sleuth 
Part of UC3BPR20 2025 - Acquisition and Analysis of Forensic Artefacts in a Smart Home Environment: A Study in IoT Forensics.

The [SlyFox IoT Sleuth (SFHPCBA01)](https://github.com/oeeve/SlyFox) prototype has been developed as a forensic acquisition tool for Homey Pro (and other RPI CM4-based devices), based on the acquisition process described in [github.com/oeeve/UC3BPR20](https://github.com/oeeve/UC3BPR20).

A comprehensive IoT forensics dataset based on a purpose-built testbed consisting of the Homey Pro (2023), the Homey Android application and a selection of Zigbee sensors and acutators has been made available at [github.com/oeeve/UC3BPR20](https://github.com/oeeve/UC3BPR20) to support future research, training, and testing in IoT forensics.

<figure>
  <img src="media/4_deliverables_flow.webp" alt="SlyFox">
  <figcaption>Figure 1: SlyFox IoT Sleuth project deliverables, including the
    <a href="https://github.com/oeeve/UC3BPR20">IoT forensics dataset</a>.</figcaption>
</figure>
<p>&nbsp;</p>




<!-- DOWNLOAD & USE -->
<a name="download"></a>
## Download & Use

### Download

| Application  | SHA-256 |
| ----------- | -------------- |
| [![Download](https://custom-icon-badges.demolab.com/badge/Ubuntu:-SlyFoxIoT.deb_(TBA)-B58DAE?style=flat&logo=download&logoColor=white)](https://github.com/oeeve/UC3BPR20) | `TBA` |

### Installation
**TBA**


### Use
**TBA**




<!-- SCHEMATIC & LAYOUT -->
<a name="schematic"></a>
## Schematic & Layout

### Block Diagram
<figure>
  <img src="media/4_block_diagram_3.webp" alt="SlyFox">
  <figcaption>Figur 2: Block diagrams. Left: PCB layout. Right: System diagram.</figcaption>
</figure>
<p>&nbsp;</p>


### Schematic
<figure>
  <img src="media/5_slyfox_hw_schematics_1.webp" alt="SlyFox">
  <figcaption>Figure 3: SlyFox IoT Sleuth (SFHPCBA01) carrier board for CM4. Based on reference design from <a href="https://datasheets.raspberrypi.com/cm4io/cm4iousb3-appnote.pdf">CM4IO</a>.</figcaption>
</figure>
<p>&nbsp;</p>


#### Bill of Materials

| ID     | Model                   | Description                                                                                                                                          | DS  |
| ------ | ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| P1, P2 | Hirose DF40C-100DS-0.4v | Hirose 100-pin connectors, used by the CM4.                                                                                                          | [1] |
| J1     | TE 2345986-1            | USB-C connector to interface with host / lab PC.                                                                                                     | [2] |
| SW1    | CL-SB-12B               | Latching-switch to pull \texttt{nRPIBOOT} to ground and force eMMC USB boot.                                                                         | [3] |
| R4 R5  | ERJ-UP6D5101V           | 0603 5k1 pulldown resistors. Set to keep CC1 and CC2 on J1 permanent low. This configuration defines J1 as a device-only, USB 2.0 only interface.    | [4] |
| C1     | EEH-ZK1V331P            | 330 µF electrolyte PHA capacitor. Inrush protection and bulk decoupling on VBUS, required on USB downstream devices.                                 | [5] |
| U1     | 74LVC1G07               | Open drain and voltage-level controller. When `PI_LED_nPWR` is low, it will pull to ground and activate LED 1 / 2.                                   | [6] |
| LED1   | SML-E12RWT86            | 0603 LED. Connected to U1 and `PI LED nPWR` CM4's power signal. Lights red when CM4 is powered on.                                                   | [7] |
| LED2   | SML-E12GWT86            | 0603 LED. Connected to U2 and `PI nLED Activity` CM4's storage access indicator, blinking green when the eMMC is read or written to.                 | [7] |
| LED3   | SML-E12GWT86            | 0603 LED. Connected to ground through SW1, and lights green when \texttt{nRPIBOOT} is pulled low, thus set in USB boot mode.                         | [7] |

[1]: https://www.hirose.com/product/p/CL0684-4033-4-51
[2]: https://www.te.com/en/product-2345986-1.html
[3]: https://www.nidec-components.com/e/catalog/switch/cl-sb.pdf
[4]: https://api.pim.na.industrial.panasonic.com/file_stream/main/fileversion/4484
[5]: https://industrial.panasonic.com/sa/products/pt/hybrid-aluminum/models/EEHZK1V331P
[6]: https://www.ti.com/lit/ds/symlink/sn74lvc1g07.pdf
[7]: https://www.farnell.com/datasheets/4410072.pdf
<br>



### PCB Layout
<figure>
  <img src="media/5_slyfox_hw_pcb_1.webp" alt="SlyFox">
  <figcaption>Figure 4: PCB - Top.</figcaption>
</figure>
 <p>&nbsp;</p>




<!-- RENDERS -->
<a name="renders"></a>
## PCB Renders

<figure>
  <img src="media/5_slyfox_hw_4.webp" alt="SlyFox">
  <figcaption>Figure 5: PCBA - Top and Front.</figcaption>
</figure>
 <p>&nbsp;</p>

<figure>
  <img src="media/5_slyfox_hw_5.webp" alt="SlyFox">
  <figcaption>Figure 6: PCBA - Isometric.</figcaption>
</figure>
<p>&nbsp;</p>

<figure>
  <img src="media/5_slyfox_hw_6.webp" alt="SlyFox">
  <figcaption>Figure 7: PCBA + CM4 - Side.</figcaption>
</figure>
<p>&nbsp;</p>

<figure>
  <img src="media/5_slyfox_hw_7.webp" alt="SlyFox">
  <figcaption>Figure 8: PCBA + CM4 - Isometric.</figcaption>
</figure>
<p>&nbsp;</p>




<!-- SOFTWARE -->
<a name="software"></a>
## Software

**TBA**

<figure>
  <img src="media/4_app_concept.webp" alt="SlyFox" width="600">
  <figcaption>Figure 9: App concept (GUI).</figcaption>
</figure>
<p>&nbsp;</p>



---

<p align="right">(<a href="#readme-top">back to top</a>)</p>


`Until next time...`
<br>

  <a href="https://oddweb.io">
    <img src="media/oddscull_the_engineer.webp" alt="Logo" width="200">
  </a>