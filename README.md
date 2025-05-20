# Tailscale for GitHub Codespaces  
*Run Tailscale VPN in GitHub Codespaces with persistent IPs – no sudo required. Simple setup, secure connections.*  

[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)  

## 🌟 Why Use This?  
- 🌐 **Same IP every time** – No more reconfiguring tools  
- 🔒 **Private networking** – Enjoy encrypted peer-to-peer connections of Tailscale 
- ⚡ **Easy Setup** – Ready in seconds!  
- 🚫 **No special permissions** – Works without `sudo`  

---

## 🚀 Get Started  

### 1. Install Tailscale  
```bash
curl -fsSL https://tailscale.com/install.sh | sh
```

### 2. Add Your Key
1. Get a key from [Tailscale Admin](https://login.tailscale.com/admin/authkeys)
2. Save it securely:
```bash
mkdir -p ~/.config/tailscale
echo "tskey-auth-XXXXXX" > ~/.config/tailscale/authkey
chmod 600 ~/.config/tailscale/authkey
```
*(Replace `tskey-auth-XXXXXX` with your actual key)*

### 3. Download Control Scripts
```bash
wget -O ~/start-tailscale https://raw.githubusercontent.com/itsMeRaj69/tailscale-codespaces/main/scripts/start-tailscale
wget -O ~/stop-tailscale https://raw.githubusercontent.com/itsMeRaj69/tailscale-codespaces/main/scripts/stop-tailscale
```
### 4. Make them executable
```bash
chmod +x ~/start-tailscale ~/stop-tailscale
```

---

## 🛠️ Usage  
| Command | What It Does |  
|---------|--------------|  
| `~/start-tailscale` | Connect to your VPN |  
| `~/stop-tailscale`  | Disconnect safely |  

---

## 🔐 Pro Tips  
- 🔑 Use **reusable keys** for convenience  
- 🗑️ **Revoke old keys** in [Tailscale Admin](https://login.tailscale.com/admin/authkeys)  

---

## ❓ Need Help?
```bash
# Reset everything (fresh start)
rm -rf ~/.config/tailscale/ /tmp/tailscale*
```


📜 *MIT Licensed | Not affiliated with Tailscale Inc.*  
