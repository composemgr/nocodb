## 👋 Welcome to nocodb 🚀

NocoDB - Open-source Airtable alternative

## 📋 Description

NocoDB turns any MySQL, PostgreSQL, SQL Server, SQLite & MariaDB into a smart spreadsheet. Build APIs in minutes, create custom views, collaborate with your team, and more.

## 🚀 Services

- **app**: NocoDB application (`nocodb/nocodb:latest`)
- **db**: PostgreSQL database (`postgres:16-alpine`)

## 📦 Installation

### Using curl
```shell
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/nocodb/main/docker-compose.yaml" | docker compose -f - up -d
```

### Using git
```shell
git clone "https://github.com/composemgr/nocodb" ~/.local/srv/docker/nocodb
cd ~/.local/srv/docker/nocodb
docker compose up -d
```

### Using composemgr
```shell
composemgr install nocodb
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
BASE_HOST_NAME=nocodb.example.com
BASE_DOMAIN_NAME=example.com

# JWT Secret (generate: openssl rand -hex 32)
APP_JWT_TOKEN=changeme_jwt_token

# Admin Account
APP_ADMIN_USER=admin
APP_ADMIN_PASS=changeme_admin_password

# Database
DB_USER_NAME=nocodb
DB_USER_PASS=changeme_db_password
DB_CREATE_DATABASE_NAME=nocodb
```

## 🌐 Access

- **NocoDB UI**: http://localhost:8080
- **Default Admin**: See APP_ADMIN_USER and APP_ADMIN_PASS

## 📂 Volumes

- `./rootfs/data/nocodb` - Application data and attachments
- `./rootfs/db/postgres/nocodb` - Database files

## 🔐 Security

- Change default admin password immediately
- Use strong JWT secret
- Configure HTTPS with reverse proxy
- Enable 2FA for admin accounts
- Regular backups

## 🔍 Logging

```shell
docker compose logs -f app
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+
- 1GB+ RAM recommended

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
