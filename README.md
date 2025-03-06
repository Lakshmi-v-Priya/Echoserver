# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
sever.py
```
import socket
HOST = "127.0.0.1"  
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
client.py
```
import socket
HOST = "127.0.0.1"  
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Lakshmi Priya , 212223220049")
    data = s.recv(1024)
print(f"Received {data!r}")
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/5b7c4023-1fce-48c5-abbc-19dccd741c98)
![image](https://github.com/user-attachments/assets/5ade422e-99d2-4454-a750-25cb2629940d)


## RESULT:
The program is executed successfully
