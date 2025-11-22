# 🌟 CampusGenie: AI-Powered Multilingual Smart Assistant

A comprehensive full-stack web application designed to revolutionize university communication by providing **real-time**, **context-aware**, and **multilingual** information to students and faculty.

---

## 🚀 Features

### **Core Features**
- **Multilingual AI Chatbot (Selene):** Understands and responds in English, Hindi, and regional languages using the Gemini API.
- **Contextual RAG System:** Retrieves live data (Timetables, Circulars) from MongoDB to provide accurate, personalized answers.
- **Faculty Dashboard:** Secure portal for faculty to manage and publish live Timetable and Circular data (CRUD functionality).
- **Personalized Student Portal:** Central hub for accessing user-specific information and the AI assistant.
- **Secure Authentication:** Role-based access control (Student/Faculty).
- **AI Study Planner Framework:** Architectural foundation for generating personalized study schedules.

### **Technical Features**
- **Responsive Design:** Mobile-first UI using Tailwind CSS.
- **API Connectivity:** Axios with interceptors for streamlined handling.
- **Session Security:** Passport.js + express-session.
- **Data Persistence:** MongoDB integration with Mongoose ODM.
- **Maintainability:** Clean separation using MVC architecture.

---

## 🏗️ Architecture

### **Backend**
- **Framework:** Node.js + Express.js  
- **Database:** MongoDB with Mongoose  
- **AI Integration:** Google Generative AI SDK (Gemini 2.5 Flash)  
- **Authentication:** Passport.js (Local Strategy)  
- **Validation:** Joi Schema Validation  
- **Security:** Helmet, CORS, Rate Limiting  

### **Frontend**
- **Framework:** React + Vite  
- **Styling:** Tailwind CSS + shadcn/ui  
- **State Management:** React Context API  
- **Routing:** React Router v6+  
- **HTTP Client:** Axios with Interceptors  

---

## 📁 Project Structure

```
├── backend/
│   ├── config/          # DB, Session, CORS configuration
│   ├── controllers/     # Route handlers (includes chatbot logic)
│   ├── middleware/      # Custom middleware (isLoggedIn, isAdmin)
│   ├── models/          # MongoDB models (User, Timetable, Circular, ChatLog)
│   ├── routes/          # API routes (users, chatbot, timetable, circulars)
│   ├── utils/           # Utility helpers
│   └── app.js           # Main application file
├── frontend/
│   ├── src/
│   │   ├── components/  # Reusable UI components (ProtectedRoute)
│   │   ├── contexts/    # AuthContext & others
│   │   ├── hooks/       # Custom hooks
│   │   ├── pages/       # Portal, Dashboard, Login, etc.
│   │   ├── services/    # API services (auth, chatbot, timetable, circulars)
│   └── public/          # Static assets
└── .env                 # Environment variables
```

---

## 🛠️ Installation & Setup

### **Prerequisites**
- Node.js (v18+)
- MongoDB (Local or Atlas)
- npm or yarn
- Gemini API Key

---

## ⚙️ Backend Setup

```bash
cd backend
npm install
```

### Create **.env** in `backend/`
```
NODE_ENV=development
PORT=3000
MONGODB_URI=mongodb://localhost:27017/campusgenie
SESSION_SECRET=your-super-secure-session-secret-change-this
GEMINI_API_KEY=YOUR_AI_API_KEY_HERE
```

### Start Backend
```bash
npm run dev
```

---

## 🎨 Frontend Setup

```bash
cd frontend
npm install
```

### Create **.env** in `frontend/`
```
VITE_API_URL=http://localhost:3000
VITE_APP_NAME=CampusGenie
```

### Start Frontend
```bash
npm run dev
```

---

## 📡 API Documentation

### **Authentication**
- `POST /users/register` — Register  
- `POST /users/login` — Login  
- `POST /users/logout` — Logout  

### **Timetable API (CRUD)**
- `GET /timetable` — Get timetable  
- `POST /timetable` — Add a class  
- `DELETE /timetable/:id` — Delete class  

### **Circulars API**
- `GET /circulars` — Get all circulars  
- `POST /circulars` — Add new circular (Faculty)  
- `DELETE /circulars/:id` — Delete circular (Faculty)  

### **AI Chatbot**
- `POST /chatbot/chat` — Send prompt and get context-aware response  

---

## 🔒 Security Features

- **Passport.js Authentication**
- **Role-Based Authorization**
- **Input Validation with Joi**
- **Secure Sessions (connect-mongo)**
- **API Key Protection (Backend only)**
- **CORS Policies**
- **Helmet for HTTP security**

---

## 🤝 Contributing

1. Fork the repository  
2. Create a feature branch  
   ```bash
   git checkout -b feature/new-ai-feature
   ```
3. Commit your changes  
4. Push the branch  
5. Open a Pull Request  

---

## 📝 License
This project is licensed under the **ISC License**.

---

Made with ❤️ for a smarter campus worldwide.
