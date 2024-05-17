# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
## ROLL :212223240104
## NAME: NARESH.R
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

## clint
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

## OUPUT
## CLINT
![Screenshot 2024-05-17 190404](https://github.com/feryjfgkuyfgewjfgew/3b_CHAT_USING_TCP_SOCKETS/assets/150319377/bfaed416-e783-4d86-b4d7-58e48beab0c1)


## SERVER
![Screenshot 2024-05-17 190345](https://github.com/feryjfgkuyfgewjfgew/3b_CHAT_USING_TCP_SOCKETS/assets/150319377/a2e2ef51-c20e-4d0c-b48e-3e9f2334f6bf)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
