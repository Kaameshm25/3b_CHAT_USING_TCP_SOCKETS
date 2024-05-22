# Ex No :3b  CREATION FOR CHAT USING TCP SOCKETS
## NAME : KAAMESH M
## REGISTER NUMBER : 212223040080
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT
```py
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### SERVER 
```py
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUTPUT
### CLIENT OUTPUT

![CN 3b c](https://github.com/Kaameshm25/3b_CHAT_USING_TCP_SOCKETS/assets/144870650/e9ec508b-99ed-4d10-839f-7174398bca6c)

### SERVER OUTPUT

![CN 3b s](https://github.com/Kaameshm25/3b_CHAT_USING_TCP_SOCKETS/assets/144870650/93f2c71d-ef2b-4051-b16c-1d162c7c0c9f)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
