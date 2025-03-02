# Detailed Explanation of Wi-Fi and IEEE 802.11 Standards

This image provides an overview of Wi-Fi technology and its association with the IEEE 802.11 family of standards. Let’s break it down into key concepts.

## 1️⃣ What is Wi-Fi?

Wi-Fi is a wireless networking technology that allows devices to connect to the internet or communicate wirelessly using radio signals.

### Key Points About Wi-Fi

* The name Wi-Fi is NOT an abbreviation (contrary to common belief). It is a brand name given by the Wi-Fi Alliance.
* It is based on Wireless Local Area Network (WLAN) technology.
* Wi-Fi and WLAN are often used interchangeably, but WLAN is a broader term.
* **Operating Frequency Bands:**
    * 2.4 GHz Band – Longer range but more interference.
    * 5 GHz Band – Faster speeds with less interference but a shorter range.
* Wi-Fi operates under the IEEE 802.11 family of standards.

## 2️⃣ IEEE and Wi-Fi Standardization

### What is IEEE?

* IEEE (Institute of Electrical and Electronics Engineers) is a global organization that sets technical standards for networking, computing, and electronics.
* In 1990, IEEE established the 802.11 Working Group to create wireless networking standards.
* The first 802.11 standard was ratified in 1997 with speeds of 1 Mbps and 2 Mbps.

### Evolution of Wi-Fi Standards

Over time, IEEE introduced improved versions of 802.11 with better speeds, efficiency, and frequency options.

| Wi-Fi Standard       | Year Introduced | Max Speed    | Frequency Band   | Key Features                                                     |
| --------------------- | --------------- | ------------ | ---------------- | ---------------------------------------------------------------- |
| 802.11                | 1997            | 1-2 Mbps     | 2.4 GHz          | First Wi-Fi standard                                             |
| 802.11b               | 1999            | 11 Mbps      | 2.4 GHz          | Improved range, interference issues                              |
| 802.11a               | 1999            | 54 Mbps      | 5 GHz            | Higher speed, but less range                                     |
| 802.11g               | 2003            | 54 Mbps      | 2.4 GHz          | Backward compatible with 802.11b                                 |
| 802.11n               | 2009            | 600 Mbps     | 2.4 GHz & 5 GHz  | First to introduce MIMO (Multiple Input, Multiple Output) technology |
| 802.11ac              | 2014            | 1 Gbps+      | 5 GHz            | Uses MU-MIMO (Multi-User MIMO) for improved performance           |
| 802.11ax (Wi-Fi 6)    | 2019            | 9.6 Gbps     | 2.4 GHz & 5 GHz  | Better efficiency, lower latency, improved battery life          |

### Upcoming Wi-Fi Standards

* Wi-Fi 6E (802.11ax Extended) → Expands Wi-Fi 6 to 6 GHz band for even faster speeds.
* Wi-Fi 7 (802.11be) → Expected in 2024-2025, bringing higher speeds, lower latency, and multi-link operation.

## 3️⃣ How Wi-Fi Works

Wi-Fi transmits data wirelessly using radio waves in the 2.4 GHz or 5 GHz frequency bands. The key steps are:

* A router or access point converts wired internet signals into wireless signals.
* Devices like laptops, smartphones, and smart TVs connect to the network via Wi-Fi adapters.
* Data is sent and received using radio signals via 802.11 protocols.

### Wi-Fi vs. Cellular (4G/5G)

| Feature          | Wi-Fi                           | Cellular (4G/5G)                  |
| ---------------- | ------------------------------- | --------------------------------- |
| Coverage         | Short-range (home, office)      | Long-range (citywide, nationwide) |
| Speed            | Faster for local networks       | Can be slower than Wi-Fi         |
| Latency          | Low latency                     | Higher latency than Wi-Fi         |
| Cost             | Free (home network)             | Expensive (mobile data plans)     |

## 4️⃣ Why Wi-Fi Matters?

* **Ubiquity:** Used in homes, offices, airports, cafes, and smart cities.
* **Supports IoT (Internet of Things):** Enables connectivity in smart homes, automation, and industry.
* **Cost-Effective:** No need for expensive cellular plans; works with a router and broadband connection.
* **Future Growth:** New standards like Wi-Fi 7 will improve performance for gaming, VR, AI applications.

## 5️⃣ Summary

* Wi-Fi is based on IEEE 802.11 standards and operates on 2.4 GHz & 5 GHz bands.
* IEEE started the 802.11 group in 1990, with the first standard finalized in 1997.
* Wi-Fi has evolved through different versions (802.11b, a, g, n, ac, ax) with faster speeds and better efficiency.
* Wi-Fi 6 and Wi-Fi 7 will drive the next-generation wireless revolution.
# Detailed Explanation of WLAN (Wi-Fi) Standards and Wi-Fi Channels

This image provides key details on 802.11 Wireless Standards and Wi-Fi Channels, helping us understand how different Wi-Fi technologies operate. Let’s break it down in detail.

## 1️⃣ 802.11 Wireless Standards

The IEEE 802.11 family defines various Wi-Fi standards, each improving upon speed, frequency, and range. The table outlines major Wi-Fi versions:

| IEEE Standard | Year Adopted | Frequency Band   | Max Data Rate | Indoor Range | Outdoor Range |
| ------------- | ------------ | ---------------- | ------------- | ------------ | ------------- |
| 802.11a       | 1999         | 5 GHz            | 54 Mbps       | 100 ft.     | 400 ft.      |
| 802.11b       | 1999         | 2.4 GHz          | 11 Mbps       | 100 ft.     | 450 ft.      |
| 802.11g       | 2003         | 2.4 GHz          | 54 Mbps       | 125 ft.     | 450 ft.      |
| 802.11n       | 2009         | 2.4 GHz & 5 GHz  | 600 Mbps      | 225 ft.     | 825 ft.      |
| 802.11ac      | 2014         | 5 GHz            | 1 Gbps        | 90 ft.      | 1,000 ft.    |

### Key Takeaways:

* 802.11b (2.4 GHz) was the first widely adopted Wi-Fi standard.
* 802.11g improved upon 802.11b, offering higher speeds at 2.4 GHz.
* 802.11n introduced dual-band support (2.4 GHz & 5 GHz), increasing speeds up to 600 Mbps.
* 802.11ac focused on 5 GHz with higher speeds (1 Gbps+) but had a shorter indoor range.

### Comparison of 2.4 GHz vs. 5 GHz Bands

| Feature                                | 2.4 GHz (802.11b/g/n)                                   | 5 GHz (802.11a/n/ac)                                 |
| -------------------------------------- | --------------------------------------------------------- | ------------------------------------------------------ |
| Speed                                  | Slower                                                    | Faster                                                 |
| Range                                  | Longer (better wall penetration)                          | Shorter                                                |
| Interference                           | High (due to other devices like Bluetooth, microwaves)    | Low                                                    |
| Best for                               | General browsing, IoT devices                             | Streaming, gaming, large file transfers                |

## 2️⃣ Wi-Fi Channels

Wi-Fi signals operate in specific frequency ranges, divided into channels to reduce interference.

### 2.4 GHz Wi-Fi Channels

* The 2.4 GHz band has 13 channels, each 5 MHz apart.
* Channels have a 22 MHz bandwidth, causing overlap between neighboring channels.
* The best non-overlapping channels are 1, 6, and 11.
* Using overlapping channels causes interference, leading to slow speeds and network issues.

### 5 GHz Wi-Fi Channels

* The 5 GHz band has more available channels and wider bandwidths.
* Channels are spaced farther apart, reducing interference.
* DFS (Dynamic Frequency Selection) channels help avoid radar interference.

### Choosing the Best Wi-Fi Channel

* **For 2.4 GHz networks:** Use Channel 1, 6, or 11 for minimal interference.
* **For 5 GHz networks:** Most channels don’t overlap, so interference is lower.

## 3️⃣ Future Wi-Fi Standards

With increasing demand for higher speeds and lower latency, newer Wi-Fi standards have been developed:

| Wi-Fi Standard             | Max Speed    | Frequency       | Key Feature                                   |
| -------------------------- | ------------ | --------------- | --------------------------------------------- |
| Wi-Fi 6 (802.11ax)         | 9.6 Gbps     | 2.4 GHz & 5 GHz | Better efficiency, low latency                |
| Wi-Fi 6E                   | 9.6 Gbps     | 6 GHz           | Less congestion, more bandwidth               |
| Wi-Fi 7 (802.11be, upcoming) | 30 Gbps+     | 6 GHz           | Multi-Link Operation, ultra-low latency       |

## 4️⃣ Summary

* 802.11 Wi-Fi standards have evolved from 802.11b (1999) to 802.11ac (2014), with each new version offering higher speeds and improved efficiency.
* 2.4 GHz offers better range, while 5 GHz offers higher speeds with less interference.
* Wi-Fi channels (1, 6, 11) reduce interference in 2.4 GHz networks, while 5 GHz provides better performance with more channels.
* Future Wi-Fi 6, 6E, and 7 will significantly improve wireless speed, efficiency, and security.
# Detailed Explanation of 802.11 Infrastructure Network and Wi-Fi Scanning

This image provides a detailed breakdown of the 802.11 network architecture and Wi-Fi scanning mechanisms used to connect devices to access points (APs). Let’s analyze each section in depth.

## 1️⃣ 802.11 Infrastructure Network Architecture

Wi-Fi networks operate in two main modes:

* **Infrastructure Mode** – Uses Access Points (APs) to manage connections.
* **Ad-Hoc Mode** – Devices communicate directly without an AP.

This image focuses on the Infrastructure Mode, which consists of the following key components:

### 📌 Key Components of Infrastructure Mode

| Component             | Description                                                                    |
| --------------------- | ------------------------------------------------------------------------------ |
| Station (STA)         | Any Wi-Fi-enabled device (laptop, smartphone) that connects to the wireless network. |
| Basic Service Set (BSS) | A group of devices (STAs) communicating using the same AP and radio frequency. |
| Access Point (AP)     | The central device in a BSS that connects STAs to the distribution system (network). |
| Portal                | Bridges the wireless network to other wired networks (e.g., Ethernet LAN).      |
| Distribution System (DS) | Connects multiple BSSs to form a larger Extended Service Set (ESS).          |

### 🔗 How the Infrastructure Network Works

* Stations (STAs) connect to an AP using Wi-Fi.
* The AP manages communication between STAs within the same BSS.
* Multiple APs can be linked via the Distribution System (DS) to create a larger network (ESS).
* The Portal connects the wireless LAN (Wi-Fi) to wired networks (e.g., Ethernet, Internet).

### 🛠 Key Features of Infrastructure Mode

* Centralized management via APs.
* Scalability by adding more APs to extend coverage.
* Better security and access control than Ad-Hoc Mode.

## 2️⃣ Wi-Fi (802.11) Scanning

When a device wants to connect to a Wi-Fi network, it must discover available APs. This is done through scanning, which happens in two ways: Passive and Active Scanning.

### 📌 Passive Scanning (Listening for AP Beacons)

* APs periodically send "Beacon Frames" containing network details (SSID, supported speeds, security).
* The device (H1) listens for these beacons.
* Once it detects an AP, it sends an Association Request.
* The AP replies with an Association Response, completing the connection.
* ✔ **Best for:** Power saving, background scanning.

### 📌 Active Scanning (Sending Probe Requests)

* The device (H1) actively sends a Probe Request to search for nearby APs.
* All APs within range respond with a Probe Response.
* The device selects the best AP and initiates an Association Request.
* The AP acknowledges with an Association Response, completing the connection.
* ✔ **Best for:** Faster network discovery, immediate connections.

### 💡 Passive vs. Active Scanning

| Feature           | Passive Scanning          | Active Scanning           |
| ----------------- | ------------------------- | ------------------------- |
| How it works      | Device listens for AP beacons | Device sends Probe Requests |
| Power Consumption | Low (saves battery)       | Higher (sends extra requests) |
| Speed             | Slower                    | Faster                    |
| Usage             | Background scanning       | Immediate connection      |

## 3️⃣ Summary

* 802.11 Infrastructure Mode uses Access Points (APs) to connect Wi-Fi devices to a larger Distribution System (DS).
* BSS (Basic Service Set) refers to a group of devices connected to a single AP, while ESS (Extended Service Set) connects multiple BSSs.
* Passive Scanning involves listening for AP beacons, whereas Active Scanning involves sending probe requests.
* Active Scanning is faster but consumes more power, while Passive Scanning is more efficient for battery life.
# Wi-Fi Alliance Mission and Certification Process Explained

This image provides insights into the Wi-Fi Alliance, its mission, and the certification process for Wi-Fi-enabled devices.

## 1️⃣ What is the Wi-Fi Alliance?

The Wi-Fi Alliance is a non-profit organization that ensures Wi-Fi devices meet interoperability, security, and performance standards. It is responsible for developing and promoting Wi-Fi standards worldwide.

### 📌 Key Objectives of the Wi-Fi Alliance

* Certify interoperability of products based on IEEE 802.11 technology.
* Expand the market for Wi-Fi Certified devices across industries.
* Ensure rigorous testing to guarantee seamless connectivity.
* Promote Wi-Fi branding and consumer awareness.

## 2️⃣ Wi-Fi Certification & Logo System

The Wi-Fi Certification Program ensures that products from different manufacturers work together seamlessly.

### 🔹 Certification Process

* Manufacturers submit their products for testing.
* The product undergoes rigorous interoperability testing.
* Successful products receive the Wi-Fi CERTIFIED™ logo.
* Certified products are listed on the Wi-Fi Alliance website.

### 🔹 Importance of Wi-Fi Certification

* Assures quality and security for end users.
* Ensures interoperability between devices from different brands.
* Mandatory for retail packaging to help consumers identify certified products.

## 3️⃣ Wi-Fi Certified Logos & Their Meaning

Wi-Fi Certified devices display official logos to indicate the standards they support. Some examples include:

* Wi-Fi CERTIFIED™ (Basic certification)
* Wi-Fi CERTIFIED 6™ (for Wi-Fi 6/6E)
* Wi-Fi CERTIFIED WPA3™ (Advanced security standard)

The logo system helps retailers and consumers quickly identify compatible products.

## 🔎 Summary

* The Wi-Fi Alliance is responsible for certifying Wi-Fi products for interoperability and security.
* The certification process ensures that different devices work together seamlessly.
* Wi-Fi CERTIFIED™ logos are mandatory on product packaging.
* Consumers should look for Wi-Fi CERTIFIED™ products for guaranteed compatibility and performance.
# Infrastructure vs. Ad-Hoc Networks Explained

This image compares Infrastructure-based networks and Ad-Hoc networks, explaining their differences and use cases.

## 1️⃣ Infrastructure Network (Traditional Wi-Fi)

* Uses a centralized Access Point (AP) (such as a router).
* Devices communicate through the AP, not directly.
* Suitable for large networks (e.g., homes, offices, public Wi-Fi hotspots).
* More stable, scalable, and secure but requires setup.

### 📌 Key Features:

* ✔️ Centralized communication
* ✔️ Better coverage with wired backbone
* ✔️ Easier management & security
* ✔️ Higher performance due to AP control

## 2️⃣ Ad-Hoc Network (Peer-to-Peer Wi-Fi)

* No Access Point (AP) is needed—devices connect directly.
* Decentralized communication.
* Useful for temporary or mobile setups (e.g., file sharing, gaming, disaster recovery).
* Can form Mobile Ad-Hoc Networks (MANETs) for dynamic, mobile connectivity.

### 📌 Key Features:

* ✔️ Quick setup, no infrastructure required
* ✔️ Flexible for temporary or emergency use
* ✔️ Ideal for short-range device-to-device communication
* ✔️ More difficult to manage & secure

## 🔎 Key Differences

| Feature               | Infrastructure Network          | Ad-Hoc Network                        |
| --------------------- | ------------------------------- | ------------------------------------- |
| Access Point (AP)     | Required                        | Not required                          |
| Scalability           | High (supports many devices)    | Limited                               |
| Security              | Stronger (via AP control)       | Weaker                                |
| Setup Complexity      | Moderate to High                | Low                                   |
| Ideal Use Cases       | Homes, offices, public Wi-Fi    | Temporary connections, emergency communication |

## ⚡ Real-World Applications

* **Infrastructure Networks:** Home Wi-Fi, corporate networks, university campuses.
* **Ad-Hoc Networks:** AirDrop, Bluetooth tethering, emergency rescue operations, military networks.
# 📡 What is Ad-Hoc Routing?

- Adhoc routing in IoT WiFi networks refers to communication between devices in a decentralized, infrastructure-less manner, where each device (or node) can act as both a host and a router.
- No fixed infrastructure like routers or access points.
- Routes can change dynamically due to mobility.
- Packets may take multiple hops to reach the destination.
- Scalability: Supports a large number of connected devices.
- An ad-hoc routing protocol is a convention that controls how nodes decide which way to route packets between computing devices in a mobile ad-hoc network

- **Neighbor Discovery** is the foundation of most adhoc protocols in which : <br>

Nodes broadcast periodic messages (e.g., beacon packets) to detect nearby devices.
Helps build a "neighbor table", allowing nodes to learn about their 2-hop neighborhood (direct and indirect connections).



## 📌 Real-World Applications

* ✔️ **Proactive:** Military mesh networks, corporate setups.
* ✔️ **Reactive:** IoT devices, emergency communication.
* ✔️ **Geographic:** UAV (drones), vehicular ad-hoc networks (VANETs).
---

# 📡 Proactive "Link-State" Routing Algorithms
![image](https://github.com/user-attachments/assets/f7443c97-d7a2-4739-afef-17a78c5353c1)

This image explains how Link-State Routing works in proactive protocols, focusing on topology discovery and route updates.

## 🛤 How Do Link-State Algorithms Work?

* Every node shares its link information with its neighbors.
* Over time, all nodes can build a complete map of the network.
* Assumes the topology remains stable long enough for all nodes to sync and have same information available

## 🔄 How Link Updates Work?

* Whenever a link changes state (goes up/down), affected nodes:
    * Send "hello" packets to detect the change.
    * Propagate the update to neighboring nodes.
* Eventually, the entire network is updated.

## 🔗 Example of Link-State Update (New Link A↔C)
![image](https://github.com/user-attachments/assets/45232f40-064d-4533-b3b5-6421cac36a35)

1️⃣ **Initial State:** Nodes A, B, C, and D have a common network topology.
2️⃣ **New Link A↔C is Established.**
3️⃣ **Nodes A and C share the new link with their neighbors.**
4️⃣ **Update propagates through the network until all nodes learn about A↔C.**

## 🌍 Advantages of Link-State Routing

* ✔️ **Faster Convergence** – All nodes quickly sync topology changes and rapidly update to network changes
* ✔️ **More Accurate Routes** – Each node has a global network view.
* ✔️ **Efficient for Large Networks** – Better than distance-vector in complex topologies.

## 🚀 Examples of Link-State Protocols:

* OLSR (Optimized Link State Routing) – Used in ad-hoc networks.
* OSPF (Open Shortest Path First) – Common in wired networks.
# 🔄 Reactive Routing: Dynamic Source Routing (DSR)

DSR is a reactive (on-demand) routing protocol used in ad-hoc networks. It only searches for a route when necessary, rather than maintaining a full routing table like proactive protocols.

## 🛤 How Does DSR Work?

### 1️⃣ Route Request (RREQ) Broadcast

When a source node (S) wants to send data to a destination node (D), it broadcasts an RREQ.
This request floods through the network until it reaches the destination or an intermediate node that knows the route.

### 2️⃣ Route Reply (RREP) Unicast

The destination node (D) sends an RREP back to the source along the reverse path.

### 3️⃣ Source Routing

Every packet carries the entire route from source to destination.
Intermediate nodes use this information to forward packets.

## 🔍 Route Discovery in DSR

🔵 Blue nodes in the diagram received RREQ for D from S.
✔ The RREQ spreads from S through multiple paths.
✔ The first RREQ that reaches D triggers an RREP to be sent back.
✔ Once S gets the RREP, it starts sending data.

## 🌍 Advantages of DSR

✅ **On-demand Routing** – Reduces overhead since routes are only discovered when needed.
✅ **Loop-Free Routing** – Source carries the route, preventing loops.
✅ **No Periodic Updates** – Saves bandwidth compared to proactive routing protocols.

## 🔴 Challenges:

* High overhead for large networks (entire path is included in each packet).
* Latency due to route discovery time.

## 🚀 Where is DSR Used?

🔹 Mobile Ad-Hoc Networks (MANETs)
🔹 Wireless Sensor Networks (WSNs)
🔹 Vehicular Ad-Hoc Networks (VANETs)
# 📡 Route Discovery in DSR (Dynamic Source Routing)

This image illustrates the Route Request (RREQ) broadcast process in Dynamic Source Routing (DSR).

## 🚀 How Route Discovery Works in DSR

### 🔹 Step 1: Source Broadcasts RREQ

The source node (S) initiates a broadcast transmission of the Route Request (RREQ) packet to find a path to the destination (D).
Each intermediate node forwards the RREQ to its neighbors until it reaches the destination.

### 🔹 Step 2: Appending Identifiers to RREQ

Every node that forwards the RREQ appends its identifier to the packet.
This helps create a record of the path taken.
**Example:** If S sends an RREQ via E, the packet now carries the path [S, E].

## ⚠️ Potential for Collision

### 🔴 Issue: Redundant RREQ Transmission

Since RREQ is broadcasted, nodes may receive it from multiple neighbors.
**Example:** Node H receives RREQ from both C and B, leading to redundant transmissions and potential collisions.

### 🔴 Solution:

Nodes discard duplicate RREQs to avoid unnecessary retransmissions.
Random delays may be used before forwarding to reduce contention.

## 🔍 Summary

✔ RREQ floods through the network until it reaches the destination.
✔ Each node appends its identifier to track the path.
✔ Redundant broadcasts can cause collisions and must be managed efficiently.
# 📌 Proactive vs Reactive Routing

Routing protocols in ad-hoc networks can be categorized into two types:

## ⚡ Reactive (On-Demand) Routing

✅ Establishes routes only when needed (reduces overhead).
✅ Stores entire route in each message (can increase message size).
✅ Floods the network with route requests (RREQs), which can cause network congestion.
❌ Example: DSR (Dynamic Source Routing) and AODV (Ad hoc On-Demand Distance Vector Routing).

## 🔄 Proactive (Table-Driven) Routing

✅ Maintains routing tables with precomputed routes.
✅ No delay in route discovery, as routes are always available.
✅ Continuously exchanges route updates between nodes.
❌ Overhead due to constant updates, even if no traffic exists.
❌ Route information may become outdated in dynamic networks.
❌ Example: OLSR (Optimized Link State Routing) and DSDV (Destination-Sequenced Distance Vector Routing).

## 🗺️ Geographic Routing

✔ Uses location-based routing instead of maintaining full routing tables.
✔ Requires nodes to know their location, as well as that of their neighbors and destination.
✔ Can use GPS (Global Positioning System) or a Location Broker for positional data.
💡 Benefit: Scalability in large networks, as decisions are made locally rather than maintaining full topology.
💡 Example: Greedy Perimeter Stateless Routing (GPSR).

## 🔍 Summary

| Routing Type | When Routes Are Established? | Scalability | Overhead                               | Example Protocols |
| ------------ | ---------------------------- | ----------- | -------------------------------------- | ----------------- |
| Reactive     | On-demand, when required     | High        | Low (when idle), but high during discovery | DSR, AODV         |
| Proactive    | Always maintained            | Low (for dynamic networks) | High (continuous updates)            | OLSR, DSDV        |
| Geographic   | Based on node location       | Very High   | Low (only needs location updates)      | GPSR              |
