# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME:N.KANNAN
## REG NO:212223230097
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
## Client:
```
import socket
s = socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr = s.accept()
while True:
    clientMessage=c.recv(1024).decode()
    c.send((clientMessage.encode()))
```
## Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```

## OUPUT:
## CLIENT:
![Screenshot 2024-05-12 201527](https://github.com/kannan-nagaraju/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145742755/0bc4a64d-e5f5-4224-9271-e6423cb8efec)

## SERVER:
![Screenshot 2024-05-12 201557](https://github.com/kannan-nagaraju/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/145742755/4963f2ff-53b6-4c2b-8fc0-6886bfbea063)


## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
