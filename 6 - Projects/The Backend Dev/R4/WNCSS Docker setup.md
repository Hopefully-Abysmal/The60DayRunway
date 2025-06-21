## 🐳 Docker Setup for Local Development

This project includes a full Docker Compose setup for running the backend (PostgreSQL + Gradle + App) without needing to install Java or Postgres on your machine.

### 🔧 Prerequisites

- **Docker** and **Docker Compose plugin** installed  
    _(Test with `docker compose version`)_
    
- Recommended: Linux/macOS system or WSL2 if on Windows
    

---

### 🚀 Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/wnc-supply-sites/wnc-supply-sites.git
cd wnc-supply-sites

# 2. Bring up the full dev environment
docker compose up --build
```

This will spin up:

- A `PostgreSQL` database pre-seeded with schema (via Flyway)
    
- A `Gradle` container to build the Spring Boot app
    
- The backend Spring Boot `app` on [http://localhost:8000](http://localhost:8000/)
    

---

### 📦 What Docker Compose Does

|Service|Role|Notes|
|---|---|---|
|`database`|PostgreSQL 16.6|Port 5432 exposed as `localhost:5000`|
|`flyway`|Runs DB migrations|Applies scripts from `./schema/sql`|
|`gradle`|Builds backend .jar|Uses `./webapp/gradlew` to build the app|
|`app`|Runs the Spring Boot backend|Serves on `localhost:8000`|

---

### ⚠️ Common Gotchas

#### 1. ❌ `docker compose` not found?

Install Docker from the [official instructions](https://docs.docker.com/compose/install/). The plugin is now separate from the legacy `docker-compose`.

#### 2. 🔐 App doesn't load (500 error)

Make sure the database has the required dev data. If you're missing data like the `deployment` entry for `localhost`, either:

- Manually insert it
    
- Or request a seed SQL dump from the team
    

#### 3. 🧪 Tests fail with DB constraints

Run `./gradlew spotlessApply test` inside `webapp/` to apply formatting and run unit tests. Some test failures may be due to seed logic or duplicate inserts — not actual bugs.

---

### 🔁 Rebuilding the Test DB

To reset the test DB (`wnc_helene_test`) with the latest migrations:

```bash
./recreate-database.sh
```

If you changed the database password or schema manually, this script ensures a fresh test DB state.

---

### 🛠️ Accessing the DB (inside Docker)

```bash
docker exec -it wnc-supply-sites-database-1 psql -U postgres -d wnc_helene_test
```

---

### 💡 Tips

- The app expects to find a `deployment` row matching `localhost:8000`. If not found, it will crash with `Expected one element, but found none`.
    
- You can inspect schema state using:
    

```bash
docker exec -it wnc-supply-sites-database-1 psql -U postgres -d wnc_helene_test -c "\dt"
```

---
