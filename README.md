💬 RealTime-ChatApp (Spring Boot + WebSocket)
A high-performance, real-time chat application built on a robust Spring Boot backend using WebSockets (STOMP) for low-latency communication and a dynamic React frontend. This application demonstrates scalable server-to-client messaging capabilities essential for modern web services.

✨ Features
Real-Time Messaging: Instant, bidirectional communication using Spring Boot WebSocket (STOMP).

User Status Tracking: Tracks when users join and leave the chat room.

Scalable Architecture: Clean separation of concerns with a Java backend and JavaScript frontend.

Intuitive Interface: Simple, responsive UI for a seamless chat experience.

🛠️ Tech Stack
Layer	Technology	Role
Backend	Spring Boot	REST API and primary WebSocket server framework.
Messaging	WebSockets (STOMP)	Enables bi-directional, persistent connection for real-time updates.
Language	Java	Core backend language.
Frontend	React	User Interface for displaying chat messages.
Client	Stomp.js / SockJS	JavaScript libraries for handling WebSocket connection on the client side.

Export to Sheets
⚙️ Setup and Installation
Prerequisites
Java 17+ (or higher, as required by Spring Boot)

Maven

Node.js & npm (for the React client)

1. Backend Setup
Clone the repository:

Bash

git clone https://github.com/Harshitha9407/RealTime-ChatApp.git
cd RealTime-ChatApp/Chatapp
Build the project using Maven:

Bash

mvn clean install
Run the Spring Boot application:

Bash

mvn spring-boot:run
The server will start on http://localhost:8080.

2. Frontend Setup
The frontend (React app, if separate) should be located within a subdirectory.

Navigate to the frontend directory:

Bash

cd [Your React Client Directory Name] # e.g., cd chat-client
Install dependencies:

Bash

npm install
Start the development server:

Bash

npm start # or npm run dev, depending on your setup
The chat application will be available in your browser (typically on http://localhost:3000 or http://localhost:5173).

📡 WebSocket Endpoints
The application uses STOMP over WebSockets for efficient messaging.

Type	Endpoint	Description
Connection	/ws	The primary WebSocket endpoint for clients to connect.
Subscribe	/topic/public	Clients subscribe to this topic to receive all public chat messages.
Send	/app/chat.sendMessage	Clients send new chat messages to this destination.
Send	/app/chat.addUser	Clients send a message to register a new user entering the chat.

Export to Sheets
💻 Project Structure
The structure demonstrates a typical Spring Boot REST/WebSocket application layout:

RealTime-ChatApp/
├── Chatapp/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/chat/app/
│   │   │   │   ├── config/ (WebSocketConfig.java)
│   │   │   │   ├── controller/ (ChatController.java)
│   │   │   │   └── model/ (ChatMessage.java)
│   │   └── resources/
│   └── pom.xml
└── [Your React Client Directory] (Not shown, but hosts the UI)
✍️ Author
Harshitha Gummadi

GitHub: @Harshitha9407
