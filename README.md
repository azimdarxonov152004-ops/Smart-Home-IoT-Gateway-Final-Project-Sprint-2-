# Smart Home IoT Gateway – Final Project (Sprint 2)

**Course:** Linux Embedded Systems Topics and Projects  
**Student:** [Ismingiz Familangiz]  
**Date:** December 2025

## Project Overview
Smart home gateway based on Raspberry Pi that:
- Collects temperature/humidity data from sensor
- Publishes to MQTT broker (with TLS)
- Receives commands from dashboard
- Supports secure OTA updates
- Uses OverlayFS for update safety

## Features Implemented (Sprint 2)
- [x] Secure MQTT with TLS client certificates
- [x] OTA update system (A/B style with OverlayFS)
- [x] Digital signature verification of update packages (RSA-2048)
- [x] Web dashboard (Node-RED or simple HTML)
- [x] Power-fail-safe update mechanism
- [x] All code in Git with proper commits

## Hardware
- Raspberry Pi 4 (or 3B+)
- /final-project/
├── ota-update/          # OTA scripts & signer
├── mqtt-client/         # MQTT publisher/subscriber
├── web-dashboard/       # Node-RED flow or HTML
├── overlay-rootfs/      # OverlayFS setup
├── keys/                # Private/public keys (public only in repo!)
└── README.md

## Demo Video (2-4 minutes)
https://youtu.be/xxxxxxx  ← YouTube link (unlisted yoki public)

## How to Run
```bash
# 1. Clone repo
git clone https://github.com/username/smart-home-gateway.git
cd smart-home-gateway

# 2. MQTT + TLS
cd mqtt-client
python3 mqtt_publisher.py

# 3. Start OTA update test
cd ../ota-update
./apply_update.sh updates/firmware_v2.signed
- DHT22 temperature/humidity sensor (or any sensor you used)

## Directory Structure
