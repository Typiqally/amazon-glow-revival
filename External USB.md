# External USB
The external USB connection on the motherboard is identified by the reference designator `JUSB_EXT`. While its exact purpose is not immediately apparent, it appears to have been used for communicating with the device, potentially for tasks like software updates and configuration adjustments.

## Pinout
| External board | PCB | Description |     |
| -------------- | --- | ----------- |:---:|
| 3              | 1   | Ground      |     |
| 2              | 2   | 2.4V        | D-  |
| 5              | 3   |             | D+  |
| 3              | 4   | Ground      |     |
| 1              | 5   |             | TX- |
| 4              | 6   | 2.4V        | TX+ |
| 3              | 7   | Ground      |     |
| 6              | 8   |             | RX- |
| 6              | 9   |             | RX+ |

The pinout shares similarities with the USB 3.0 specification, albeit with a few minor differences. One notable distinction is the absence of the 5V power delivery typically present in other USB peripherals. It appears this feature was omitted due to its lack of necessity. Similarly, the two super-speed **receive** lines are not properly connected, raising the question of whether they serve an alternate purpose or were left unused intentionally.

Further testing is required to determine whether it is feasible to exploit this connection for potential access to the main board. For instance, it might be possible to establish an ADB connection, enabling shell access and the installation of third-party applications.