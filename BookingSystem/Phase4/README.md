# **Quick Start Guide — Booking System Containers (Phase 4)**

---

## 1. Requirements 🚀

* Docker + Docker Compose installed
* You have already completed **Phase 3**, which created project

  * 📦 `cybersec-phase1-part1`
  * 📦 `cybersec-phase1-part2`
  * 📦 `cybersec-phase2`
  * 📦 `cybersec-phase3`

* You now download [`docker-compose.yml`](https://github.com/vheikkiniemi/CybersecurityAndDataPrivacySpring2026/blob/main/BookingSystem/Phase4/docker-compose.yml) for **Phase 4** into its own folder, which will create

  * 📦 `cybersec-phase4`


---

## 2. Start Phase 4 ▶️

In the folder where the **Phase 4** `docker-compose.yml` is stored:

```bash
docker compose up -d
```

**Debian-based → sudo:**

```bash
sudo docker compose up -d
```

This starts:

* 🗄️ `cybersec-db-phase4` (PostgreSQL database)
* 🌐 `cybersec-web-phase4` (web application)

---

## 3. Access the application 🌍

* Open browser:  

  `cybersec-phase1-part1` 👉  `http://localhost:8001`  
  `cybersec-phase1-part2` 👉  `http://localhost:8002`  
  `cybersec-phase2` 👉  `http://localhost:8003`  
  `cybersec-phase3` 👉  `http://localhost:8004`  
  `cybersec-phase4` 👉  `http://localhost:8006`

---

* PostgreSQL from host:  

  `cybersec-phase1-part1` 👉 
    ```bash
    docker exec -it cybersec-db-phase1-part1 psql -U postgres -d postgres
    ```
  `cybersec-phase1-part2` 👉 
    ```bash
    docker exec -it cybersec-db-phase1-part2 psql -U postgres -d postgres
    ```
  `cybersec-phase2` 👉 
    ```bash
    docker exec -it cybersec-db-phase2 psql -U postgres -d postgres
    ```
  `cybersec-phase3` 👉 
    ```bash
    docker exec -it cybersec-db-phase3 psql -U postgres -d postgres
    ```
  `cybersec-phase4` 👉 
    ```bash
    docker exec -it cybersec-db-phase4 psql -U postgres -d postgres
    ```
---

## 4. Check that both projects exist 🔍

### In Docker Desktop

1. Open **Docker Desktop**
2. Go to **Containers** tab
3. You should see two Compose projects:

   * `cybersec-phase1-part1` (from earlier part)
   * `cybersec-phase1-part2` (from earlier part)
   * `cybersec-phase2` (from earlier part)
   * `cybersec-phase3` (from earlier part)
   * `cybersec-phase4` (this new one)

Each project will have its own containers listed under it.

---

### From command line

```bash
docker compose ls
```

**Debian-based → sudo:**

```bash
sudo docker compose ls
```

You should see **all** names in the list:

```text
NAME                      STATUS
cybersec-phase1-part1     ...
cybersec-phase1-part2     ...
cybersec-phase2     ...
cybersec-phase3     ...
cybersec-phase4     ...
```

---

## 5. View logs 🧾

All services (in current project folder):

```bash
docker compose logs -f
```

**Debian-based → sudo:**

```bash
sudo docker compose logs -f
```

---

**Single service:**

```bash
docker compose logs -f web
docker compose logs -f database
```

**Debian-based → sudo:**

```bash
sudo docker compose logs -f web
```
```bash
sudo docker compose logs -f database
```

---

## 6. Stop and clean up 🧹

Stop containers (keep data):

```bash
docker compose down
```

**Debian-based → sudo:**

```bash
sudo docker compose down
```

---

Stop containers **and delete database data** (Phase 4 only):

```bash
docker compose down -v
```

**Debian-based → sudo:**

```bash
sudo docker compose down -v
```

Single service:

```bash
sudo docker compose down 'database' -v
sudo docker compose down 'web' -v
```

Use `-v` only if you are OK with **losing all PostgreSQL data** for this project.
