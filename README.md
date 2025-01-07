# Running Titan Node on Galileo Testnet

Welcome to the **Titan Node** deployment tutorial for the **Galileo Testnet**. This guide will help you set up and run a Titan node on the testnet, both manually and via an auto-installation script.

## Galileo Testnet

The **Galileo Testnet** is live! Connect to the testnet using the following details:

- **Testnet URL**: [test4.titannet.io](http://test4.titannet.io)

## Minimum Hardware Requirements

Ensure your machine meets the following minimum requirements for smooth operation:

- **CPU**: 2 cores (2c VPU)
- **RAM**: 2 GB
- **Storage**: 50 GB SSD or higher
- **Upload Speed**: 10 Mbps or higher
- **NAT**: Supported (for proper connectivity)

---

## Installation Guide

### Option 1: Manual Installation

Follow these steps to install the Titan Node manually:

#### 1. Install Snap

First, ensure that `snapd` is installed and enabled on your system:

```bash
sudo apt update
sudo apt install snapd
```
Enable Snap:
```bash
sudo systemctl enable --now snapd.socket
```
2. Install Multipass
Next, install Multipass, which is needed for the Titan Node:
```bash
sudo snap install multipass
```
3. Verify Installation
To verify that Multipass has been installed successfully:
```bash
multipass --version
```
4. Download and Extract the Titan Node Installation Package
Download the installation package and extract it to the /opt/titanagent directory:
```bash
# Download installation package
wget https://pcdn.titannet.io/test4/bin/agent-linux.zip

# Create installation directory
mkdir -p /opt/titanagent

# Extract installation package
unzip agent-linux.zip -d /opt/titanagent
```
5. Get Your Key
Open your browser and visit the Galileo Testnet link.
Log in to your Titan account.
Find and copy your Titan Node Key.
6. Run the Titan Node
Navigate to the directory where the Titan agent was extracted:
```bash
cd /opt/titanagent
```
6. Create Screen
```bash
screen -S titan_agent
```
7. Run the Titan Node agent with your key and working directory:
```bash
./agent --working-dir=<your-titan-agent-folder-path> --server-url=https://test4-api.titannet.io --key=<your-key>
```
Replace <your-titan-agent-folder-path> with the actual folder path for Titan agent data.
Replace <your-key> with the key you copied earlier.

Option 2: Auto Installation (One-click Script)
To install the Titan node automatically with a single command, use the following script:
```bash
wget https://raw.githubusercontent.com/choir94/Airdropguide/refs/heads/main/Titan_node.sh && chmod +x Titan_node.sh && ./Titan_node.sh
```

Additional Resources:
https://titannet.gitbook.io/titan-network-en/galileo-testnet/node-participation-guide/run-titan-agent-on-linux

## Support Airdrop Node

For more updates and discussions, join the [Telegram Airdrop Node](https://t.me/airdrop_node).

Traktir Admin Buat kopi
[Traktir Kopi ](https://trakteer.id/AirdropNode/tip).

