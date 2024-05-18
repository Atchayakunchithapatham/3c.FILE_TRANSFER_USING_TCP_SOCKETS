# 3c.CREATION FOR FILE TRANSFER USING TCP SOCKETS
## AIM
To write a python program for creating File Transfer using TCP Sockets Links
## ALGORITHM:
1. Import the necessary python modules.
2. Create a socket connection using socket module.
3. Send the message to write into the file to the client file.
4. Open the file and then send it to the client in byte format.
5. In the client side receive the file from server and then write the content into it.
## PROGRAM
DEVELOPED BY:ATCHAYA.K


REGISTER NUM: 2122232220011
CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
SERVER:
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
Client:
![image](https://github.com/Atchayakunchithapatham/3c.FILE_TRANSFER_USING_TCP_SOCKETS/assets/144870744/26985b84-bc7f-43e1-8ae7-14652332e39e)



Server:
![image](https://github.com/Atchayakunchithapatham/3c.FILE_TRANSFER_USING_TCP_SOCKETS/assets/144870744/1e849b2b-e467-4d2e-8fd7-494dda0a27e0)


## RESULT
Thus, the python program for creating File Transfer using TCP Sockets Links was 
successfully created and executed.
