# Reflection 2.1

![Image 07-05-24 at 23 56](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/8bb7bbd6-6a23-4d36-acc6-fdba75c83550)
![Image 07-05-24 at 23 57](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/d33763a6-8e9a-42e2-8cea-d52e53e5ec77)
![Image 07-05-24 at 23 57 (1)](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/f9db1d71-3858-46b3-aa42-17ebed50aa12)
![Image 07-05-24 at 23 57 (2)](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/4e100ba3-8133-404f-9f18-e87ced1da6b4)

How to run it:

I began by launching the server using the command ```cargo run --bin server```, which listened for incoming messages. Next, I opened three separate terminals and started a client in each using ```cargo run --bin client```. This connected each client to the server. When I typed and sent a message from any of the client terminals, that message was sent to the server, which then broadcasted it to all connected clients.

What happens when I type some text in the clients:

When I type and send a message from any client, the message is first sent to the server. The server, which is continuously listening for incoming data from connected clients, receives this message. Upon receipt, the server immediately broadcasts this message to all other clients that are connected to it. Each client then receives the message from the server and displays it in their respective terminals. This process ensures that every participant in the chat can see and respond to each message in realtime.

# Reflection 2.2

To successfully change the port to 8080, we need to adjust the port settings in both the ```client.rs``` and ```server.rs``` files. It's important because the server and client sides of the application must listen and connect on the same port for the network communication to function properly. Mismatched settings will result in the clients failing to connect to the server. After modifying the port in the ```erver.rs``` file where the server listens for incoming connections, we must also update the corresponding port in the ```client.rs``` file. This ensures that the clients try to connect to the correct port. Aligning these settings is important for establishing a successful connection between the client and the server.

# Reflection 2.3
![Image 08-05-24 at 00 36](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/4704df80-f00e-4179-92c6-4b232dab431f)
![Image 08-05-24 at 00 36 (1)](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/066e5aee-b764-40c6-a637-a1b7edcead45)
![Image 08-05-24 at 00 36 (2)](https://github.com/tvadhisti/advprog-module10-2/assets/127074983/569008c9-0d13-4364-9b45-179fa5291675)



We've recently improved our system by incorporating sender information into each message sent by a client. Now, each message includes the IP address and port number of the sender, details that can be clearly seen in the terminal output. This improvement was achieved by modifying the server's broadcasting functionality, ensuring that the sender's IP address and port from the addr variable are included whenever messages are sent to connected clients. As a result, this feature significantly improves the user experience. It allows each client to see not only the messages but also the source of those messages. This addition provides clarity and context, which are crucial in multi user communication. Overall, these changes make it easier for users to track conversations and understand who is participating.
