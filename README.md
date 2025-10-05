# -MULTITHREADED-CHAT-APPLICATION

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : ALLURI HARSHA VARDHAN

*INTERN ID*: CT06DY2897

*DOMAIN*: JAVA PROGRAMMING

*DURATION*: 6 WEEKS

*MENTOR*: NEELA SANTHOSH

*DESCRIPTION*:

The `Server` class starts by creating a **ServerSocket** object bound to port `1234`. This port number must be the same one that the client uses to connect. Once initialized, the server enters an infinite `while(true)` loop where it continuously waits for client connections using the `accept()` method. Each successful connection returns a new `Socket` object that represents communication with one client.To enable data transfer, the server sets up input and output streams. It uses `InputStreamReader` and `BufferedReader` to read messages sent by the client, and `OutputStreamWriter` with `BufferedWriter` to send responses back to the client. The inner loop continuously listens for messages from the client using `readLine()`. Each incoming message is printed on the server’s console with the prefix `"Client:"`. The server responds to every client message with `"MSG RECEIVED."`, showing that the server has successfully received and processed the data.If the client sends the message `"BYE"`, the server breaks out of the inner loop and closes the socket and all associated streams. However, because the entire program is wrapped inside a continuous `while(true)` loop, the server remains alive and ready to accept a new client after the previous one disconnects. This design makes it a **sequential server**: it handles one client at a time.The `Client` class is the other half of the communication system. It begins by creating a new `Socket` object that tries to connect to the server at `localhost` on port `1234`. Once connected, the client sets up input and output streams in the same way as the server. It uses a `Scanner` object to read input from the user’s console.Inside its loop, the client waits for the user to type a message. The message is sent to the server using the `BufferedWriter`, followed by `newLine()` and `flush()` to ensure it is immediately transmitted. After sending, the client waits for a response from the server. The server’s reply is read using `bufferedReader.readLine()` and displayed to the user’s console with the prefix `"Server:"`.If the user types `"BYE"`, the client breaks the loop, closes the socket, and terminates gracefully.When the server is started, it listens for connections. The client then connects, types a message, and sends it. The server prints the message and responds with `"MSG RECEIVED."`, which the client displays. This continues until `"BYE"` is typed, at which point the connection ends.This model is simple and effective for demonstrating socket communication. However, it only handles **one client at a time**, which limits its usefulness as a true chat system. By adding **multithreading** to the server, multiple clients could be supported simultaneously, enabling a real group chat. Features like private messaging, chat rooms, or graphical interfaces can also be built on top of this foundation.

*OUTPUT* :


