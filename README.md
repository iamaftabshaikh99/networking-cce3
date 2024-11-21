### Q1) What are the various classes in IPv4? Explain all in detail.

#### Stretched and Elaborated Answer:

IPv4 (Internet Protocol Version 4) is a fundamental protocol in the TCP/IP suite. To accommodate networks of varying sizes, IPv4 divides its 32-bit address space into five distinct classes: **Class A, Class B, Class C, Class D, and Class E**. Each class has specific characteristics and purposes, allowing for efficient allocation and management of IP addresses.

---

#### **Class A**
- **Leading Bits**: `0xxxxxxx` (The first bit is always 0).
- **Address Range**: `0.0.0.0` to `127.255.255.255`.
- **Default Subnet Mask**: `255.0.0.0` (8 network bits, 24 host bits).
- **Number of Networks**: 128 (`2^7` networks).
- **Number of Hosts per Network**: Approximately 16.7 million (`2^24 - 2` usable IPs; subtracting network and broadcast addresses).
- **Purpose**: Designed for **large-scale organizations and ISPs** that require vast IP addresses.
  
**Example Use Case**: Early internet pioneers like AT&T and IBM were assigned Class A addresses due to their massive infrastructure needs.

---

#### **Class B**
- **Leading Bits**: `10xxxxxx` (The first two bits are 10).
- **Address Range**: `128.0.0.0` to `191.255.255.255`.
- **Default Subnet Mask**: `255.255.0.0` (16 network bits, 16 host bits).
- **Number of Networks**: 16,384 (`2^14` networks).
- **Number of Hosts per Network**: Approximately 65,534 (`2^16 - 2` usable IPs).
- **Purpose**: Ideal for **medium-to-large organizations**, including universities and regional ISPs.
  
**Example Use Case**: A university campus with multiple departments and thousands of connected devices.

---

#### **Class C**
- **Leading Bits**: `110xxxxxx` (The first three bits are 110).
- **Address Range**: `192.0.0.0` to `223.255.255.255`.
- **Default Subnet Mask**: `255.255.255.0` (24 network bits, 8 host bits).
- **Number of Networks**: Over 2 million (`2^21` networks).
- **Number of Hosts per Network**: 254 (`2^8 - 2` usable IPs).
- **Purpose**: Best suited for **small businesses or home networks**.
  
**Example Use Case**: A small office with a limited number of employees and devices.

---

#### **Class D**
- **Leading Bits**: `1110xxxx` (The first four bits are 1110).
- **Address Range**: `224.0.0.0` to `239.255.255.255`.
- **Usage**: Reserved for **multicast addressing**.
  - Multicast is used to send a single data packet to multiple destinations simultaneously, commonly in applications like video streaming or online gaming.
- **Subnet Mask**: Not applicable, as Class D does not support subnetting.

**Example Use Case**: Live-streaming platforms broadcasting content to multiple subscribers.

---

#### **Class E**
- **Leading Bits**: `1111xxxx` (The first four bits are 1111).
- **Address Range**: `240.0.0.0` to `255.255.255.255`.
- **Usage**: Reserved for **experimental purposes**.
  - These addresses are not assigned for public use and are often used for research and development in networking technologies.
- **Subnet Mask**: Not applicable, as Class E is non-standard.

**Example Use Case**: Testing new network protocols in controlled environments.

---

#### **Summary Table**
| **Class** | **Address Range**       | **Default Subnet Mask** | **Hosts/Network** | **Purpose**                     |
|-----------|-------------------------|--------------------------|-------------------|----------------------------------|
| **A**     | 0.0.0.0 - 127.255.255.255 | 255.0.0.0               | ~16 million       | Large networks (e.g., ISPs).    |
| **B**     | 128.0.0.0 - 191.255.255.255 | 255.255.0.0            | ~65,000           | Medium-to-large organizations.  |
| **C**     | 192.0.0.0 - 223.255.255.255 | 255.255.255.0          | 254               | Small businesses.               |
| **D**     | 224.0.0.0 - 239.255.255.255 | N/A                    | Multicast usage   | Streaming, online gaming.       |
| **E**     | 240.0.0.0 - 255.255.255.255 | N/A                    | Experimental      | Research and testing.           |

---

#### **Understanding the Practical Significance**
1. **Network Design**: IPv4 classes enable administrators to design networks of varying sizes efficiently.
2. **Address Allocation**: Classes provide a structured way to allocate IP addresses.
3. **Real-World Relevance**: While the traditional class-based system is largely replaced by CIDR, understanding these classes is crucial for legacy systems and foundational networking knowledge.
