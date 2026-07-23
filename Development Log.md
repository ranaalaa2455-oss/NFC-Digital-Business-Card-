# Development Log

## Firmware Progress #2 – Wi-Fi Connectivity

The second stage of the firmware has been successfully completed.

After verifying that the ESP32 boots correctly, Wi-Fi connectivity has been implemented. The device now automatically attempts to connect to the configured wireless network immediately after startup.

During the connection process, the onboard LED blinks continuously to indicate that the device is attempting to connect to the Wi-Fi network. At the same time, the Serial Monitor displays:

Connecting to WiFi...

Once the connection is established successfully, the device prints:

WiFi Connected Successfully
IP Address: 10.10.0.2
Device Ready

This confirms that the ESP32 is connected to the network and ready to communicate with the backend server.

After initialization, the firmware enters its normal idle state and continuously displays:

Waiting for New Receipt...

This indicates that the device is waiting for the backend server to send a new receipt link or token.

The next development step is integrating the ESP32 with the backend server using either HTTP or MQTT. After receiving the receipt data, the firmware will store it and write it to the NFC tag, allowing customers to retrieve their digital receipt instantly by tapping their smartphone on the NFC device.

<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/1475e18d-a4cf-45df-ab9c-b60baa479b23" />


## Firmware Progress #1 – Initial Firmware Boot

The first stage of the firmware development has been successfully completed using Wokwi as a simulation environment before deploying the code to the physical ESP32 hardware.

The main objective of this stage was to verify that the firmware environment was configured correctly and that the ESP32 boot process executed successfully.

Inside the `setup()` function, the Serial Monitor is initialized at 115200 baud for debugging purposes. The onboard LED is then configured as an output pin, followed by printing the device information, including the device name, firmware version, and a **"Boot OK"** message to confirm that the startup sequence has completed successfully.

Inside the `loop()` function, the onboard LED blinks every 500 ms to simulate that the device is running normally. At the same time, the firmware continuously prints:

Waiting for Receipt...

This represents the device's idle state, indicating that it is ready and waiting to receive a new digital receipt from the backend server.

This milestone confirms that the basic firmware structure is operating correctly and provides a solid foundation for the upcoming development stages.

The next step is implementing Wi-Fi connectivity, followed by server communication (HTTP or MQTT), receiving receipt data, and finally writing the receipt URL or secure token to the NFC tag.
<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/de06dced-479f-4daa-9cc0-1dd867061240" />

## Firmware Progress #2 – Wi-Fi Connectivity & Receipt Simulation

The second stage of the firmware development has been successfully completed and validated using Wokwi.

At startup, the ESP32 performs the boot sequence and automatically attempts to connect to the configured Wi-Fi network. During the connection process, the onboard LED blinks continuously to indicate that the device is trying to establish a network connection. At the same time, the Serial Monitor displays:

Connecting to WiFi...

Once the connection is established successfully, the firmware prints:

WiFi Connected Successfully

IP Address: 10.10.0.2

Device Ready

This confirms that the ESP32 is connected to the network and ready to communicate with the backend server.

After the initialization process, a simulated server communication is performed. The firmware checks for a new digital receipt and receives a sample receipt URL, which is stored in the `receiptURL` variable.

The Serial Monitor then displays:

New Receipt Received!

Once a receipt has been received, the device enters a waiting state and continuously displays:

Waiting Customer Tap...

This simulates the normal operating mode of the NFC receipt device, where it waits for the customer to tap their smartphone on the NFC tag to access the digital receipt.

At this stage, the receipt URL is simulated for testing purposes. In the next development phase, the simulated data will be replaced with real-time data received from the backend server using MQTT. The received receipt URL or secure token will then be written directly to the NFC tag, allowing customers to open their digital receipt instantly with a single tap.
<img width="1600" height="899" alt="image" src="https://github.com/user-attachments/assets/c920ff31-7b13-485d-b88c-d475916dccef" />

