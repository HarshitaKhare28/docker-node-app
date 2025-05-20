# 🚀 Docker Node App

A simple Node.js application running inside a Docker container. This project demonstrates how to containerize a Node.js app using Docker.

---

## 📁 Project Structure

```
docker-node-app/
├── Dockerfile
├── app.js
├── package.json
├── .gitignore
└── README.md
```

---

## 🛠️ Technologies Used

- Node.js
- Express.js
- Docker

---

## 🐳 Run the App with Docker

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/docker-node-app.git
cd docker-node-app
```
## Build the Docker Image

docker build -t docker-node-app .

## Run the Container

docker run -p 3000:3000 docker-node-app

## Open in Browser

Visit: http://localhost:3000
## 📄 Dockerfile
```
FROM node:18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
```
