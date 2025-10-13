Skip to content
Navigation Menu
Kabe-Innovates
3b-CHAT_USING_TCP_SOCKETS

Type / to search
Code
Pull requests
Actions
Projects
Security
Insights
You’re making changes in a project you don’t have write access to. Submitting a change will write it to a new branch in your fork Rohiniaiml/3b_CHAT_USING_TCP_SOCKETS, so you can send a pull request.
3b-CHAT_USING_TCP_SOCKETS
/
README.md
in
main

Edit

Preview
Indent mode

Spaces
Indent size

2
Line wrap mode

Soft wrap
Editing README.md file contents
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
# 3b) CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM

Developed by : **ROHINI R**

Reg no : **212224240138**

### Client 
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

### Server
```python
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
Refer to the following screenshot to view the output of the program.


<img width="1846" height="415" alt="image" src="https://github.com/user-attachments/assets/22a57121-cb5d-49bd-bd6e-4a636a853734" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.

Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
Editing 3b-CHAT_USING_TCP_SOCKETS/README.md at main · Kabe-Innovates/3b-CHAT_USING_TCP_SOCKETS
