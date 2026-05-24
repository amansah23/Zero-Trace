# ZeroTrace 🕶️

> A secure one-time secret sharing platform built with the MERN stack.

ZeroTrace is a privacy-focused web application that allows users to securely share sensitive information like passwords, API keys, tokens, and confidential notes using self-destructing links.

Once the secret is viewed, it is permanently deleted from the database.

No logs.  
No recovery.  
No trace.

---

## ✨ Features

- 🔐 AES encrypted secret storage
- ⏳ One-time readable secret links
- 🛡️ Security-focused backend architecture
- 📱 Fully responsive UI
- ⚡ Fast MERN stack implementation
- 🍪 Secure HttpOnly cookie support
- 🚫 Rate limiting & abuse protection

---

# 🛠️ Tech Stack

## Backend
- Node.js
- Express.js
- MongoDB + Mongoose
- JWT Authentication
- Crypto Module (AES Encryption)
- Joi Validation
- Helmet
- Express Rate Limit

## Frontend
- React.js (Vite)
- Tailwind CSS
- Axios
- React Router DOM

---

# 📂 Folder Structure

```bash
ZeroTrace/
│
├── backend/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   └── server.js
│
├── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── main.jsx
│
└── README.md


⚙️ Installation & Setup
1️⃣ Clone Repository
git clone <repository_url>
cd ZeroTrace
2️⃣ Backend Setup
cd backend
npm install

Create a .env file inside the backend directory:

PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
ENCRYPTION_KEY=your_32_character_key
ADMIN_PASSWORD=your_admin_password

⚠️ ENCRYPTION_KEY must be exactly 32 characters long.

Run backend server:

npm run dev

Backend runs at:

http://localhost:5000
3️⃣ Frontend Setup
cd frontend
npm install
npm run dev

Frontend runs at:

http://localhost:5173
📡 API Endpoints
Method	Endpoint	Description
POST	/api/secrets	Create a new secret
GET	/api/secrets/:id	Read & destroy a secret
POST	/api/admin/login	Admin authentication
GET	/api/admin/stats	Get active secrets count
🔒 Security Features
AES Encryption
Self-destructing secrets
JWT-based admin authentication
Joi input validation
Rate limiting
Secure HTTP headers via Helmet
HttpOnly secure cookies
CORS protection
🚀 Deployment
Frontend Deployment (Vercel)
Push project to GitHub
Import the frontend folder into Vercel
Configure:
Build Command: npm run build
Output Directory: dist
Backend Deployment (Render)
Create a new Web Service
Select backend as Root Directory
Configure:
Build Command: npm install
Start Command: npm start
Add these environment variables in Render dashboard:
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
ENCRYPTION_KEY=your_32_character_key
ADMIN_PASSWORD=your_admin_password
🎯 Purpose of the Project

ZeroTrace was built to explore:

Secure secret sharing systems
Encryption implementation
REST API development
Authentication & authorization
MERN stack architecture
Production deployment
🤝 Contributions

Pull requests, issues, and suggestions are welcome.

Feel free to fork the repository and improve the project.

⭐ Final Thought

"Some information should exist only once."