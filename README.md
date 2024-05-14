# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
NAME:RAMYA.P

REGISTER NUMBER: 212223240137

DEPARTMENT: AIML

# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### CLIENT SIDE:
```python
import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

### SERVER SIDE:
```python
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

## OUPUT:

### CLIENT SIDE:
![image](https://github.com/23014107/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151625620/ad534c0b-e66d-4319-b857-bf1f02f19c0f)

### SERVER SIDE:
![image](https://github.com/23014107/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151625620/341a176b-03b5-44fc-8648-816d5fd44c03)

## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
