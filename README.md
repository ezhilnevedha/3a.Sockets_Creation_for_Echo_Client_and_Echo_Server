# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Name: Ezhil Nevedha K
## Reg.no: 212223230055
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
client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUTPUT
client.py
![image](https://github.com/user-attachments/assets/1b9a3b75-1571-4244-ae06-e27b866282c8)

server.py
![image](https://github.com/user-attachments/assets/47376ec0-2348-4392-b966-99061b9be9d1)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
