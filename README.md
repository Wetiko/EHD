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

# example

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


# Telnet

Telnet is a network protocol that allows you to establish a command-line session with a remote host over a TCP/IP connection.

1. Connecting to a remote host:
   ```
   telnet <host> <port>
   ```

   Replace `<host>` with the IP address or hostname of the remote host, and `<port>` with the desired port number. By default, Telnet uses port 23.

2. Telnet commands after establishing a connection:
   - `Ctrl + ]`: Enter Telnet command mode.
   - `close`: Close the Telnet connection.
   - `quit`: Close the Telnet connection and exit Telnet.

3. Telnet command mode:
   After entering Telnet command mode (`Ctrl + ]`), you can use the following commands:

   - `?` or `help`: Display a list of available Telnet commands.
   - `close`: Close the Telnet connection.
   - `display`: Show the current settings for the Telnet client.
   - `mode`: Toggle between character mode and line mode.
   - `quit`: Close the Telnet connection and exit Telnet.
   - `send`: Send special Telnet characters.
   - `set`: Set various Telnet options.

4. Telnet options:
   - `toggle crlf`: Toggle sending carriage return and line feed characters.
   - `toggle echo`: Toggle local echoing of characters.
   - `toggle escape`: Toggle recognition of the Telnet escape character.
   - `toggle autoflush`: Toggle automatic flushing of output.
   - `toggle termdata`: Toggle terminal data transfer.
   - `display`: Show the current settings for Telnet options.
   - `set`: Set a specific Telnet option.

5. Other Telnet commands and features:
   - `Ctrl + ]`, followed by `send <string>`: Send a string of characters to the remote host.
   - `Ctrl + ]`, followed by `z`, then `s`: Suspend Telnet and return to the local shell.
   - `Ctrl + ]`, followed by `z`, then `r`: Resume a suspended Telnet session.

Please note that Telnet is an insecure protocol as the data is transmitted in plain text. It is recommended to use secure alternatives like SSH (Secure Shell) whenever possible.

# example

1. Connecting to a remote host:
   ```
   telnet 192.168.1.100
   ```
   This command establishes a Telnet connection to the remote host with the IP address 192.168.1.100 using the default Telnet port 23.

2. Telnet command mode:
   After establishing a Telnet connection, you can enter Telnet command mode by pressing `Ctrl + ]`. Here are some commands you can use:

   - Closing the Telnet connection:
     ```
     close
     ```
     This command closes the Telnet connection and returns you to the local shell.

   - Exiting Telnet:
     ```
     quit
     ```
     This command closes the Telnet connection and exits Telnet entirely.

   - Displaying available Telnet commands:
     ```
     ? or help
     ```
     This command displays a list of available Telnet commands.

   - Sending a special Telnet character:
     ```
     send <string>
     ```
     This command sends a string of characters to the remote host.

   - Setting Telnet options:
     ```
     set <option>
     ```
     This command sets a specific Telnet option. For example, `set termdata` enables terminal data transfer.

3. Telnet options:
   Here are some examples of Telnet options and their usage:

   - Toggling local echoing of characters:
     ```
     toggle echo
     ```
     This command toggles the local echoing of characters. When enabled, characters you type will be displayed locally as you type them.

   - Setting Telnet option values:
     ```
     set <option> <value>
     ```
     This command sets a specific Telnet option to a desired value. For example, `set termdata off` disables terminal data transfer.

   - Displaying Telnet option settings:
     ```
     display
     ```
     This command displays the current settings for Telnet options.

Please note that the exact commands and options available may vary depending on the Telnet client you are using and the remote host's configuration.