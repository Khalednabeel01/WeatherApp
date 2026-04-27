# WeatherApp
Microservices-based Weather App using Kubernetes, Docker, and Ingress with external API integration

# 🌦️ WeatherApp Microservices (Kubernetes + DevOps)

## 📌 Overview

WeatherApp is a Microservices project built using Kubernetes, providing:

* 🔐 Authentication Service
* 🌤️ Weather Service (fetches weather data from an external API)
* 🗄️ MySQL Database
* 🌐 Ingress Routing for access through Domain

The project aims to apply **DevOps + Kubernetes + Microservices Architecture** concepts practically.

---

## 📁 Project Structure

```
kubernetes-lab/
├── auth/
│   ├── README.md
│   └── mysql/
│       ├── deployment.yml
│       ├── headless-service.yml
│       ├── init-job.yml
│       ├── service.yml
│       └── statefulset.yml
├── ui/
│   ├── deployment.yml
│   ├── ingress.yml
│   └── service.yml
└── weather/
    ├── deployment.yml
    └── service.yml
```

---

## 🏗️ Architecture

* **weatherapp-auth** → Responsible for user registration
* **weatherapp-weather** → Responsible for fetching weather data
* **MySQL StatefulSet** → For data storage
* **Kubernetes Services** → For communication between services
* **Ingress (NGINX)** → To link the domain `weatherapp.local` to the services

---

## 🚀 Technologies Used

* Kubernetes (K8s)
* Docker
* Go (Backend Services)
* MySQL
* NGINX Ingress Controller
* GitHub

---

## ⚙️ Setup & Deployment

### 1️⃣ Clone the Project

```bash
git clone https://github.com/YOUR_USERNAME/weatherapp.git
cd weatherapp
```

---

### 2️⃣ Apply Kubernetes Resources

```bash
kubectl apply -f .
```

---

### 3️⃣ Create Secrets

```bash
kubectl create secret generic weather \
  --from-literal=apikey=YOUR_API_KEY
```

---

### 4️⃣ Run Ingress

Make sure you have NGINX Ingress Controller running

---

### 5️⃣ Edit hosts file

On your machine:

```
172.24.155.21   weatherapp.local
```

---

## 🌐 Usage

### From the browser:

```
http://weatherapp.local
```

### API:

```
http://weatherapp.local/cairo
```

---

## 🧪 Testing

```bash
curl http://weatherapp.local/cairo
```

---

## 🔐 Security

* Use Kubernetes Secrets to manage API Keys
* Do not store any sensitive data inside the code

---

---

## 👨‍💻 Author

Khaled Nabil
DevOps Engineer | Kubernetes Enthusiast
