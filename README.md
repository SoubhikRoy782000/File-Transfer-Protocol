# File-Transfer-Protocol

Aim -

To implement FTP application, where the Client on establishing a connection with the Server sends the  name of the file it wishes to access remotely. The Server then sends the contents of the file to the Client,  where it is stored.

Give Requirements –

There are two hosts, Client and Server. The Client sends the name of the file it needs from the Server and 
the Server sends the contents of the file to the Client, where it is stored in a file. 

Algorithm -

Server:

Step 1: Include the necessary header files.
Step 2: Create a socket using a socket function with family AF_INET, type as SOCK_STREAM.
Step 3: Bind the local host address to the socket using the bind function.
Step 4: Listen on the socket for connection requests from the client.
Step 5: Accept connection requests from the Client using accept function.
Step 6: Fork the process to receive a message from the client and print it on the console and another 
process to read messages from the console and send it to the client simultaneously38

Client:

Step 1: Include the necessary header files.
Step 2: Create a socket using a socket function with family AF_INET, type as SOCK_STREAM.
Step 3: Get the server IP address and the Port number from the console.
Step 4: Using gethostbyname function assign it to a hostent structure, and assign it to sin_addr of the 
server address structure.
Step 5: Request a connection from the server using the connect function.
Step 6: Fork the process to receive a message from the server and print it on the console and another 
process to read messages from the console and send it to the server simultaneously.
