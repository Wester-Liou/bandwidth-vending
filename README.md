# Traffic Vending

Turn your unused internet bandwidth into passive income. This project sets up multiple bandwidth sharing applications (Honeygain, PacketStream, Pawns.app, TraffMonetizer) using Docker.

[中文版 README (Traditional Chinese)](README.zh-TW.md)

## 💰 Start Earning (Referral Links)

Sign up using the links below to get a head start (and support this project):

- **Honeygain**: [Join Honeygain](https://join.honeygain.com/EFG20FAEB3)
- **PacketStream**: [Join PacketStream](https://packetstream.io/?psr=7r2e)
- **Pawns.app**: [Join Pawns.app](https://pawns.app/?r=18988103)
- **TraffMonetizer**: [Join TraffMonetizer](https://traffmonetizer.com/?aff=2099471)

## 🚀 Included Services

- **Honeygain**: Share internet bandwidth for data intelligence.
- **PacketStream**: Peer-to-peer residential proxy network.
- **Pawns.app (formerly IPRoyal Pawns)**: Share internet for surveys and other tasks.
- **TraffMonetizer**: Monetize your traffic.
- **Watchtower**: Automatically updates running Docker containers.

## 📋 Prerequisites

- [Docker](https://docs.docker.com/get-docker/) installed.
- [Docker Compose](https://docs.docker.com/compose/install/) installed (usually included with Docker Desktop/Plugin).

## 🛠️ Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/traffic-vending.git
   cd traffic-vending
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
   DEVICE_NAME=traffic-vending

   # Honeygain
   HONEYGAIN_EMAIL=your_email@example.com
   HONEYGAIN_PASSWORD=your_password

   # PacketStream
   PS_CLIENT_CID=your_cid

   # Pawns.app
   PAWS_EMAIL=your_email@example.com
   PAWS_PASSWORD=your_password

   # TraffMonetizer
   TRAFFMONETIZER_TOKEN=your_token
   ```

## ▶️ Usage

### Start Services

Run the containers in the background:

```bash
docker-compose up -d
```

### View Logs

Check the status of your containers:

```bash
docker-compose logs -f
```

### Stop Services

Stop and remove containers:

```bash
docker-compose down
```

## ⚙️ Configuration Details

See `.env` for all configurable options. Make sure to keep your credentials secure and never commit your actual `.env` file to version control (it is ignored by default).

## 🔄 Updates

This setup includes **Watchtower**, which will automatically check for and update your containers to the latest images every hour.
