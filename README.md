# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

# DATE:16-03-2023
# AIM :
To write a python program to perform stop and wait protocol

# ALGORITHM :
Start the program.
Get the frame size from the user
To create the frame based on the user request.
To send frames to server from the client side.
If your frames reach the server it will send ACK signal to client otherwise it will sendNACK signal to client.
Stop the program
# SERVER PROGRAM :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
 ```
# CLIENT PROGRAM:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
 print(ack)
 continue
 else:
 c.close()
 break
 ```
# SERVER OUTPUT :
![image](https://github.com/AGALYARAMESHKUMAR/EX-2/assets/119394395/b8dfbb72-98e4-41e2-9b87-494ebd8174ff)


# CLIENT OUTPUT:
![image](https://github.com/AGALYARAMESHKUMAR/EX-2/assets/119394395/d448e97d-8cfb-4557-9195-e1428ed92a80)


# RESULT :
Thus, python program to perform stop and wait protocol was successfully executed.


