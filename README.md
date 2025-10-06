# 💬 RealTime-ChatApp

A high-performance, real-time chat application built with Spring Boot and WebSockets (STOMP) for low-latency communication and a dynamic React frontend. This project demonstrates scalable, real-time server-to-client messaging — a key capability for modern web applications.

## ✨ Features

- 💬 **Real-Time Messaging** – Instant, bidirectional communication using Spring Boot WebSocket (STOMP)
- 🟢 **User Status Tracking** – Tracks when users join and leave chat rooms
- ⚙️ **Scalable Architecture** – Clean separation of backend (Spring Boot) and frontend (React)
- 🎨 **Intuitive Interface** – Simple, responsive UI for a seamless chat experience

---

## 🛠️ Tech Stack

| Layer | Technology | Role |
|-------|-----------|------|
| **Backend** | Spring Boot | REST API and WebSocket server framework |
| **Messaging** | WebSockets (STOMP) | Enables bi-directional, persistent connection for real-time updates |
| **Language** | Java | Core backend language |
| **Frontend** | React | User interface for displaying chat messages |
| **Client** | Stomp.js / SockJS | Handles WebSocket connection on the client side |

---

## ⚙️ Setup and Installation

### 🔧 Prerequisites

- Java 17+
- Maven
- Node.js & npm (for the React client)

### 🖥️ 1. Backend Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Harshitha9407/RealTime-ChatApp.git
   cd RealTime-ChatApp/Chatapp
   ```

2. **Build the project using Maven:**
   ```bash
   mvn clean install
   ```

3. **Run the Spring Boot application:**
   ```bash
   mvn spring-boot:run
   ```

   The server will start at `http://localhost:8080`

### 💻 2. Frontend Setup

1. **Navigate to your React client directory:**
   ```bash
   cd [Your React Client Directory Name]  # e.g., cd chat-client
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the development server:**
   ```bash
   npm start     # or npm run dev, depending on your setup
   ```

   The frontend will run on `http://localhost:3000` (or `http://localhost:5173` for Vite)

---

## 📡 WebSocket Endpoints

The application uses STOMP over WebSocket for efficient and scalable messaging.

| Type | Endpoint | Description |
|------|----------|-------------|
| **Connection** | `/ws` | Primary WebSocket endpoint for clients |
| **Subscribe** | `/topic/public` | Clients subscribe to this topic for public chat |
| **Send** | `/app/chat.sendMessage` | Endpoint to send new chat messages |
| **Send** | `/app/chat.addUser` | Registers a new user entering the chat |

---

## 📁 Project Structure

```
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
```

---

## 🚀 How It Works

1. **Client Connection**: Users connect to the WebSocket server via `/ws` endpoint
2. **User Registration**: New users are registered through `/app/chat.addUser`
3. **Message Broadcasting**: Messages sent to `/app/chat.sendMessage` are broadcast to all subscribed clients at `/topic/public`
4. **Real-Time Updates**: All connected clients receive instant updates without polling

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/Harshitha9407/RealTime-ChatApp/issues).

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👩‍💻 Author

**Harshitha Gummadi**

- GitHub: [@Harshitha9407](https://github.com/Harshitha9407)
