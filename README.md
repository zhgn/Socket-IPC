Socket-IPC
==========

Socket-IPC demo (server and client).

Note that this project is not aiming at doing something like QBus. Anyways, it may
evolve into something similar (as in broadcasting a message), But then again, it won't be anywhere
near QBus.

Code is fully functional and tested on Windows 7 and Linux 3.8 with QtCreator 2.6.2 and Qt 5.0.1

None of the signals/slots of both the server and the client part need any further documentation than the following.
Both classes will do exactly what you'd expect them to do. Nothing more and nothing less.

###Server

The following signals are emitted:

```cpp
void clientConnected(int clientID);

void newMessageFromClient(int clientID, QString message);

void clientDisconnected(int clientID);
```

Also, there are two public slots (methods):

```cpp
void disconnectClient(int clientID);

void sendMessageToClient(int clientID, QString message);
```

A small demo can be found in the ```main.cpp``` file inside the ```server``` folder.



###Client

The following signals are emitted:

```cpp
void disconnected();

void  newMessageFromServer(QString message);
```

Also, there are two public slots (methods):

```cpp
void disconnect();

void sendMessage(QString message);
```

A small demo can be found in the ```main.cpp``` file inside the ```client``` folder.