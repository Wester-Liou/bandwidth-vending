# Bandwidth Vending

Turn your unused internet bandwidth into passive income. This project sets up multiple bandwidth sharing applications using Docker, complete with container monitoring and metrics collection.

[中文版 README (Traditional Chinese)](README.zh-TW.md)

## 💰 Start Earning (Referral Links)

Sign up using the links below to get a head start (and support this project):

- **Bitping**: [Join Bitping](https://app.bitping.com/)
- **Honeygain**: [Join Honeygain](https://join.honeygain.com/EFG20FAEB3)
- **PacketStream**: [Join PacketStream](https://packetstream.io/?psr=7r2e)
- **Pawns.app**: [Join Pawns.app](https://pawns.app/?r=18988103)
- **TraffMonetizer**: [Join TraffMonetizer](https://traffmonetizer.com/?aff=2099471)

## 🚀 Included Services

### Bandwidth Sharing

- **Bitping**: Decentralized network monitoring and data relay.
- **Honeygain**: Share internet bandwidth for data intelligence.
- **PacketStream**: Peer-to-peer residential proxy network.
- **Pawns.app (formerly IPRoyal Pawns)**: Share internet for surveys and other tasks.
- **TraffMonetizer**: Monetize your traffic.

### Infrastructure

- **Watchtower**: Automatically updates running Docker containers every hour.
- **cAdvisor**: Provides real-time container resource usage and performance metrics.
- **Prometheus**: Collects and stores container metrics from cAdvisor.

## 📋 Prerequisites

- [Docker](https://docs.docker.com/get-docker/) installed.
- [Docker Compose](https://docs.docker.com/compose/install/) installed (usually included with Docker Desktop/Plugin).

## 🛠️ Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Wester-Liou/bandwidth-vending.git
   cd bandwidth-vending
   ```

2. **Configure Environment Variables**:
   Copy the example environment file:

   ```bash
   cp .env.example .env
   ```

3. **Edit `.env`**:
   Open `.env` and fill in your credentials (email, password, tokens) for each service.

   ```ini
   # Device Name (appears in dashboards)
   DEVICE_NAME=bandwidth-vending

   # Bitping
   BITPING_EMAIL=your_email@example.com
   BITPING_PASSWORD=your_password

   # Honeygain
   HONEYGAIN_EMAIL=your_email@example.com
   HONEYGAIN_PASSWORD=your_password

   # PacketStream
   PS_CLIENT_CID=your_cid

   # Pawns.app
   PAWNS_EMAIL=your_email@example.com
   PAWNS_PASSWORD=your_password

   # TraffMonetizer
   TRAFFMONETIZER_TOKEN=your_token
   ```

## ▶️ Usage

### Start Services

Run the containers in the background:

```bash
docker compose up -d
```

### View Logs

Check the status of your containers:

```bash
docker compose logs -f
```

### Stop Services

Stop and remove containers:

```bash
docker compose down
```

## 📊 Monitoring

This setup includes a built-in monitoring stack:

- **cAdvisor** — accessible at `http://localhost:8080` (bound to localhost only)
- **Prometheus** — accessible at `http://localhost:9090` (bound to localhost only)

Prometheus scrapes container metrics from cAdvisor automatically. You can use this data to monitor CPU, memory, network, and disk usage per container.

## ⚙️ Configuration Details

See `.env.example` for all configurable options. Make sure to keep your credentials secure and never commit your actual `.env` file to version control (it is ignored by default via `.gitignore`).

## 🔄 Updates

This setup includes **Watchtower**, which will automatically check for and update your bandwidth sharing containers to the latest images every hour. It also revives stopped containers and cleans up old images.
