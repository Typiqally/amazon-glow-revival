Author(s): Jelle Maas
Dated: 2nd of November
# Amazon Glow Revival
The Amazon Glow, a creation of Amazon, was introduced amid the Covid-19 pandemic with the aim of providing an entertaining way for children to engage with their family members at home. Regrettably, the product faced low demand, leading to its cancellation. To exacerbate the situation, Amazon issued an update, now referred to as the “kill update,” rendering all Amazon Glow devices useless and contributing to electronic waste.
## Objective
The Amazon Glow Revival (AGR) project is dedicated to resurrecting the Amazon Glow by reverse engineering its internal components and understanding its functionality. The primary objective of this initiative is to unlock the device's software, empowering developers to craft their own applications. Although not all Amazon Glow devices were affected by the kill update, a significant number of them were impacted. As part of the project, efforts are being made to reverse the effects of the update, aiming to revive bricked Amazon Glow devices and restore their functionality.

This repository functions as the central storage hub for all research findings. It also serves as a platform to document the various approaches taken, and the corresponding results obtained during the research process.
## Approaches
> It is crucial to explicitly acknowledge that the findings and information presented in this research might be incomplete. Given the intricate nature of the devices, it is not always possible to ascertain if all relevant information has been uncovered.

Reverse engineering a device such as the Amazon Glow poses significant challenges, resembling the exploration of a black box where inputs and outputs are observable, but the internal processes remain obscure. Adding to the complexity, there is limited information accessible about the Amazon Glow, primarily due to its short-lived presence in the open market.
### 1. Debug connector
The devices' main board has an unpopulated connector marked with the `JDBG` label, indicating that it is some kind of debugging connector. It may be possible to gain some kind of access from this connector, by figuring out what kinds of signals are sent over its data pins.
### 2. External USB board
Similar to the debug connector, the device also has pinout for an external USB board, which is connected to a breakout board on the outside of the device. It may be possible to gain some kind of access by exploiting this connector, again by figuring out what kinds of signals are sent over its data pins.
### 3. Wi-Fi sniffing and DNS spoofing
The Amazon Glow relies on a Wi-Fi connection for its proper operation. However, attempting to connect it to the internet can lead to the device becoming inoperable (bricking). Fortunately, it is possible to set up a local Wi-Fi connection and monitor the device's traffic. By doing so, it may be feasible to selectively allow certain connections to access the internet while blocking others.
## License
The Amazon Glow Revival project is licensed under the terms of MIT See [LICENSE](LICENSE) for details.