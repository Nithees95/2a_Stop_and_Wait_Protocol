
## AIM :
To write a python program to perform stop and wait protocol
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:
```
NAME : YEGAVINTI NITHEESH
REG NO:212224040370
```
```
CLIENT: 
 
import socket 
s=socket.socket() 
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
```
SERVER: 
 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())
```

## OUTPUT:
### CLIENT:
<img width="1015" height="280" alt="Screenshot 2025-09-17 134013" src="https://github.com/user-attachments/assets/91c9ff41-aa97-47fa-aadd-19c71a8d4f9e" />

### SERVER:


<img width="1019" height="242" alt="Screenshot 2025-09-17 134022" src="https://github.com/user-attachments/assets/fb798f6b-0b77-4680-be4c-3188db18e4dc" />

## RESULT:
Thus, python program to perform stop and wait protocol was successfully executed.
