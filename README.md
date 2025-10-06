💬 RealTime-ChatApp (Spring Boot + WebSocket)

A high-performance, real-time chat application built on a robust Spring Boot backend using WebSockets (STOMP) for low-latency communication and a dynamic React frontend.
This project demonstrates scalable, real-time server-to-client messaging — a key capability for modern web applications.

✨ Features

💬 Real-Time Messaging – Instant, bidirectional communication using Spring Boot WebSocket (STOMP).

🟢 User Status Tracking – Tracks when users join and leave chat rooms.

⚙️ Scalable Architecture – Clean separation of backend (Spring Boot) and frontend (React).

🎨 Intuitive Interface – Simple, responsive UI for a seamless chat experience.

🛠️ Tech Stack
Layer	Technology	Role
Backend	Spring Boot	REST API and WebSocket server framework.
Messaging	WebSockets (STOMP)	Enables bi-directional, persistent connection for real-time updates.
Language	Java	Core backend language.
Frontend	React	User interface for displaying chat messages.
Client	Stomp.js / SockJS	Handles WebSocket connection on the client side.
⚙️ Setup and Installation
🔧 Prerequisites

Java 17+

Maven

Node.js & npm (for the React client)

🖥️ 1. Backend Setup

Clone the repository:

git clone https://github.com/Harshitha9407/RealTime-ChatApp.git
cd RealTime-ChatApp/Chatapp


Build the project using Maven:

mvn clean install


Run the Spring Boot application:

mvn spring-boot:run


The server will start at http://localhost:8080
.

💻 2. Frontend Setup

Navigate to your React client directory:

cd [Your React Client Directory Name]  # e.g., cd chat-client


Install dependencies:

npm install


Start the development server:

npm start     # or npm run dev, depending on your setup


The frontend will run on http://localhost:3000
 (or http://localhost:5173
 for Vite).

📡 WebSocket Endpoints

The application uses STOMP over WebSocket for efficient and scalable messaging.

Type	Endpoint	Description
Connection	/ws	Primary WebSocket endpoint for clients.
Subscribe	/topic/public	Clients subscribe to this topic for public chat.
Send	/app/chat.sendMessage	Endpoint to send new chat messages.
Send	/app/chat.addUser	Registers a new user entering the chat.
📁 Project Structure
RealTime-ChatApp/
├── Chatapp/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/chat/app/
│   │   │   │   ├── config/        # WebSocketConfig.java
│   │   │   │   ├── controller/    # ChatController.java
│   │   │   │   └── model/         # ChatMessage.java
│   │   └── resources/
│   └── pom.xml
└── [Your React Client Directory]   # React frontend (UI)

👩‍💻 Author

Harshitha Gummadi
🔗 GitHub: @Harshitha9407
