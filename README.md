# NFC-Digital-Business-Card-
# NFC Digital Business Card

## Hardware Schematic

The hardware schematic shown below represents the complete electrical design of the NFC Digital Business Card prototype. The system is built around the ESP32 microcontroller, which serves as the main processing unit responsible for handling NFC communication, Wi-Fi connectivity, and communication with the backend server.

The power management section includes a low-dropout (LDO) voltage regulator that converts the battery voltage into a stable 3.3V supply required by the ESP32 and all peripheral circuits. A dedicated battery charging circuit allows the rechargeable lithium battery to be charged safely through the USB connector while protecting it against overcharging.

The schematic also integrates a battery monitoring circuit that continuously measures the battery voltage, enabling the firmware to detect the remaining battery capacity and notify the user when charging is required.

The NFC section contains the NFC interface used for wireless communication with smartphones. Once a phone is brought near the device, the ESP32 reads or writes NFC data and establishes communication with the backend server to display the user's digital profile instantly.

This schematic represents the first stage of the hardware development process and provides the electrical connections between all major system components before PCB layout and manufacturing.

<img width="463" height="317" alt="schematic png" src="https://github.com/user-attachments/assets/dccb4cc5-402d-4f72-a09f-9087bed7c0b9" />

## PCB Top View

The following image illustrates the top view of the printed circuit board (PCB) designed for the NFC Digital Business Card prototype. The layout has been carefully organized to achieve compact dimensions while maintaining efficient routing between all electronic components.

The ESP32 development board is positioned on one side of the PCB to provide easy programming access through the USB connector. The NFC module is placed near the center of the board to maximize reading performance and reduce interference from surrounding components.

The power management circuit, including the charging module, voltage regulation stage, filtering capacitors, and DC input connector, is grouped together to minimize electrical noise and improve overall system stability.

The PCB layout also considers future manufacturing by maintaining proper component spacing, routing clearance, and accessibility for assembly and maintenance.


<img width="787" height="473" alt="pcb-top png" src="https://github.com/user-attachments/assets/d7d63cd3-64d1-47bc-8e6e-e8f67ece843f" />

## PCB 3D Assembly

The 3D assembly view demonstrates the final arrangement of all electronic components after PCB design. This visualization helps verify the mechanical compatibility between modules before manufacturing.

It allows inspection of component heights, spacing, connector accessibility, and overall board appearance while ensuring that no physical interference exists between components.

The model provides a realistic representation of the final prototype, simplifying the manufacturing and assembly process.
<img width="837" height="426" alt="pcb-3d png" src="https://github.com/user-attachments/assets/6d80f9d5-c778-4f1b-acfd-6b54cf3bc0a5" />


## Side View

The side view highlights the vertical arrangement of the ESP32 development board, NFC module, and power circuitry. This perspective is useful for checking component clearance, connector accessibility, and enclosure compatibility before fabrication.

It also verifies that sufficient spacing exists between stacked modules, reducing the possibility of mechanical conflicts during assembly.

<img width="700" height="442" alt="pcb-side png" src="https://github.com/user-attachments/assets/e9f50633-44a6-4fb3-bc9c-ae37e15c44ce" />
