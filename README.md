 📰 MERN Blog App

A full-featured blog application built using the **MERN stack (MongoDB, Express.js, React.js, Node.js)**. This app supports blog post creation, editing, deletion, commenting, image uploads, pagination, filtering, and more.

---

## 📁 Project Structure

mern-blog-app/
├── client/ # Frontend (React + Vite + TailwindCSS)
│ ├── src/
│ │ ├── components/
│ │ ├── pages/
│ │ ├── services/
│ │ └── App.jsx
│ ├── public/
│ └── .env.example
├── server/ # Backend (Node.js + Express + MongoDB + Mongoose)
│ ├── controllers/
│ ├── models/
│ ├── routes/
│ ├── uploads/
│ └── .env.example
├── README.md

yaml
Always show details

Copy

---

## 🚀 Features Implemented

- 📝 CRUD blog posts (Create, Read, Update, Delete)
- 📷 Upload featured images
- 🔍 Search by title/content
- 🏷️ Filter by category
- 📄 Pagination for post lists
- 💬 Add and view comments
- 📦 RESTful API with proper error handling and validation
- 🔐 Authentication-ready structure (easy to extend)

---

## ⚙️ Tech Stack

- **Frontend:** React, Tailwind CSS, React Router, Axios
- **Backend:** Node.js, Express.js, MongoDB, Mongoose, Multer
- **State Management:** React Hooks (useState, useEffect)
- **Other:** Vite, PNPM, Nodemon, dotenv

---

## 🧪 Screenshots

| Post List | Create Post | Single Post + Comments |
|-----------|-------------|------------------------|
| ![Post List](C:\Users\DG\OneDrive\Desktop\week-4-mern-integration-assignment-Julius-Nganga\screenshotss\Screenshot 2025-07-10 091312.png) | ![Create Post]() | ![Post Detail](C:\Users\DG\OneDrive\Desktop\week-4-mern-integration-assignment-Julius-Nganga\screenshotss\Screenshot 2025-07-10 091345.png) |

---

## 📦 Setup Instructions

### 🛠 Requirements

- Node.js >= v18
- MongoDB local or Atlas cluster
- PNPM (preferred): `npm i -g pnpm`

---

### 🖥 Server Setup (Backend)

```bash
cd server
pnpm install
cp .env.example .env
# Update .env with your MongoDB URI and PORT
pnpm dev
🌐 Client Setup (Frontend)
bash
Always show details

Copy
cd client
pnpm install
cp .env.example .env
# Set VITE_API_BASE_URL (e.g. http://localhost:5000/api)
pnpm dev
🔐 Environment Variables
🗂 server/.env.example
env
Always show details

Copy
PORT=5000
MONGO_URI=your_mongodb_connection_string
UPLOAD_FOLDER=uploads
🗂 client/.env.example
env
Always show details

Copy
VITE_API_BASE_URL=http://localhost:5000/api
📘 API Documentation
📝 Posts
Method	Endpoint	Description
GET	/api/posts	List all posts (supports search, page, limit, category)
GET	/api/posts/:id	Get single post
POST	/api/posts	Create new post
PUT	/api/posts/:id	Update post
DELETE	/api/posts/:id	Delete post

🗂 Categories
Method	Endpoint
GET	/api/categories
POST	/api/categories

💬 Comments
Method	Endpoint	Description
GET	/api/posts/:id/comments	List comments for a post
POST	/api/posts/:id/comments	Add a new comment

🖼 Uploads
Method	Endpoint
POST	/api/upload (form-data with image)

🙌 Credits
Built with ❤️ using the MERN stack.