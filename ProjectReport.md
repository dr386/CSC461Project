# LG Wireless TV - 60 GHz Wireless Technology

## 1. Introduction of LG Wireless TV with 60GHz Technology

In a groundbreaking move within the consumer electronics industry, LG has unveiled its latest innovation - 97-inch LG SIGNATURE OLED M (model M3). It ensures reliable and high-quality transmission of 4K content at 120Hz refresh rate. Central to this innovation is the Zero Connect Box, a device designed to transmit large amounts of data wirelessly, thereby eliminating the clutter and constraints of physical cables [1]. This use of 60 GHz technology represents a bold foray into utilizing high-frequency wireless bands for consumer applications, providing an insight into the future of wireless technology in home entertainment.

Traditional home entertainment systems have often been limited by the need for physical connections, leading to reduced flexibility and increased complexity in setup and use. The advent of 60 GHz wireless technology marks a significant leap in overcoming these limitations. By harnessing the capabilities of 60 GHz Wireless, the Zero Connect Box can transmit data at extremely high speeds. It is an example of this paradigm shift, illustrating the practical applications and benefits of advanced wireless technology in everyday use.

However, the implementation of 60 GHz wireless technology is not without its challenges. The high frequency of 60 GHz signals means they have shorter range and are more susceptible to physical obstructions compared to lower frequency signals used in traditional Wi-Fi. This limitation necessitates innovative approaches in technology design and deployment to ensure reliable and efficient data transmission. Overcoming these hurdles is crucial for harnessing the full potential of 60 GHz wireless communication. By addressing these challenges, technologies like LG's Zero Connect Box can have the way for a more robust wireless experience. This sets the stage for exploring the specific technological solutions and advancements that make 60 GHz wireless communication a viable and superior choice for home entertainment systems.

## 2. Overview of 60GHz Wireless Technology

In this paper, I primarily focus on the key features of the 60GHz Wireless technology, particularly in the IEEE 802.11ad standard. 

1. High Bandwidth and Speed: This refers to the technology's ability to transmit large amounts of data quickly.
2. OFDM (Orthogonal Frequency-Division Multiplexing) Modulation: A method that efficiently uses the spectrum by dividing it into multiple frequency bands.
3. Dynamic Channel Time Allocation: A feature that optimizes channel usage based on current network demands.
4. Support for Beamforming: This technology enhances signal quality and range by directing the signal towards specific receivers.

## 3. Technical Details

The 60GHz wireless network, described in IEEE 802.11ad standard, shows specialness compared to other Wi-Fi standards.

### 3.1 **60 GHz Band and Gbps Throughput**

The standard leverages the wide availability of the 60 GHz band for unlicensed use, which allows for new technologies enabling high-speed Wi-Fi communication in this frequency band. This utilization is a major shift from traditional 2.4 and 5 GHz bands, requiring a rethinking of Wi-Fi operation and a transition from omnidirectional to directional wireless medium usage.

It can also provide multi-gigabit-per-second throughput. This high data rate capacity opens up new application scenarios for Wi-Fi users, such as instant wireless synchronization, high-speed media file exchange between mobile devices without a fixed network infrastructure, and wireless cable replacement for connections to high-definition wireless displays.

### 3.2 Physical Layer with OFDM Modulation

The 60 GHz wireless network introduces a sophisticated Physical Layer (PHY) which incorporates Orthogonal Frequency-Division Multiplexing (OFDM) modulation, a key aspect for achieving high-speed wireless communication. The 802.11ad standard defines three different PHY layers to cater to various application scenarios. 

The first type of physical layer is the control PHY. It is specifically optimized for operations with a low signal-to-noise ratio, particularly useful before the implementation of beamforming, which will be introduced later in this paper.

The next type is the Single Carrier (SC) PHY, which facilitates power-efficient and low-complexity transceiver implementation. This kind of PHYs are more likely to be implemented due to their lower complexity and energy consumption. The SC PHY offers a throughput of up to 4.62 Gb/s, with the lowest SC data rate being 385 Mb/s using BPSK modulation and a rate 1/2 code.

The third type is Orthogonal Frequency-Division Multiplexing (OFDM) PHY which is designed for maximum throughput, although with increased complexity and energy requirements. OFDM is a method of digital signal modulation in which a single data stream is split across multiple closely spaced frequencies to provide more efficient data transmission. It works by dividing a high-rate data stream into several lower-rate streams that are transmitted simultaneously over multiple  frequencies or subcarriers. The subcarriers are mathematically arranged in an orthogonal manner, which enables them to avoid interference by ensuring that their signals do not overlap [2]. The OFDM PHY utilizes 64-QAM and a rate 13/16 code to achieve the highest data rates of up to 6.75 Gb/s. This PHY type is particularly suited for stationary devices with fixed power supply and high throughput demands, like access points and wireless displays.

### 3.3 Dynamic Channel Time Allocation

Dynamic Channel Time Allocation (DCTA) is a key mechanism designed to optimize the allocation of channel time in a wireless network environment. DCTA is essentially an advanced form of polling-based channel access. It provides a high level of flexibility in resource allocation, where polled stations request channel time as opposed to just transmitting a single frame.

The allocation process involves the Primary Channel Point (PCP) or Access Point (AP) initiating a polling phase, during which it sends polling frames to each associated station. These stations respond with Service Period Requests (SPRs) for channel time. To prevent interference with dynamic allocations and ensure that the allocated channel time is used effectively, the PCP/AP makes use of extended frame duration fields. This extension causes other nodes that overhear a frame to assume that the channel is occupied until the time specified in the duration field. In essence, it signals to other stations to refrain from using the channel for the duration of the protected transmission, thereby avoiding potential collisions.

In figure 1, during a polling phase, channel time is allocated to different stations, and each allocation is preceded by a grant period. The channel protection points ensure that each allocation and the corresponding grant period are protected, allowing for a smooth and uninterrupted communication process between the PCP/AP and the stations.

![**Figure 1. Dynamic channel allocation [3].** ](images/fig1.gif)

**Figure 1. Dynamic channel allocation [3].** 

The advantages of DCTA is its ability to efficiently handle burst traffic, allow the network to react promptly to changes in traffic demand. Additionally, DCTA effectively addresses the challenges of directional communication. The dynamic allocation mechanism, when combined with the directional capabilities, helps to mitigate these challenges.

### 3.4 **Beamforming Training**

Beamforming is a technique used in wireless communications where an array of antennas emits the same signal at slightly different times. This technique is commonly employed in radar, sonar, seismology, wireless communications, and radio astronomy. Within 60 GHz wireless networks, beamforming utilizes increased antenna gain to counteract the higher attenuation characteristic of the 60 GHz band, thereby creating a highly directional signal focus.

Beamforming training is a process where communicating nodes agree on the optimal pair of receive and transmit sectors to optimize signal quality and throughput. This involves a discretized antenna azimuth that reduces the search space of possible antenna array configurations. The training process has two stages. The first stage, direct sector-level sweep (SLS), involves a sector matching to find an initial configuration. The second stage, beam refinement phase (BRP), allows for the refinement of these sectors, where antenna weight vectors varying from predefined sector patterns are evaluated to optimize transmissions on phased antenna arrays.

### 3.4.1 Sector-Level Sweep Phase (SLS)

The SLS phase aims to determine an initial coarse-grained antenna sector configuration, which is critical for establishing high-quality directional links. As shown in figure 2, each station during SLS acts once as a transmitter and once as a receiver. The station that transmits first is termed the initiator, and the second one is the responder. During SLS, two stations (initiator and responder) exchange a series of Sector Sweep (SSW) frames across different antenna sectors to identify the one providing the highest signal quality.

The SSW Feedback frame in figure 2 is sent by the responder to the initiator, containing information about the optimum antenna configuration based on the responder's sweep. Then it is acknowledged with an SSW-ACK by the responder. The feedback is essential for determining the best transmit and receive sectors for both the initiator and responder, ensuring optimal signal quality and throughput.

![**Figure 2. Sector-level sweep [3].**](images/fig2.gif)

**Figure 2. Sector-level sweep [3].**

Figure 3 shows the SLS execution process. In transmit sector sweep, frames are transmitted across different sectors while the receiver uses a quasi-omnidirectional pattern. The purpose is to identify the strongest transmit sector. Each frame is marked with an identifier for the used antenna and sector. In receive sector sweep, the transmitter maintains transmission on the same sector (the best-known sector) to test for the optimum receive sector at the receiver. This allows the identification of the strongest reception sector for the responder

![**********************Figure 3. Transmit and receive sector training [3].**********************](images/fig3.gif)

**********************Figure 3. Transmit and receive sector training [3].**********************

The goal of SLS is to establish an initial coarse-grained configuration of the antenna sectors. And devices are able to optimize their directional communication capabilities through the SLS process.

### 3.4.1 **Beam Refinement Phase (BRP)**

The Beam Refinement Protocol (BRP) is a crucial phase in the beamforming process, aimed at optimizing and fine-tuning the directional communication established during the initial Sector-Level Sweep (SLS) phase.

BRP tests different antenna configurations, both for transmission and reception, to ascertain which configuration offers the highest signal quality. The process relies on the data obtained from the SLS phase, using it as a baseline for refining antenna patterns. During BRP transactions, transmit (TRN-T) and receive (TRN-R) training fields are appended to frames, allowing for the evaluation of different antenna configurations within the same frame. BRP is an iterative process where both the initiator and the responder can request training for their respective antenna patterns, enabling continuous improvement and optimization of the link.

As shown in figure 4, TX (Transmit) training request and RX (Receive) training request are crucial components of the Beam Refinement Protocol (BRP). A TX training request is made to optimize the transmit antenna configurations. It involves requesting and testing various transmit antenna patterns to determine the most effective one for signal transmission. The initiator of the beamforming process sets a TX-TRN-REQ (Transmit Training Request) header field and appends transmit training fields (TRN-T) to the BRP frame. This action initiates the testing of different transmit antenna configurations. The feedback received during this process, typically in the form of Signal-to-Noise Ratio (SNR), helps in identifying the optimal configuration for transmission.

An RX training request focuses on refining the receive antenna configurations. The goal is to ascertain the best antenna pattern for receiving signals. This request is made by specifying the number of configurations to be tested in the frame's L-RX (Receive Link) header field. The corresponding node responds by appending the appropriate number of receive training fields (TRN-R) to its next frame, facilitating the evaluation of various receive antenna patterns. Similar to TX training, the feedback here helps in determining the most effective receive antenna configuration.

![**********************Figure 4. Beam refinement transactions [3].**********************](images/fig4.gif)

**********************Figure 4. Beam refinement transactions [3].**********************

The role of BRP in the beamforming process is pivotal for enhancing the efficiency and effectiveness of directional communication in the 60 GHz band, a key aspect of the IEEE 802.11ad standard.

## 4. Advantages and Limitations

60 GHz wireless networks offer a unique blend of advantages and also face certain limitations. In terms of benefits, these networks provide several key features which include: 

1. **High Data Rates:** One of the most significant advantages of 60 GHz networks is their ability to support Gbps data rates. This is ideal for applications requiring high-speed data transfer, like video streaming for LG wireless TV.
2. **Reduced Interference**: The 60 GHz frequency band is less crowded compared to 2.4 GHz and 5 GHz bands, resulting in lower interference levels. 
3. **Small Antenna Size**: The wavelength at 60 GHz is very small, which allows for the use of small-sized antennas like Zero Connect Box.

However, despite these advantages, 60 GHz wireless networks also encounter certain limitations. These include:

1. **Limited Range**: The high frequency of 60 GHz signals leads to high atmospheric and environmental attenuation, limiting the effective range of these networks. If the Zero Connect Box is moved to a distance of 30 feet, the signal strength may no longer be sufficient for transmission [4].
2. **Obstacle Penetration**: 60 GHz signals have difficulty penetrating solid objects like walls, leading to significant signal loss. This requires a clear line of sight for optimal performance.
3. **Cost and Complexity**: The technology required for 60 GHz transmission, including beamforming and phased arrays, can be more complex and expensive to implement compared to traditional Wi-Fi technologies.

## 5. Future Prospects

With these limitations in mind, we can make some improvements in the future. These improvements will result in a distinctive user experience.

1. ****Increased Integration in Consumer Electronics.**** Future developments may see an increased integration of 60 GHz technology in consumer electronics for faster wireless data transfer and connectivity. In the coming years, it is plausible that the Zero Connect Box and home router may be integrated into a single device.
2. **Automotive Industry**: The automotive sector could see advancements in vehicle-to-vehicle communication and in-car wireless networks, leveraging the high data rates and low latency of 60 GHz technology.
3. **Improved Beamforming Technologies**: Further research and development in beamforming and phased array antennas are expected to enhance the directionality and range of 60 GHz signals, overcoming some of the current limitations.

## 6. Conclusion

The exploration of 60 GHz wireless technology, as exemplified by LG's SIGNATURE OLED M (model M3) and its accompanying Zero Connect Box, represents a significant milestone in the evolution of wireless communication, particularly in the realm of consumer electronics. In this paper, I have provided an in-depth analysis of the various aspects of 60 GHz technology, discussing its innovative features such as high bandwidth and speed, OFDM modulation, dynamic channel time allocation, and the intricacies of beamforming training.

The advantages of 60 GHz wireless networks are numerous, offering groundbreaking data rates, reduced interference, and the convenience of smaller antenna sizes. However, the challenges of limited range, obstacle penetration issues, and the inherent cost and complexity of the technology underline the need for continuous innovation and improvement. Looking forward, the potential of 60 GHz wireless technology is vast. Anticipated advancements in integration within consumer electronics, automotive applications, and improved beamforming technologies promise to further elevate the capabilities and user experience of wireless networks.

In conclusion, with the ongoing development of 60 GHz wireless technology, an increasing number of multimedia devices, such as LG wireless TVs, are becoming prevalent in the consumer electronics industry. These devices are poised to reshape our wireless communication landscape and unlock new possibilities in the years ahead.

## References

[1] LG Electronics, “LG’s new OLED TV with Zero connect technology redefines freedom to design your space,” LG’S NEW OLED TV WITH ZERO CONNECT TECHNOLOGY REDEFINES FREEDOM TO DESIGN YOUR SPACE , https://www.lg.com/us/press-release/lgs-new-oled-tv-with-zero-connect-technology-redefines-freedom-to-design-your-space (accessed Dec. 10, 2023).

[2] S. B. Weinstein, "The history of orthogonal frequency-division multiplexing [History of Communications]," in IEEE Communications Magazine, vol. 47, no. 11, pp. 26-35, November 2009, doi: 10.1109/MCOM.2009.5307460.

[3] T. Nitsche, C. Cordeiro, A. B. Flores, E. W. Knightly, E. Perahia and J. C. Widmer, "IEEE 802.11ad: directional 60 GHz communication for multi-Gigabit-per-second Wi-Fi [Invited Paper]," in IEEE Communications Magazine, vol. 52, no. 12, pp. 132-141, December 2014, doi: 10.1109/MCOM.2014.6979964.

[4] 2023 9:33 pm UTC Scharon Harding - Aug 8, “New LG tvs relegate I/O to a box you can set 30 feet from the screen,” Ars Technica, https://arstechnica.com/gadgets/2023/08/lgs-wireless-ish-oled-tvs-start-at-7000/ (accessed Dec. 11, 2023).