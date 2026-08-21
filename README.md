# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
<H2>CLIENT</H2>

```
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
 ```
<H2>SERVER</H2>

```
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
<H2>CLIENT</H2>
<img width="503" height="331" alt="image" src="https://github.com/user-attachments/assets/bb6bf218-16f6-4654-97a9-6cdd4554e1ed" />

<H2>SERVER</H2>
<img width="474" height="273" alt="image" src="https://github.com/user-attachments/assets/6aea9e84-153a-49a6-8c69-327bda313c67" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
