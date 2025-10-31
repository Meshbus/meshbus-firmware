# Meshbus Firmware

This repository contains the firmware for the Meshbus project, which is designed to facilitate communication between various IoT devices using a mesh networking protocol.

## Quick Start

To get started with the Meshbus firmware, follow these steps:

1. **Clone the Repository**:

```bash
# Clone the repository
git clone https://github.com/meshbus/meshbus-firmware.git
```

2. **Set Up the Development Environment**:

```bash
# Navigate to the project directory
cd meshbus-firmware

# Initialize virtual environment
python3 -m venv ./.venv
source ./.venv/bin/activate

# Install West
pip install west

# Initialize Zephyr Project
west update

# Install Zephyr Python packages
west packages pip --install

# Install Zephyr SDK locally
west sdk install --install-base ./.sdk

# Fetch Zephyr modules and blobs
west blobs fetch
```

3. **Build the Firmware**:

```bash
# Navigate to the application directory
cd app

# Build for QEMU Cortex-M3 or your target board
west build -b qemu_cortex_m3
```
