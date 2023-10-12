Links : [[021 RHCSA Index]]

# Port numbers and sockets

- Every server has unique IP address
- We can run multiple network applications on a single server
- All applications on a single server use single IP address
- So, to bring further uniqueness in communication, every application uses another address called **port number**
- Application Port Numbers range from **1 to 65535**
- **Well-known ports: 1 — 1023**
	- **e.g.: SSH (22), HTTP (80), HTTPS (443)**
- Ports above 1023 are used for session management and custom port assigning
- So, applications use their unique port numbers on Server IP address to talk to clients
- Almost all network applications are service based
- Also, every network application has a config file from where it takes all the instructions
- Whenever we modify the config file of an application, it is must to restart its service
- To start their process, we need to start their service

>[!Note]
A process of a network application listening client requests on its port number is called a socket
in Linux, applications like **netstat** and **ss** are used to list all open sockets of a server
Commands: netstat —n (or) ss —tnlp

>[!tip]
Network applications are either <abbr title="User Authentication is must">TCP</abbr> based or <abbr title="User Authentication is optional">UDP</abbr> based
