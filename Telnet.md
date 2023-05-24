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
