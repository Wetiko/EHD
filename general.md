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