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
- 🌐 **Modern UI**: Responsive and interactive frontend with smooth transitions.last

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

## Local Development

1. Start the frontend:

```bash
cd frontend
npm install
npm run dev
```

2. Start the backend:

```bash
cd backend
npm install
npm start
```

## Docker Build

1. Build frontend image:

```bash
cd frontend
docker build -t your-dockerhub-username/mern-frontend:latest .
```

2. Build backend image:

```bash
cd backend
docker build -t your-dockerhub-username/mern-backend:latest .
```

## Kubernetes Deployment

1. Start Minikube:

```bash
minikube start
```

2. Create namespace:

```bash
kubectl create namespace mern-app
```

3. Create MongoDB secret:

```bash
kubectl create secret generic mongodb-secret \
  --namespace mern-app \
  --from-literal=uri=your-mongodb-uri
```

4. Deploy the application:

```bash
cd k8s
kubectl apply -f frontend-deployment.yaml
kubectl apply -f backend-deployment.yaml
kubectl apply -f frontend-service.yaml
kubectl apply -f backend-service.yaml
```

5. Access the application:

```bash
minikube service frontend-service -n mern-app
```

## GitHub Actions Setup

1. Add the following secrets to your GitHub repository:

   - DOCKER_USERNAME
   - DOCKER_PASSWORD
   - MONGODB_URI

2. Set up a self-hosted runner on your machine where Minikube is running.

3. Push your code to the main branch to trigger the deployment.

## Monitoring

1. Check pod status:

```bash
kubectl get pods -n mern-app
```

2. Check services:

```bash
kubectl get services -n mern-app
```

3. Check deployments:

```bash
kubectl get deployments -n mern-app
```

## Troubleshooting

1. View pod logs:

```bash
kubectl logs <pod-name> -n mern-app
```

2. Describe resources:

```bash
kubectl describe pod <pod-name> -n mern-app
kubectl describe service <service-name> -n mern-app
```

## Cleanup

1. Delete the deployment:

```bash
kubectl delete -f k8s/
```

2. Delete the namespace:

```bash
kubectl delete namespace mern-app
```

3. Stop Minikube:

```bash
minikube stop
```
