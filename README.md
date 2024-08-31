<h1>AlexCTF</h1>

<h3>Objective</h3>
The aim of to get the hidden flag. We are provided with a .pcap file.
<br /> <br />
<h3>Skills Learned</h3>
● Volatility tool <br />

<br />
<h3>Tools Used</h3>
● Binwalk <br />

<br />
<h3>Steps</h3>

Firstly, we used “binwalk” tool to check the contents of the pcap file. It contains a PNG file.
<br />
<img width="733" alt="alex1" src="https://github.com/user-attachments/assets/cc68898e-93c0-4480-8feb-459fa6ac3db7">
<br />
*Ref 1: Content of pcap file*
<br />
<br />
The next step was opening the pcap file with the Wireshark tool to inspect the sniffed traffic. We can see multiple frames.
<br />
In order to find the PNG, we ordered the packets from larger to smaller to see big payloads.
<br />
<img width="732" alt="alex2" src="https://github.com/user-attachments/assets/8f2bff68-fcbc-44b3-97a5-2ba38e0bf301">
<br />
*Ref 2: Wireshark packets"
<br />
<br />
In the biggest packet, we saw the word “PNG”, as shown in the image below.
<br />
<img width="734" alt="alex3" src="https://github.com/user-attachments/assets/2c350901-ee41-4637-983c-0614ff43e84c">
<br />
*Ref 3: Biggest packet"
<br />
<br />
We exported the bytes as raw file to check the contents:
<br />
<img width="545" alt="alex4" src="https://github.com/user-attachments/assets/9a4066d6-c579-4884-a8ef-1e9700e8313a">
<br />
*Ref 4: Bytes of packet"
<br />
<br />
<img width="373" alt="alex5" src="https://github.com/user-attachments/assets/04ba08fd-25e5-4731-a8f8-c949b228a566">
<br />
*Ref 5: Export raw bytes of packet"
<br />
<br />
The result is a raw file called filebytes.
<br />
<img width="89" alt="alex6" src="https://github.com/user-attachments/assets/98e6a248-0ea7-4935-baa3-931e6d94ad3f">
<br />
*Ref 6: Raw file"
<br />
<br />
When clicking on the raw file, this image opened up, finding the flag.
<br />
<img width="467" alt="alex7" src="https://github.com/user-attachments/assets/bd668139-b942-4968-a3b2-127fc7877322">
<br />
*Ref 6: Flag"
