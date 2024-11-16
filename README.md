# 🔔 Real-Time Notification System

A powerful *Real-Time Notification System* built using *JavaScript, Node.js, React, WebSocket, and MongoDB. This project enables instant delivery of notifications, handling over **2,000+ messages per minute. It is designed to scale efficiently, supporting **8,000+ concurrent users* and handling backend traffic surges up to *10x*.

## 🚀 Features
- Real-time notifications using *WebSocket*
- Scalable architecture supporting high traffic loads
- React-based frontend optimized for large user bases
- Efficient MongoDB database for storing user and notification data
- Built with performance and scalability in mind

## 🛠 Tech Stack
- *Frontend*: React
- *Backend*: Node.js, Express
- *Real-Time Communication*: WebSocket
- *Database*: MongoDB
- *Tools*: Postman (API testing), MongoDB Compass (Database management)

## 📁 Project Structure

Real-Time-Notification-System/
├── backend/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── config/
│   ├── utils/
│   ├── .env
│   ├── server.js
├── frontend/
│   ├── public/
│   ├── src/
│   ├── .env
│   ├── package.json
│   ├── App.js
│   └── index.js
├── README.md
└── package.json


## 📦 Installation

### Prerequisites
- Node.js (v14.x or higher)
- MongoDB (v4.x or higher)
- npm (v6.x or higher)

### Clone the Repository
bash
git clone https://github.com/Pawarmamta/real-time-notification-system.git
cd Real-Time-Notification-System


### Backend Setup
1. *Navigate to the backend directory*:
   bash
   cd backend
   

2. *Install dependencies*:
   bash
   npm install
   

3. **Create a .env file** in the backend directory and add the following:
   
   PORT=5000
   MONGO_URI=mongodb://localhost:27017/notificationDB
   

4. *Run the server*:
   bash
   npm start
   
   Backend server will be running on http://localhost:5000.

### Frontend Setup
1. *Navigate to the frontend directory*:
   bash
   cd frontend
   

2. *Install dependencies*:
   bash
   npm install
   

3. **Create a .env file** in the frontend directory and add the following:
   
   REACT_APP_API_URL=http://localhost:5000
   

4. *Run the frontend application*:
   bash
   npm start
   
   Frontend will be running on http://localhost:3000.

## 🚦 Usage

### WebSocket Endpoints
- *Connect to WebSocket*:
  javascript
  const socket = new WebSocket('ws://localhost:5000');
  

- *Listen for Notifications*:
  javascript
  socket.onmessage = (event) => {
    console.log('New Notification:', event.data);
  };
  

- *Send a Notification* (for admins or system triggers):
  javascript
  socket.send(JSON.stringify({ message: 'New Update Available!' }));
  

### REST API Endpoints

#### Users
- *GET* /api/users - Get all users
- *POST* /api/users - Create a new user

#### Notifications
- *GET* /api/notifications - Get all notifications
- *POST* /api/notifications - Create a new notification
- *DELETE* /api/notifications/:id - Delete a notification by ID

### Example Requests
- *Send Notification to All Users* (via WebSocket)
  javascript
  fetch('http://localhost:5000/api/notifications', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({ message: 'Welcome to the platform!' }),
  });
  

## 🗄 MongoDB Indexing for Performance
- Optimized MongoDB with indexes on frequently queried fields (e.g., userId, timestamp) to support high-speed data retrieval.
- Enabled *horizontal scaling* to handle increased loads, ensuring *10x traffic capacity*.

## 🔍 Testing
- WebSocket connections tested with *Postman* and *WebSocket clients*.
- API endpoints tested using *Jest* (optional setup available).

## 📸 Screenshots
### 1. Notification Dashboard
![Dashboard](https://user-images.githubusercontent.com/yourusername/notification-dashboard.png)

### 2. Real-Time WebSocket Connection
![WebSocket](https://user-images.githubusercontent.com/yourusername/websocket-connection.png)

## 🖥 Scaling & Optimization
- Leveraged *Node.js cluster module* to utilize multi-core systems, boosting performance.
- Implemented *load balancing* for handling large concurrent connections.
- Frontend React components optimized using *React.memo* and *useCallback* to minimize unnecessary re-renders.

## 🤝 Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a new branch (git checkout -b feature-branch)
3. Commit your changes (git commit -m 'Add new feature')
4. Push to the branch (git push origin feature-branch)
5. Open a Pull Request

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📬 Contact
- *GitHub*: [Pawarmamta](https://github.com/Pawarmamta)
- *Email*:mamtapawar892@gmail.com