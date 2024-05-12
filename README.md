## EXP NO 3B.CREATION FOR CHAT USING TCP SOCKETS

## NAME: VISWANADHAM VENKATA SAI SRUTHI
## REG NO: 212223100061

## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client:

```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## Server:

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
## Client:

![image](https://github.com/sruthiviswanadham/3b_CHAT_USING_TCP_SOCKETS/assets/151760421/c7b4843e-b47e-41d7-a691-a9370617da58)

## Server:


![image](https://github.com/sruthiviswanadham/3b_CHAT_USING_TCP_SOCKETS/assets/151760421/303b69e5-8be6-4764-93ee-45d63a459f17)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
