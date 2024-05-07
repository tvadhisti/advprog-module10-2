# Reflection 2.1

![Image 07-05-24 at 23 56](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/8bb7bbd6-6a23-4d36-acc6-fdba75c83550)
![Image 07-05-24 at 23 57](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/d33763a6-8e9a-42e2-8cea-d52e53e5ec77)
![Image 07-05-24 at 23 57 (1)](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/f9db1d71-3858-46b3-aa42-17ebed50aa12)
![Image 07-05-24 at 23 57 (2)](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/4e100ba3-8133-404f-9f18-e87ced1da6b4)

How to run it:

I began by launching the server using the command ```cargo run --bin server```, which listened for incoming messages. Next, I opened three separate terminals and started a client in each using ```cargo run --bin client```. This connected each client to the server. When I typed and sent a message from any of the client terminals, that message was sent to the server, which then broadcasted it to all connected clients.

What happens when I type some text in the clients:

When I type and send a message from any client, the message is first sent to the server. The server, which is continuously listening for incoming data from connected clients, receives this message. Upon receipt, the server immediately broadcasts this message to all other clients that are connected to it. Each client then receives the message from the server and displays it in their respective terminals. This process ensures that every participant in the chat can see and respond to each message in realtime.


