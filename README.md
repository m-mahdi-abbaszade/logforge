# LogForge: Real-time Observability Stack

LogForge is a Docker-based log monitoring system built with OpenSearch, Fluent Bit, and Nginx.

It collects logs in real-time and visualizes them using OpenSearch Dashboards.

---

## 🚀 Architecture

Nginx → Fluent Bit → OpenSearch → Dashboards

---

## ⚙️ Tech Stack

- OpenSearch (Search & Storage)
- OpenSearch Dashboards (Visualization)
- Fluent Bit (Log Processor)
- Nginx (Log Generator)
- Docker Compose (Orchestration)

---

# 📁 Project Structure

logforge/
│
├── docker-compose.yml
├── README.md
│
├── fluent-bit/
│ └── fluent-bit.conf
│
├── nginx/
│ └── logs/
│
└── screenshots/
└── dashboard.png

---

# 🚀 Getting Started

### 1️⃣ Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/logforge.git
cd logforge
```

### 2️⃣ Start the system

```bash
docker-compose up -d
```

### 3️⃣ Generate logs

```bash
curl http://localhost:8080
```

```bash
#Run multiple times:
for i in {1..20}; do curl http://localhost:8080; done
```

---

## 🌐 Services

- Nginx: http://localhost:8080

- Dashboards: http://localhost:5601

- OpenSearch: http://localhost:9200

---

## 📊 Dashboards Setup
1-Open OpenSearch Dashboards

2-Go to Discover

3-Create index pattern:

  nginx-logs*
  
4-Use time field:

  @timestamp

---

## 📈 Example Visualizations

You can build:

Request count over time

HTTP status code distribution (200/404/500)

Top client IPs

Traffic spikes monitoring

---

## 📸 Screenshot

![Dashboard](https://github.com/m-mahdi-abbaszade/logforge/blob/main/screenshots/Screenshot%202026-04-13%20120326.png)








