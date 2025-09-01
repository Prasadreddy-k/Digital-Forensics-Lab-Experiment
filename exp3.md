# Experiment 3 : Capture and Analyze Network Traffic using Wireshark

## Aim 🎯
The aim of this experiment is to capture and analyze network traffic passing through a network interface using Wireshark. This process helps in understanding the communication between devices on a network, troubleshooting network issues, and identifying potential security vulnerabilities.

## Description 📝
Wireshark is a powerful and widely-used network protocol analyzer. It allows users to capture packets in real-time and display them in a human-readable format. Network traffic, whether it’s web browsing, email, or a simple ping, is broken down into small units called packets. Wireshark captures these packets, providing a detailed view of what's happening on the network. The captured data can then be filtered and analyzed to reveal information such as the source and destination IP addresses, the type of protocol being used (e.g., HTTP, TCP, UDP), and the actual data payload. This deep-level insight is invaluable for network administrators, security professionals, and developers.

## Tools & Equipment Used 🛠️
Computer: A workstation with a functioning network interface card (NIC).

Wireshark: A free and open-source network protocol analyzer.

Network Connection: An active network connection, either wired (Ethernet) or wireless (Wi-Fi).

## Procedure 👩‍🔬
Preparation:
![alt text](<Screenshort3/Screenshot 2025-09-01 233015.png>)
Ensure Wireshark is installed on your computer.

Close any unnecessary applications that might generate unwanted network traffic. This helps in keeping the captured data clean and focused.
![alt text](<Screenshort3/Screenshot 2025-09-01 233124.png>)
Launch Wireshark with administrator privileges.

Capturing Traffic:
![alt text](<Screenshort3/Screenshot 2025-09-01 233312.png>)
Upon launching, Wireshark will show a list of available network interfaces.

Identify the interface you are currently using for your network connection. You can usually tell which one is active by observing the real-time traffic graph next to the interface name.

Select the active interface and double-click it, or click the blue shark fin icon to start the capture.
![alt text](<Screenshort3/Screenshot 2025-09-01 233415.png>)
As soon as you start, Wireshark will begin capturing all packets passing through that interface. You'll see a constant stream of new packets appearing in the main window.

Perform a specific network activity you want to analyze, such as visiting a website, sending an email, or performing a DNS lookup.

Analyzing Traffic:
![alt text](<Screenshort3/Screenshot 2025-09-01 233546.png>)
Once you've performed the activity, click the red square Stop button in Wireshark to halt the capture.

Now, you can analyze the captured data. The top pane lists the captured packets, the middle pane shows the details of the selected packet, and the bottom pane displays the raw data in hexadecimal and ASCII.

Use the filter bar at the top to narrow down the packets you are interested in. For example, to see only HTTP traffic, type http and press Enter. To see traffic from a specific IP address, use a filter like ip.addr == 192.168.1.1.

Click on a packet in the top pane to examine its details in the middle pane. You can expand sections like Ethernet II, Internet Protocol Version 4, and Transmission Control Protocol to see detailed information about each layer of the packet.

## Results 📊
Captured Packets: Wireshark successfully captured a series of packets related to the specified network activity.

Protocol Identification: The analysis identified various protocols in use, such as DNS for name resolution, TCP for connection-oriented communication, and HTTP for web traffic.

Data Inspection: By examining the packet details, information like the source and destination IP addresses, port numbers, and specific application data were successfully identified. For example, the Host header in an HTTP request was clearly visible, revealing the website visited.

Traffic Flow: The sequential nature of the captured packets provided a clear picture of the network communication flow, showing the requests and responses between the client and the server. This confirms that Wireshark is an effective tool for a detailed packet-level analysis.