
#   OPEN SYSTEM INTERCONNECTION (OSI) MODEL
This text covers the features of "OPEN SYSTEM INTERCONNECTION (OSI)" model introduced by the International organization for standardization (ISO) in 1984.


![N|Solid](https://media.geeksforgeeks.org/wp-content/uploads/computer-network-osi-model-layers.png)

## Why do we need it?
Suppose we have two different computers with distinct operating systems e.g., windows and MAC OS connected to the same network over LAN cable, RJ45 connectors, and network interface card (NIC).
Without the presence of this OSI model, these two systems can't communicate with each other as encryption, decryption methods used are different for each operating system.
As the name suggests this model is used for interconnection between different types of operating systems.
OSI model consists of seven layers in total. In the sender’s system, each layer serves as input to the layer after it and obtains its input from the layer before it. The same process is vice versa in the receiver’s system.

>In simple terms, data to be transmitted from the sender’s system is processed in the application layer at the start, then passed on to each successive layer after it for further processing and then transmitted to the receiver’s system through a physical media connected at the physical layer. When this data is received at the destination system at the physical layer, it is processed and passed on to each successive layer after it (in the reverse order as in the sender's system) for further processing which is then understood by the receiver’s system at the application layer.

Each layer consists of its protocols, Let's dig in deep into each of the layers now:
### Layer1: Application layer 
The **application layer** consists of the various protocols used by applications for communication. e.g. (protocol eg HTTP, POP3, FTP, HTTPS, SMTP).
### Layer 2: Presentation layer
The **presentation layer** has the following main functions:
- ***Translation***- It converts characters and numbers received from the previous layer to machine-readable binary format.
- ***Data compression***- It reduces no. of bits required to represent data which can be done in two ways viz.
    1. _Lossy_ 
    2. _Lossless_
- ***Encryption*** - This is done to maintain the integrity and security of data. The sender encrypts the data (the receiver decrypts data). For achieving this,  Secure Sockets Layer (SSL) is used.

### Layer 3- Session layer 
This layer sets up and manages the connection enabling sending and receiving of data and also terminates the connection once data transfer is done. The major functions of the session layer are:
- ***Session management***- This ensures correct image and text from the server are delivered to the correct image and text on the web browser.
- ***Authentication***- It checks for the user is registered or not with the help of a user ID and password.
- ***Authorization***- It checks if the user has permission to access the file on the server.

### Layer 4- Transport layer
This layer has the following major features:
- ***Segmentation***- It converts the data to data units with sequence no. and source & destination port no. to which the application is listening (e.g. chrome, firefox, etc.)

- ***Flow control***- It controls the amount of data being transmitted i.e., increase or reduce the speed of data transmission

- ***Error control***- This can be done with the help of an auto-repeat request to read corrupt data

Data can be transferred using:-
1.  The _transmission control protocol_ (TCP) is slow but transfers complete data due to feedback. TCP is used for email, etc.
2.  The _User datagram protocol_ (UDP) is fast but can't be sure if some data is lost. UDP is used for live streaming, etc.

### Layer 5- Network layer
Features of the **network layer** are as follows:
- ***Logical addressing*** based on IPV4, IPV6, and mask
- ***Routing*** which determines the destination route based on mask and IPV.
- ***Path determination*** which selects the best possible path for data delivery using:- 
    1.  _Open Shortest Path First_ (OSPF)
    2.  _Border Gateway Protocol_ (BGP)
    3.  _Intermediate System-Intermediate System_ (IS-IS)

The network layer is responsible for Logical addressing.
The network layer converts data into Data packets that contain the receiver and sender's IP address.

### Layer 6- Data Link Layer
**Data Link Layer** is responsible for Physical addressing based on MAC address.
It converts the data packet into a Frame by adding head and tail.
Its feature of Media access control keeps an eye on the availability of shared media to be used for the transmission of data to avoid collision of various data sources.
### Layer 7- Physical layer
This layer converts the bits received from the previous layer into the signal which is transmitted.
A signal is generated based on the type of media connected e.g., voltage signal for copper cable, light signal for optical fiber, and radio signals for air transmission.

#### References


| Sr. no. | Source | Details |
| ------ | ------ | ------ | 
| 1 | Text |[(https://docs.microsoft.com/en-US/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model)](https://docs.microsoft.com/en-US/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) |
| 2 | Video | [(https://www.youtube.com/watch?v=vv4y_uOneC0)](https://www.youtube.com/watch?v=vv4y_uOneC0) |
| 3  | ISO Standard **ISO / IEC 7498 -1: 1994 (E)**| Information Technology- Open Systems Interconnection- Basic Reference Model: The Basic Model |
