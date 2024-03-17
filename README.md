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
CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
   msg=input("Client > ") 
   s.send(msg.encode()) 
   print("Server > ",s.recv(1024).decode())
```
SERVER:
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
CLIENT:

![Screenshot 2024-03-17 211059](https://github.com/HARISHA2006/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148843830/30ff104d-40e6-45a6-8b6c-225ed5948653)

SERVER:

![Screenshot 2024-03-17 211249](https://github.com/HARISHA2006/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148843830/f9990833-595a-48ce-9674-6b3ed0c7ae95)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
