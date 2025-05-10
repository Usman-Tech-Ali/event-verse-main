//write project description

# 🎉 Event-Verse - Event Management System (EMS)

Event-Verse is a full-stack Event Management System designed to simplify the management and participation in events. Built for attendees, organizers, and staff, the platform streamlines event registration, feedback collection, and personalized engagement.

## 🚀 Features

- 🔐 **Secure Authentication**: JWT-based login system for attendees, staff, and administrators.
- 📝 **Event Registration**: Users can explore, register, and manage their event participation.
- ❤️ **Preferences Module**: Attendees can select their interests for tailored event suggestions.
- 🔔 **Smart Reminders**: Email and in-app notifications for upcoming events and trailer releases.
- 🗣 **Feedback System**: Post-event feedback submission with rating and comments.
- 📊 **Admin Dashboard**: Manage users, create events, and view analytics.
- 🌐 **Modern UI**: Responsive and interactive frontend with smooth transitions.

## 🛠 Tech Stack

### 🔧 Backend

- Node.js
- Express.js
- MongoDB (Mongoose ODM)
- JWT for Authentication

### 🎨 Frontend

- React.js
- Tailwind CSS / CSS3
- Axios for API Integration
- React Router

### 📫 Other Tools

- Postman (for API testing)
- Git & GitHub for version control
- Nodemailer (for email reminders)

## 📁 Project Structure

Event-Verse/
├── app/
│ ├── backend/ # Node.js backend
│ │ ├── controllers/
│ │ ├── models/
│ │ ├── routes/
│ │ ├── middlewares/
│ │ └── .env # Environment variables
│ └── frontend/ # React frontend
│ ├── components/
│ ├── pages/
│ ├── hooks/
│ └── assets/
├── README.md
└── package.json

## 🧪 How to Run Locally

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/event-verse-main.git
   cd event-verse-main
   ```
2. **Set Up Environment Variables**
   Create a .env file inside app/backend/
   PORT=5000
   MONGO_URI=your_mongo_connection_string
   JWT_SECRET=your_jwt_secret
   EMAIL_USER=your_email
   EMAIL_PASS=your_password
   add your stripe key
3. **Install Dependencies**
   Backend
   cd app/backend
   npm install
   Frontend
   cd app/frontend
   npm install
4. **Start the Application**
   Backend
   cd app/backend
   npm start
   Frontend
   cd app/frontend
   npm start
   --done
