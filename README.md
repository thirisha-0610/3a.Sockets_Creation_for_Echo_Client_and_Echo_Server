# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

### NAME: THIRISHA A
### REG NO: 212223040228

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

## Client 

import socket

s=socket.socket()

s.connect(('localhost',8000))

while True:

 msg=input("Client > ")
 
 s.send(msg.encode())
 
 print("Server > ",s.recv(1024).decode())

## Server

import socket

s=socket.socket()

s.bind(('localhost',8000))

s.listen(5)

c,addr=s.accept()

while True:

 ClientMessage=c.recv(1024).decode()
 
 c.send(ClientMessage.encode())
 
## OUPUT

![image](https://github.com/thirisha-0610/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149347494/d2807b39-8a86-48e2-a864-84ae0c321623)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
