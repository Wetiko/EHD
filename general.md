# Ping sweep
`fping --alive --quiet –g <subnet start> <subnet end>`

# Look up host
Windows
`nslookup`
linux
`host <domain name>`
`dig <domain name>`

# SSH
`ssh <username>@<server ip address>`

# Anonymous Log INs

Connecting to a Linux server anonymously typically refers to establishing a remote shell session without providing any user credentials. By default, most Linux servers are not configured to allow anonymous access for security reasons. However, if you have specific permission or the server is intentionally set up to allow anonymous access, you can connect using the following methods:

1. SSH:
   - If the server allows anonymous SSH access, you can use an SSH client to connect. However, keep in mind that this is highly uncommon and potentially insecure.
   - Connect using the following command:
     ```
     ssh <server-ip>
     ```

2. Telnet:
   - Telnet is an unencrypted protocol and is generally not recommended for remote access due to security vulnerabilities. Nonetheless, if the server allows anonymous Telnet access, you can use it to connect.
   - Connect using the following command:
     ```
     telnet <server-ip>
     ```

3. FTP:
   - FTP (File Transfer Protocol) allows file transfers between systems. Some FTP servers may allow anonymous access to download public files.
   - Connect using an FTP client or the command-line FTP client:
     ```
     ftp <server-ip>
     ```

4. Anonymous FTP login:
   - If the FTP server allows anonymous access, you can attempt to login using the default username "anonymous" and provide an email address as the password.
   - Connect using the following command:
     ```
     ftp <server-ip>
     ```
     Once connected, provide the username "anonymous" and any email address as the password.

Note: It's essential to ensure that you have explicit permission to connect anonymously to a server. Connecting to a server without authorization can be illegal and is considered unethical. Always adhere to appropriate security practices and follow the rules and guidelines set by the server administrators.


# General Linux commands
To find kali version or kali linux kernel version
`cat /etc/os-release`
`uname -a`

To find ip address
`ip addr`
`ifconfig`

To find gateway ip
`ip route`

To see dns server
`cat /etc/resolv.conf`


# checking apache version

If you don't have direct access to the server, you can try to determine the Apache version with this:

1. Check the HTTP response headers: You can use the `curl` command to send a request to the server and inspect the response headers. The `-I` option is used to fetch only the headers. Run the following command:

   ```
   curl -I http://server-ip-address/
   ```

   Look for the "Server" header in the response. It usually includes the Apache version information.

   Example output:
   ```
   HTTP/1.1 200 OK
   Date: Wed, 15 Jun 2022 10:00:00 GMT
   Server: Apache/2.4.41 (Ubuntu)
   ...
   ```

   In this example, the Apache version is 2.4.41.
