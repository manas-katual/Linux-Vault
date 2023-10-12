Links : [[021 RHCSA Index]]

# Secure Shell (SSH)

- SSH is a remote service
- It is used for remote CLI access of Linux servers
- It works on server-client scenario
- SSH server is installed on Linux servers
- SSH client is installed on admin computer
- It is a TCP based service. Hence, it requires user authentication to login
- The server application uses TCP port 22 to connect with clients
- SSH is the most secured service for remote access as it provides end-to-end data encryption throughout the session
- On Linux, **openssh** tool is used on both server and client
- On window client tools like putty and secureCRT are used as SSH client
- By default ssh allows root login
- SSH authentication methods:
- There are 2 authentication methods for SSH login
	- **Password authentication**
	- **Key-pair authentication**
- Password authentication is the default method
- Password authentication is not a safer way to use SSH as password (though in encrypted form) travels over the network or internet. Hence, there is still a chance of the password getting trapped
- The more secure way is to use SSH keypair authentication
- In this method, a keypair is generated on client machine
- The keypair will have a private key and a public key
- Public key should be stored on server and private key should be stored on client
- When client with a private key will send request to server, the server will authenticate client with the keypair and will not require password
- Key does not travel on network unlike the password. Hence, this method is more secured

>[!Note]
>Keypair
>	Private key (id_rsa file)
>	Public key (id_rsa.pub file)