# kill-process-on-a-specific-port
kill process on a specific port



You can kill a process running on a specific port in your Mac through the Terminal. Here is how to do it:

1. Open your Terminal.

2. Run the following command to find out what process is running on port 8080:

```bash
lsof -i :8080
```

3. This will output a list of all processes using port 8080. The output should look like this:

```bash
COMMAND   PID    USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME
java    12345   user   23u  IPv6 0x45678      0t0  TCP *:8080 (LISTEN)
```

4. In this case, the process ID (PID) is 12345. 

5. To kill the process, run the following command:

```bash
kill -9 PID
```
Replace "PID" with the actual PID number from the output in step 3. 

Remember, you should only kill processes that you know are safe to stop, and that won't disrupt your operating system or the running of other applications. Always ensure you understand what process you're stopping before you proceed.
