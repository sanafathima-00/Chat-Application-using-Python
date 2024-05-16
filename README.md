# Chat Application using Pythom
1. Server Side:
<br>
> The server-side code sets up a basic chat server using sockets.
<br>
> It listens for incoming connections on the specified `HOST` and `PORT`.
<br>
> When a client connects, it adds the client socket to the `clients` list.
<br>
> The `handle_client` function runs in a separate thread for each connected client:
<br>
- It receives messages from the client.
<br>
- If the message is empty or there's an issue with the connection, it removes the client from the list.
<br>
- Otherwise, it broadcasts the message to all other connected clients (except the sender).
<br>
> The main loop accepts new connections and starts a thread for each client.
<br>
<br>
2. Client Side:
<br>
> The client-side code connects to the same `HOST` and `PORT`.
<br>
> It creates two threads:
<br>
- The `send_message` thread reads input from the user and sends it to the server.
<br>
- The `receive_message` thread receives messages from the server and prints them.
<br>
> If there's an issue with the connection, it handles exceptions and closes the socket.
