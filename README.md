# Multi-threaded-server

Language: JAVA

Networking: HTTP, TCP/IP, Sockets

1. Client-Side Program: A client can communicate with a server using this code. This involves 
    - Establish a Socket Connection
    - Communication

2. Server-Side Program: 
    a) Server class: 
        Establishing the Connection: Server socket object is initialized and inside a while loop a socket object continuously accepts an incoming connection.
        Obtaining the Streams: The inputstream object and outputstream object is extracted from the current requests’ socket object.
        Creating a handler object: After obtaining the streams and port number, a new clientHandler object is created with these parameters.
        Invoking the start() method: The start() method is invoked on this newly created thread object.

    b) ClientHandler class: 
        An object of this class acts as a Runnable target for a new thread.
        First, this class implements Runnable interface so that it can be passed as a Runnable target while creating a new Thread.
        Secondly, the constructor of this class takes a parameter, which can uniquely identify any incoming request, i.e. a Socket.
        Inside the run() method of this class, it reads the client’s message and replies.