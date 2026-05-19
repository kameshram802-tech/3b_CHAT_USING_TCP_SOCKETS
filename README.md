# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())

```

### SERVER.py
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUPUT

### CLIENT
<img width="955" height="266" alt="image" src="https://github.com/user-attachments/assets/eea8f914-0b04-4db5-8b89-174e99065607" />


### SERVER
<img width="954" height="273" alt="image" src="https://github.com/user-attachments/assets/d5b63141-2cb6-4ee7-9791-d344db23e2c6" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
