# 2a_Stop_and_Wait_Protocol
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
```
client side:
  i=input("Enter a data: ") 
  c.send(i.encode()) 
  ack=c.recv(1024).decode() 
  if ack: 
    print(ack) 
    continue 
  else: 
    c.close() 
    break

server side:
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
  print(s.recv(1024).decode()) 
  s.send("Acknowledgement Recived".encode())
```
## OUTPUT
<img width="870" height="374" alt="image" src="https://github.com/user-attachments/assets/f80e66d8-86f1-49c8-9d4f-007968a275ac" />
<img width="783" height="346" alt="image" src="https://github.com/user-attachments/assets/af4eae93-2ac0-4f81-ae7b-69d2c37cae18" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
