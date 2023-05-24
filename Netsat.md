# Netstat


Here's an list of `netstat` commands that includes descriptions:

1. Display all active network connections and listening sockets:
   ```
   netstat -a
   ```

2. Show listening sockets with their associated programs:
   ```
   netstat -l -p
   ```

3. Display network statistics for all protocols (both incoming and outgoing):
   ```
   netstat -s
   ```

4. Show the PID (Process ID) and name of the program for each active connection and listening socket:
   ```
   netstat -p
   ```

5. Display only TCP connections:
   ```
   netstat -t
   ```

6. Display only UDP connections:
   ```
   netstat -u
   ```

7. Show both listening and non-listening sockets, but display numerical IP addresses and port numbers:
   ```
   netstat -an
   ```

8. Display the routing table:
   ```
   netstat -r
   ```

9. Show statistics for each network protocol (packets, errors, etc.):
   ```
   netstat -s
   ```

10. Display extended information for each active connection, including the user associated with the connection:
    ```
    netstat -e
    ```

11. Display only established connections (both TCP and UDP):
    ```
    netstat -o
    ```

12. Show the process and program information for each connection (including listening ports):
    ```
    netstat -ap
    ```

13. Display network connections in a continuous, updating manner:
    ```
    netstat -c
    ```

14. Show network connections using IPv6 addresses:
    ```
    netstat -6
    ```

15. Display the PID, program name, and process information for each active connection, both TCP and UDP:
    ```
    netstat -atunp
    ```

16. Show the interface statistics for all interfaces:
    ```
    netstat -i
    ```

17. Display multicast group information:
    ```
    netstat -g
    ```

18. Show listening UNIX domain sockets:
    ```
    netstat -lx
    ```

19. Display kernel routing information:
    ```
    netstat -nr
    ```

20. Show the socket statistics for all protocols:
    ```
    netstat -s
    ```

21. Display listening sockets with their associated programs and process information:
    ```
    netstat -plnt
    ```

22. Show statistics for each active network interface:
    ```
    netstat -i
    ```

23. Display network connections in a continuous, updating manner along with the timestamp:
    ```
    netstat -c -t
    ```

24. Show the number of received and sent packets for each network interface:
    ```
    netstat -i -e
    ```

25. Display the state of all network interfaces:
    ```
    netstat -ie
    ```

26. Show the multicast group memberships for all network interfaces:
    ```
    netstat -g
    ```

27. Display routing information for IPv4 and IPv6 in a detailed format:
    ```
    netstat -r -n
    ```

28. Show the status of TCP connections in a continuous, updating manner:
    ```
    netstat -c -a -p tcp
    ```

29. Display the network connections associated with a specific process ID (PID):
    ```
    netstat -p <pid>
    ```

30. Show the summary of active network connections by protocol:
    ```
    netstat -s -p tcp,udp
    ```

31. Display the number of open file descriptors for each process:
    ```
    netstat -o
    ```

32. Show the number of retransmitted TCP packets for each connection:
    ```
    netstat -s --tcp
    ```

33. Display the number of TCP connections in TIME_WAIT state:
    ```
    netstat -nt | grep TIME_WAIT | wc -l
    ```

34. Show the number of established connections per IP address:
    ```
    netstat -ntu | awk '{print $5}' | cut -d: -f1 | sort | uniq -c | sort -nr
    ```

These are additional `netstat` commands that provide various insights into network connections, statistics, processes, and more. Remember to refer to the `netstat` manual or command documentation for more detailed information on the specific options and their usage for your operating system.

# Examples

Here are some examples of `netstat` commands with their outputs:

1. Display all active network connections:
   ```
   netstat -a
   ```

   Output:
   ```
   Active Internet connections (including servers)
   Proto Recv-Q Send-Q Local Address         Foreign Address       (state)
   tcp        0      0 0.0.0.0:22            0.0.0.0:*             LISTEN
   tcp        0      0 127.0.0.1:631         0.0.0.0:*             LISTEN
   tcp        0      0 192.168.0.101:5432    0.0.0.0:*             LISTEN
   tcp6       0      0 :::22                  :::*                  LISTEN
   udp        0      0 0.0.0.0:631           0.0.0.0:*
   ```

2. Show listening sockets with their associated programs:
   ```
   netstat -l -p
   ```

   Output:
   ```
   Active Internet connections (only servers)
   Proto Recv-Q Send-Q Local Address         Foreign Address       State       PID/Program name
   tcp        0      0 0.0.0.0:22            0.0.0.0:*             LISTEN      1234/sshd
   tcp6       0      0 :::22                  :::*                  LISTEN      1234/sshd
   ```

3. Display network statistics for all protocols:
   ```
   netstat -s
   ```

   Output:
   ```
   Ip:
       10002389 total packets received
       0 forwarded
       0 incoming packets discarded
        ...
   ```

4. Show the PID (Process ID) and name of the program for each active connection and listening socket:
   ```
   netstat -p
   ```

   Output:
   ```
   Active Internet connections (including servers)
   Proto Recv-Q Send-Q Local Address         Foreign Address       State       PID/Program name
   tcp        0      0 0.0.0.0:22            0.0.0.0:*             LISTEN      1234/sshd
   tcp        0      0 192.168.0.101:5432    0.0.0.0:*             LISTEN      5678/postgres
   ```

These examples demonstrate the usage of `netstat` commands and provide sample outputs for each command. The actual output may vary depending on your system and network configuration.