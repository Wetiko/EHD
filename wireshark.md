# wireshark 

# common search filters

Here's a list of Wireshark search filters for various protocols:

TCP:
1. Filter for TCP traffic:
   ```
   tcp
   ```

2. Filter for TCP handshake packets (SYN, SYN-ACK, ACK):
   ```
   tcp.flags.syn == 1
   tcp.flags.ack == 1
   ```

3. Filter for TCP connection establishment (SYN packets):
   ```
   tcp.flags.syn == 1 and tcp.flags.ack == 0
   ```

4. Filter for TCP connection termination (FIN packets):
   ```
   tcp.flags.fin == 1
   ```

DNS:
1. Filter for DNS traffic:
   ```
   dns
   ```

2. Filter for DNS queries:
   ```
   dns.flags.response == 0
   ```

3. Filter for DNS responses:
   ```
   dns.flags.response == 1
   ```

4. Filter for DNS queries for a specific domain:
   ```
   dns.qry.name == "<domain>"
   ```

HTTP:
1. Filter for HTTP traffic:
   ```
   http
   ```

2. Filter for HTTP GET requests:
   ```
   http.request.method == "GET"
   ```

3. Filter for HTTP POST requests:
   ```
   http.request.method == "POST"
   ```

4. Filter for HTTP response codes:
   ```
   http.response.code == <status-code>
   ```

HTTPS:
1. Filter for HTTPS traffic:
   ```
   ssl
   ```

2. Filter for SSL handshake packets:
   ```
   ssl.handshake.type == 1
   ```

3. Filter for SSL/TLS client hello packets:
   ```
   ssl.handshake.type == 1 and ssl.handshake.version == <TLS-version>
   ```

4. Filter for SSL/TLS server hello packets:
   ```
   ssl.handshake.type == 2 and ssl.handshake.version == <TLS-version>
   ```

FTP:
1. Filter for FTP traffic:
   ```
   ftp
   ```

2. Filter for FTP commands:
   ```
   ftp.request.command
   ```

3. Filter for FTP responses:
   ```
   ftp.response.code
   ```

SMTP:
1. Filter for SMTP traffic:
   ```
   smtp
   ```

2. Filter for SMTP commands:
   ```
   smtp.command
   ```

3. Filter for SMTP responses:
   ```
   smtp.response
   ```

These are just a few examples of Wireshark search filters for common protocols. You can customize and combine these filters based on your specific needs and the protocols you want to analyze. Refer to the Wireshark documentation or protocol-specific documentation for more detailed filter options and syntax.


# Searching packets

To find IP addresses and other information from packets in Wireshark, you can utilize various features and fields within the Wireshark interface. Here's an explanation of the steps involved:

1. Capture Packets: Start capturing packets using Wireshark by selecting the appropriate network interface. This can be done by clicking on the desired interface from the available options in the main Wireshark window.

2. Analyze Packets: Once the packets are captured, Wireshark will display them in the packet list pane. Each row in the list represents a captured packet.

3. Source and Destination IP Addresses: The source and destination IP addresses can typically be found in the "Source" and "Destination" columns of the packet list. These columns display the IP addresses associated with each packet.

4. IP Address Details: To get more details about an IP address, such as hostname or additional information, you can right-click on an IP address in the packet list and select options like "Resolve", "Copy", or "Apply as Filter". Resolving an IP address will attempt to resolve it to a hostname, if possible.

5. Protocol Specific Fields: Depending on the protocols being used in the captured packets, you can look for specific fields within the packet details pane to find relevant information. For example, if you are analyzing HTTP traffic, you can expand the HTTP section in the packet details pane to view details like URLs, HTTP headers, and parameters.

6. Filtering by IP Address: You can apply filters to the packet list to display packets only associated with specific IP addresses. To do this, you can right-click on an IP address in the packet list and select options like "Apply as Filter" > "Selected" > "IP Address". This will create a filter that shows only the packets with the selected IP address.

7. Follow TCP Streams: In the case of TCP traffic, Wireshark provides a convenient feature called "Follow TCP Stream" that allows you to view the complete conversation between the source and destination IP addresses. Right-click on a TCP packet and select "Follow" > "TCP Stream" to see the entire communication.

These steps provide a general overview of how to find IP addresses and other relevant information from packets in Wireshark. Remember to adjust your analysis approach based on the specific protocols and fields you are interested in. Wireshark offers extensive features for packet analysis, and exploring the various options and functionalities will help you extract the desired information effectively.