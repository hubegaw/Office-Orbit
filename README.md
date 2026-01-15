# Office Orbit - Desk Booking System For Your Office

Modern desk booking application with interactive office maps, issue reporting, and comprehensive monitoring.

## 🚀 Tech Stack

### Backend
- **Java 25** with **Quarkus 3.x**
- **PostgreSQL 15**
- **Hibernate ORM with Panache**

### Frontend
- **Angular 20**
- **PrimeNG**

### Monitoring
- **Prometheus** (metrics collection)
- **Grafana** (visualization & dashboards)
- **Micrometer** (metrics instrumentation)

### Testing
- **JUnit 5**
- **Testcontainers**
- **Robot Framework + Selenium**

### Infrastructure
- **Docker & Docker Compose**
- **Kubernetes**
- **GitHub Actions**

## 📋 Prerequisites

- **Docker** & **Docker Compose**
- **Java 25**
- **Node.js 20+** & **npm**
- **Git**
- **Minikube**

## 🏃 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/office-orbit.git
cd office-orbit
```

### 2. Setup environment variables
```bash
cp .env.example .env
# Edit .env with your local settings (optional, defaults work fine)
```

### 3. Start infrastructure (PostgreSQL, Prometheus, Grafana)
```bash
docker-compose up -d
```

### 4. Verify services are running
- **Grafana:** http://localhost:3000
- **Prometheus:** http://localhost:9090
- **PostgreSQL:** localhost:5432

### 5. Run Quarkus backend (Dev Mode)
```bash
cd backend
./mvnw quarkus:dev
```
Backend will be available at: http://localhost:8080

### 6. Run Angular frontend
```bash
cd frontend
npm install
npm start
```
Frontend will be available at: http://localhost:4200

## 📊 Monitoring

### Access Grafana
1. Open http://localhost:3000
2. Login: `admin` / `admin`
3. Add Prometheus datasource:
    - URL: `http://prometheus:9090`
    - Click "Save & Test"

### View Metrics
- **Prometheus UI:** http://localhost:9090/graph
- **Quarkus Metrics:** http://localhost:8080/q/metrics
- **PostgreSQL Metrics:** http://localhost:9187/metrics

## 🧪 Testing

### Backend Unit Tests
```bash
cd backend
./mvnw test
```

### Backend Integration Tests
```bash
./mvnw verify
```

### Frontend Tests
```bash
cd frontend
npm test
```

### E2E Tests (Robot Framework)
```bash
# TODO: To Be Defined
```

## 🏗️ Project Structure
```
office-orbit/
├── office-orbit-core/       # Quarkus backend
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/        # Application code
│   │   │   └── resources/   # Configuration files
│   │   └── test/            # Tests
│   └── pom.xml
├── office-orbit-ui/         # Angular frontend
│   ├── src/
│   │   ├── app/
│   │   └── assets/
│   └── package.json
├── k8s/                     # Kubernetes manifests
├── prometheus/              # Prometheus configuration
│   └── prometheus.yml
├── grafana/                 # Grafana provisioning (TODO)
├── .github/
│   └── workflows/           # CI/CD pipelines
├── docker-compose.yml       # Local development stack
├── .env.local               # Environment variables template
└── README.md
```

## 🎯 Features (Planned)

### For Employees
- [ ] Interactive office map
- [ ] Book/modify/cancel desk reservations
- [ ] View booking history
- [ ] Report office issues
- [ ] Request missing supplies

### For Managers
- [ ] All employee features
- [ ] Manage users (add/edit/delete)
- [ ] View and handle employee reports
- [ ] Read missing office supplies
- [ ] Assign repairs to external vendors

### For Admins
- [ ] Full user management with role assignments
- [ ] Application monitoring dashboard
- [ ] System health metrics
- [ ] Error logs and debugging tools

## 🔐 Security

- JWT-based authentication
- Role-based access control
- OIDC integration with Keycloak
- SQL injection prevention
- CORS configuration

## 📚 Learning Resources

This project is built for learning purposes. Key learning areas:

1. **Hexagonal Architecture** (Ports & Adapters)
2. **Domain-Driven Design** (DDD)
3. **Observability** (metrics, logs, traces)
4. **Containerization** (Docker, Kubernetes)
5. **CI/CD** automation
6. **Testing pyramid** (unit, integration, E2E)

## 📄 License

MIT License - see LICENSE file for details

---

**Note:** This is a learning project focusing on modern Java/Angular stack, clean architecture, and DevOps best practices.
