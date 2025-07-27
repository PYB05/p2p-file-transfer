P2P File Transfer System
========================

A Peer-to-Peer (P2P) file transfer application with:

- Hashing-based error correction  
- Optional encryption  
- Parallel file chunk processing  

This system enables efficient and secure file sharing using WebRTC and WebSocket.

--------------------------------------------

Features
--------

- Direct browser-to-browser file sharing  
- Chunked file transfer for better performance  
- Hash verification for error detection and correction  
- AES encryption support (optional)  
- Real-time connection via WebRTC  
- WebSocket-based signaling server  

--------------------------------------------

Technologies Used
-----------------

Frontend: HTML, CSS, JavaScript  
Backend: Node.js (for signaling server)  
Libraries:  
  - WebRTC  
  - Socket.IO  
  - CryptoJS (for hashing and encryption)  

--------------------------------------------

Getting Started
---------------

1. Clone the Repository

   git clone https://github.com/PYB05/p2p-file-transfer.git
   cd p2p-file-transfer

2. Install Node.js (for signaling server)

   Download from: https://nodejs.org

3. Run the Signaling Server

   cd server
   npm install
   node index.js

   The signaling server will run at: ws://localhost:3000

4. Launch the Web App

   - Open index.html in two different browsers or systems  
   - One acts as Sender, the other as Receiver  
   - Select file → Establish connection → Start transfer  

--------------------------------------------

Folder Structure
----------------

p2p-file-transfer/  
├── index.html  
├── style.css  
├── script.js  
├── server/  
│   ├── index.js  
│   └── package.json  
└── README.txt  

--------------------------------------------

How It Works
------------

1. Sender selects a file  
2. File is split into chunks  
3. Each chunk is hashed using SHA-256  
4. (Optional) Each chunk is encrypted using AES  
5. Chunks are sent over WebRTC DataChannels  
6. Receiver verifies chunks via hash  
7. Chunks are reassembled into the original file  

--------------------------------------------

Future Improvements
-------------------

- Mobile browser support  
- In-app messaging during transfers  
- Transfer pause/resume  
- Cloud sync backup  

## Author

https://github.com/PYB05
https://github.com/RyanFlame27
