# WeatherApp
Microservices-based Weather App using Kubernetes, Docker, and Ingress with external API integration

# 🌦️ WeatherApp Microservices (Kubernetes + DevOps)

## 📌 Overview

WeatherApp هو مشروع Microservices مبني باستخدام Kubernetes، بيقدم:

* 🔐 Authentication Service
* 🌤️ Weather Service (بيجيب بيانات الطقس من API خارجي)
* 🗄️ MySQL Database
* 🌐 Ingress Routing للوصول من خلال Domain

المشروع هدفه تطبيق مفاهيم **DevOps + Kubernetes + Microservices Architecture** بشكل عملي.

---

## 🏗️ Architecture

* **weatherapp-auth** → مسؤول عن تسجيل المستخدمين
* **weatherapp-weather** → مسؤول عن جلب بيانات الطقس
* **MySQL StatefulSet** → لتخزين البيانات
* **Kubernetes Services** → للتواصل بين الخدمات
* **Ingress (NGINX)** → لربط الدومين `weatherapp.local` بالخدمات

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

### 1️⃣ Clone المشروع

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

### 3️⃣ إنشاء Secrets

```bash
kubectl create secret generic weather \
  --from-literal=apikey=YOUR_API_KEY
```

---

### 4️⃣ تشغيل Ingress

تأكد إنك مشغل NGINX Ingress Controller

---

### 5️⃣ تعديل hosts file

على جهازك:

```
172.24.155.21   weatherapp.local
```

---

## 🌐 Usage

### من المتصفح:

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

* استخدام Kubernetes Secrets لإدارة API Keys
* عدم تخزين أي بيانات حساسة داخل الكود

---

## 📂 Project Structure

```
.
├── auth-service/
├── weather-service/
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   └── statefulset.yaml
└── README.md
```

---

## 💡 Future Improvements

* CI/CD باستخدام GitHub Actions
* Monitoring (Prometheus + Grafana)
* استخدام Helm Charts
* إضافة Redis caching

---

## 👨‍💻 Author

Khaled Nabil
DevOps Engineer | Kubernetes Enthusiast

---

## ⭐ Notes

المشروع ده هدفه التعلم والتطبيق العملي لمفاهيم:

* Microservices
* Kubernetes Networking
* Secrets Management
* Ingress Routing

---
