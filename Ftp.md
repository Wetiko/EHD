# Ftp
 
Here's an example of how to connect to an FTP server using the `ftp` command:

```
ftp <hostname>
```

Replace `<hostname>` with the hostname or IP address of the FTP server you want to connect to.

For instance, if the FTP server's hostname is `ftp.example.com`, you would enter:

```
ftp ftp.example.com
```

After executing the command, the FTP client will attempt to establish a connection to the specified FTP server. If the connection is successful, you will see a prompt asking for your username and password. Enter the appropriate credentials to log in to the FTP server.

Here's an example interaction:

```
$ ftp ftp.example.com
Connected to ftp.example.com.
220---------- Welcome to Example FTP Server ----------
220- Authorized use only
220---------------------------------------------------
Name (ftp.example.com:user): myusername
331 Password required for myusername:
Password:
230 User myusername logged in.
Remote system type is UNIX.
ftp>
```

Once connected, you can proceed with executing various FTP commands to navigate the remote file system, upload or download files, and perform other operations as needed.


# Useful commands

Here are some common commands used in the FTP (File Transfer Protocol):

1. Connect to an FTP server:
   ```
   ftp <hostname>
   ```

2. Login to the FTP server with username and password:
   ```
   user <username> <password>
   ```

3. Change the current directory on the remote server:
   ```
   cd <directory>
   ```

4. Change the current directory on the local machine:
   ```
   lcd <directory>
   ```

5. List files and directories on the remote server:
   ```
   ls
   ```

6. List files and directories on the local machine:
   ```
   dir
   ```

7. Download a file from the remote server to the local machine:
   ```
   get <filename>
   ```

8. Upload a file from the local machine to the remote server:
   ```
   put <filename>
   ```

9. Rename a file on the remote server:
   ```
   rename <oldname> <newname>
   ```

10. Delete a file on the remote server:
    ```
    delete <filename>
    ```

11. Create a new directory on the remote server:
    ```
    mkdir <directory>
    ```

12. Remove a directory on the remote server:
    ```
    rmdir <directory>
    ```

13. Display the current remote directory:
    ```
    pwd
    ```

14. Change the transfer mode to binary:
    ```
    binary
    ```

15. Change the transfer mode to ASCII (text):
    ```
    ascii
    ```

16. Enable passive mode for data transfers:
    ```
    passive
    ```

17. Enable active mode for data transfers:
    ```
    active
    ```

18. Enable or disable the display of remote server responses:
    ```
    verbose
    ```

19. Set the local file transfer type to automatic:
    ```
    type auto
    ```

20. Set the local file transfer type to binary:
    ```
    type binary
    ```

21. Set the local file transfer type to ASCII (text):
    ```
    type ascii
    ```

22. Disconnect from the FTP server and exit the FTP session:
    ```
    bye
    ```

23. Help command to get information about FTP commands:
    ```
    help
    ```

These are the combined FTP commands that you can use for various operations when connected to an FTP server. Remember to replace `<hostname>`, `<username>`, `<password>`, `<filename>`, `<directory>`, or any other placeholders with the appropriate values based on your specific FTP server and requirements.