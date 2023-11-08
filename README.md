Author(s): Jelle Maas
Dated: 2nd of November

# Amazon Glow Revival
The Amazon Glow, a creation of Amazon, was introduced amid the Covid-19 pandemic with the aim of providing an entertaining way for children to engage with their family members at home. Regrettably, the product faced low demand, leading to its cancellation. To exacerbate the situation, Amazon issued an update, now referred to as the “kill update,” rendering all Amazon Glow devices useless and contributing to electronic waste.

## Objective
The Amazon Glow Revival (AGR) project is dedicated to resurrecting the Amazon Glow by reverse engineering its internal components and understanding its functionality. The primary objective of this initiative is to unlock the device's software, empowering developers to craft their own applications. This gives rise to the following main research question: *“How can the Amazon Glow be exploited, such that third party apps can be executed on it?”*. Adding onto that, it is currently unsure how the drivers for the projector, camera's, buttons, etc. be used within the applications, which gives rise to the sub research question: *“How can third-party apps for the Amazon Glow make use of components such as the projector, camera's, buttons, etc.?”*

Furthermore, although not all Amazon Glow devices were affected by the kill update, a significant number of them were impacted. As part of the project, efforts are being made to reverse the effects of the update, aiming to revive bricked Amazon Glow devices and restore their functionality. This gives rise to another sub research question: *“How can already bricked Amazon Glow devices be restored to full functionality?”*

## Requirements
| #   | Requirement               | Description                                                                            | Priority |
| --- | ------------------------- | -------------------------------------------------------------------------------------- | -------- |
| 1   | Third-party apps          | Device can run third-party applications                                                | Must     |
| 2   | Application driver access | Applications can use the built-in drivers to access the projector, camera's, etc.      | Should   |
| 3   | Un-bricking               | It is possible to unbrick already bricked devices                                      | Could    |
| 4   | Custom operating system   | Device can run custom operating systems, such as, but not limited to, default Android  | Could    |
| 5   | Universal connectivity    | Applications can make use of external connectivity such as the external USB connection | Could    |
## Approaches
> It is crucial to explicitly acknowledge that the findings and information presented in this research might be incomplete. Given the intricate nature of the devices, it is not always possible to ascertain if all relevant information has been uncovered.

Reverse engineering a device such as the Amazon Glow poses significant challenges, resembling the exploration of a black box where inputs and outputs are observable, but the internal processes remain obscure. Adding to the complexity, there is limited information accessible about the Amazon Glow, primarily due to its short-lived presence in the open market.

The list provided outlines several potential approaches to be investigated during the reverse engineering process. It is important to acknowledge that this list is not exhaustive; additional methods may be explored as the process unfolds, and certain approaches do not produce the desired outcomes.

### 1. Debug connector
The devices' main board has an unpopulated connector marked with the `JDBG` reference designator, indicating that it is some kind of debugging connector. It may be possible to gain some kind of access from this connector, by figuring out what kinds of signals are sent over its data pins.

### 2. External USB board
Similar to the debug connector, the device also has pinout for an external USB board, which is connected to a breakout board on the outside of the device. It may be possible to gain some kind of access by exploiting this connector, again by figuring out what kinds of signals are sent over its data pins.

### 3. Wi-Fi sniffing and DNS spoofing
The Amazon Glow relies on a Wi-Fi connection for its proper operation. However, attempting to connect it to the internet can lead to the device becoming inoperable (bricking). Fortunately, it is possible to set up a local Wi-Fi connection and monitor the device's traffic. By doing so, it may be feasible to selectively allow certain connections to access the internet while blocking others.

## License
The Amazon Glow Revival project is licensed under the terms of MIT See [LICENSE](LICENSE) for details.