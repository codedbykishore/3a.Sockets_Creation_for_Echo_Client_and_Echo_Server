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
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER:
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
## OUPUT
## CLIENT:
![Screenshot 2024-04-12 141039](https://github.com/codedbykishore/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147139122/cf971dc6-5c98-4e10-be4b-78ac8f0158c1)
## SERVER:
![Screenshot 2024-04-12 141050](https://github.com/codedbykishore/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/147139122/b2544240-f0de-4c78-bfed-575be4ff76f8)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
