# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

## Developed By : SELVA JOBIN S
## Register No  : 212223220102
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
## client.py:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

## server.py:
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
## OUTPUT:
## client:
![321569226-c3232dc0-c6c0-4dad-b70f-f0194e1866cc](https://github.com/selvajobin/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149985750/543aea67-2096-4de2-99e0-c1ea8687b065)

## server:
![321569276-77e6e228-3c13-49ce-9285-94f5ccd12aa3](https://github.com/selvajobin/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/149985750/fc70628e-fb34-4c13-be26-51e3f2046dc2)


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
