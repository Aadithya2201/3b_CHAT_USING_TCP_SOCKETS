# 3b.CREATION FOR CHAT USING TCP SOCKETS

### NAME : AADITHYA R
### REGISTER NUMBER : 212223240001

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## client
```

import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## server
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

## OUTPUT
## server
![image](https://github.com/user-attachments/assets/c47d7cac-a8fe-4b8a-a2d8-0a425718c3e0)
## client
![image](https://github.com/user-attachments/assets/ab57cacd-690f-460c-bb88-536057678a6f)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
