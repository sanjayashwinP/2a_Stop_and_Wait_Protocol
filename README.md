# 2a_Stop_and_Wait_Protocol
## NAME:SANJAY ASHWIN P
## REG NO:212223040181
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
# CLIENT:
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

# SERVER
import socket  
s=socket.socket()   
s.connect(('localhost',8000))  
while True:   
 print(s.recv(1024).decode())  
 s.send("Acknowledgement Recived".encode())  

## OUTPUT
# CLIENT:
![Screenshot 2024-04-09 152227](https://github.com/sanjayashwinP/SocketStudy/assets/147473265/4e0cf9cf-56b3-438c-9cf0-22e36435d524)

# SERVER:
![Screenshot 2024-04-09 152237](https://github.com/sanjayashwinP/SocketStudy/assets/147473265/ac835f24-cb5a-492a-acb8-107b1a5c4355)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
