# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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

Developed by : ISHWAR S

Reg no : 212225230106

### Client 
```python
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### Server
```python
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
Refer to the following screenshot to view the output of the program.
<img width="1267" height="247" alt="Screenshot 2026-05-27 081003" src="https://github.com/user-attachments/assets/376e5ba5-3590-487f-8825-7909672bde59" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
