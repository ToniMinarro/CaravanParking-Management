## 🚀 Environment Setup

### 🐳 Needed tools

1. [Install Docker](https://www.docker.com/get-started)
2. Clone this project: `git clone https://github.com/ToniMinarro/CaravanParking-Management.git`
3. Move to the project folder: `cd CaravanParking-Management`

### 🛠️ Environment configuration

1. Create a local environment file (`cp .env .env.local`) if you want to modify any parameter

### 🔥 Application execution

1. Install all the dependencies and bring up the project with Docker executing: `make build`
2. Then you'll have 2 apps available (1 API and 1 Frontend):
   1. [CaravanParkingManagement Backend](apps/caravan_management/backend): http://localhost:8030/health-check
   2. [CaravanParkingManagement Frontend](apps/caravan_management/frontend): http://localhost:8031/health-check

### ✅ Tests execution

1. Install the dependencies if you haven't done it previously: `make deps`
2. Execute PHPUnit and Behat tests: `make test`

## 👩‍💻 Project explanation

Simple application to manage IN/OUT in a caravans parking area.

### ⛱️ Bounded Contexts

* [Caravan Parking Management](src/CaravanManagement).

### 🎯 Hexagonal Architecture

This repository follows the Hexagonal Architecture pattern. Also, it's structured using `modules`.

## 📱 Monitoring
Every time a domain event is published it's exported to Prometheus. You can access to the Prometheus panel [here](http://localhost:9999/).

