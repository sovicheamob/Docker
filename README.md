# 🐳 Project Docker Setup

This project runs using Docker only.

---

## 🚀 Start Services

```bash
docker compose up -d

🛑 Stop Services
docker compose down

📦 Create Volume (first time only)
docker volume create sqlserver-data

🔍 Check Running Containers
docker ps

📋 View Logs
docker logs sqlserver

🧹 Reset Everything (Remove Containers + Volume)
docker compose down -v

⚡ Full Comparison Table
| Command                    | Purpose           | Creates? | Stops? | Removes?       | Data Safe?
| ---------------            | ----------------- | -------- | ------ | ------------   | ----------
| `docker compose up -d`     | Start project     | ✔ Yes    | ❌    | ❌             | ✔
| `docker stop`              | Pause container   | ❌       | ✔     | ❌             | ✔
| `docker start`             | Resume container  | ❌       | ❌    | ❌             | ✔
| `docker restart`           | Refresh container | ❌       | ✔     | ❌             | ✔
| `docker compose down`      | Stop project      | ❌       | ✔ all | ✔ containers   | ✔
| `docker compose down -v`   | Stop project      | ❌       | ✔ all | ✔ containers   | ❌❌ DELETE DATA
