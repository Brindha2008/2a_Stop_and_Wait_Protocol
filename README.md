# 2a_Stop_and_Wait_Protocol
## DATE:11/05/2026
## NAME:BRINDHA A R
## REG:212225040050
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
## CLIENT.PY
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
## SERVER.PY
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Received ".encode())

```

## OUTPUT

<img width="1913" height="498" alt="Screenshot 2026-05-11 143150" src="https://github.com/user-attachments/assets/7e900933-b8a0-49a1-b862-356bd0e4371f" />

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
