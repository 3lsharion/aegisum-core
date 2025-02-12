Building Aegisum
================

## Table of Contents
- [Windows Installation](#windows-installation-)
- [Linux Installation](#linux-installation-)
- [Troubleshooting](#troubleshooting-)

## Windows Installation 🪟

**Warning:** Windows may flag the software as a virus. This is a false positive. You can verify its safety using the VirusTotal link below:

[View VirusTotal Scan](https://www.virustotal.com/gui/file/0fd44e69c136e943e7a1d65f0dd7e9a9e9d3a4abb43194f02e248b6ecf18356e)

### Steps:
1. **Download & Extract**
   - Download the latest [Windows Release](https://github.com/Aegisum/aegisum-core/releases): **windows-aegisum-core.zip**
   - Extract the ZIP file using WinRAR, 7-Zip, or the built-in Windows extractor.

2. **Install Aegisum Core**
   - Run `aegisum-qt.exe`
   - Follow the on-screen installation instructions.

3. **Initial Setup**
   - The first launch may take a few minutes as the blockchain syncs.
   - Create your wallet and back up your wallet.dat file in a secure location.

## Linux Installation 🐧

### 1. Update Your System
Run the following command to update and upgrade your Ubuntu server:
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

### 2. Download the Aegisum Core
```bash
wget --content-disposition -O linux-aegisum-v1.0.tar.gz https://github.com/Aegisum/aegisum-core/releases/download/v1.0/linux-aegisum-v1.0.tar.gz
```

### 3. Extract the Files
```bash
tar -czvf linux-aegisum-v1.0.tar.gz
```

### 4. Install Aegisum Core
```bash
sudo mv aegisumd aegisum-cli aegisum-tx /usr/bin/
```

### 5. Create the Data Directory
```bash
mkdir $HOME/.aegisum
```

### 6. Start Aegisum Core
```bash
aegisumd
```

The daemon will start syncing the blockchain. You can check the progress using:
```bash
aegisum-cli getblockcount
```

## Troubleshooting ⚙️
- If the daemon does not start, check for missing dependencies using:
  ```bash
  ldd aegisumd
  ```
- Ensure your firewall allows connections on port **22276** for P2P and **22275** for RPC.

## Need Help? 💬
Join the **[Aegisum Community](https://discord.gg/4E5caDKkeP)** for support and discussions!


See doc/build-*.md for instructions on building the various
elements of the Aegisum Core reference implementation of Aegisum.
