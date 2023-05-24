# EHD
notes for ehd (With help from ai)



# Nmap


1. Scanning Techniques:

   - TCP connect scan: `-sT`
   - SYN scan (half-open scan): `-sS`
   - UDP scan: `-sU`
   - TCP ACK scan: `-sA`
   - TCP Window scan: `-sW`
   - TCP Null scan: `-sN`
   - TCP FIN scan: `-sF`
   - TCP Xmas scan: `-sX`
   - IP protocol scan: `-sO`
   - ICMP echo request scan: `-PE`
   - ICMP timestamp request scan: `-PP`

2. Port Specification:

   - Scan specific ports: `-p <port(s)>`
   - Scan port ranges: `-p <start-port>-<end-port>`
   - Scan all ports: `-p-`

3. Host Discovery:

   - Ping scan: `-sn`
   - TCP ACK ping scan: `-PA`
   - TCP SYN ping scan: `-PS`
   - UDP ping scan: `-PU`
   - IP protocol ping scan: `-PO`
   - ARP ping scan: `-PR`

4. Service and Version Detection:

   - Service detection: `-sV`
   - Light version detection: `-sV --version-light`
   - Aggressive version detection: `-sV --version-all`

5. Operating System Detection:

   - OS detection: `-O`
   - Enable more aggressive OS detection: `-O --osscan-guess`

6. Scripting Engine:

   - Execute NSE scripts: `--script <script(s)>`
   - Execute scripts in a category: `--script <category>`
   - Run default set of scripts: `--script default`

7. Output Formats:

   - Output to normal text: `-oN <file>`
   - Output to XML: `-oX <file>`
   - Output to grepable format: `-oG <file>`
   - Output in all formats: `-oA <basename>`

8. Timing and Performance:

   - Timing template selection: `-T<0-5>`
   - Set the maximum number of parallel probes: `--max-parallelism <value>`
   - Set the maximum number of parallel hosts: `--max-hostgroup <value>`

9. Miscellaneous:

   - Specify target(s): `<target(s)>`
   - Save profiles for later use: `--save-xml <file>`

These are just some of the commonly used Nmap commands and options. Nmap provides many more options for advanced scanning, customization, and fine-tuning. You can refer to the official Nmap documentation or run `nmap -h` for a comprehensive list of available options and their descriptions.

1. Basic TCP Scan:
   ```
   nmap -sT <target>
   ```

2. SYN Scan (half-open scan) with Service Version Detection:
   ```
   nmap -sS -sV <target>
   ```

3. UDP Scan:
   ```
   nmap -sU <target>
   ```

4. TCP ACK Scan:
   ```
   nmap -sA <target>
   ```

5. TCP Null Scan:
   ```
   nmap -sN <target>
   ```

6. TCP FIN Scan:
   ```
   nmap -sF <target>
   ```

7. TCP Xmas Scan:
   ```
   nmap -sX <target>
   ```

8. Scan Specific Ports:
   ```
   nmap -p 80,443 <target>
   ```

9. Scan Port Ranges:
   ```
   nmap -p 1-1000 <target>
   ```

10. Scan All Ports:
    ```
    nmap -p- <target>
    ```

11. Ping Scan (Host Discovery):
    ```
    nmap -sn <target>
    ```

12. Service and Version Detection:
    ```
    nmap -sV <target>
    ```

13. OS Detection:
    ```
    nmap -O <target>
    ```

14. Execute NSE Scripts:
    ```
    nmap --script <script(s)> <target>
    ```

15. Save Output in XML Format:
    ```
    nmap -oX output.xml <target>
    ```

16. Aggressive Scan (Includes OS detection and version detection):
    ```
    nmap -A <target>
    ```

17. Timing Template (Fast scan):
    ```
    nmap -T4 <target>
    ```

18. Scan Multiple Hosts:
    ```
    nmap <target1> <target2> <target3>
    ```
