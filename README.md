# PyDust - Termux/Linux WPS Brute Force Tool
⚠️ **HANYA UNTUK TUJUAN PEMBELAJARAN/PENELITIAN ETIS** ⚠️  
Penulis tidak bertanggung jawab atas penyalahgunaan.

## Fitur
- Serangan brute force WPS
- Mode Pixie Dust attack
- Dukungan untuk daftar perangkat rentan
- Pemindaian jaringan Wi-Fi otomatis


## Important to **Install dependencies:**

```bash
pkg update && pkg upgrade -y
pkg install root-repo -y
pkg install git tsu python wpa-supplicant pixiewps iw openssl -y
termux-setup-storage
```

---

## ⚡ Instalasi Cepat (All-in-One Command)

```bash
apt update && apt upgrade -y && \
pkg install root-repo git tsu python wpa-supplicant pixiewps iw openssl -y && \
git clone --depth 1 https://github.com/risunCode/PyDust-OneShot && \
termux-setup-storage && \
sudo python PyDust-OneShot/pydust.py -i wlan0 -K
```

## 📁 Clone Tanpa Dependencies
```bash
git clone --depth 1 https://github.com/risunCode/PyDust-OneShot
```

---
## 🔄 Reinstall OneShot (Hapus & Clone Ulang)
```bash
rm -rf PyDust-OneShot
git clone https://github.com/risunCode/PyDust-OneShot.git
sudo python pydust.py -i wlan0 -d 5 -l -K
```

---

### ▶️ Running Script.

- **Pixie Dust (interface down):**
```bash
sudo python PyDust-OneShot/pydust.py -i wlan0 --iface-down -K
```

- **Pixie Dust Unlimited:**
```bash
sudo python PyDust-OneShot/pydust.py -i wlan0 -d 3 -l -K
```

- **Online Brute Force:**
```bash
sudo python PyDust-OneShot/pydust.py -i wlan0 -l -B
```

- **Push Button Connect (semua target):**
- contoh target
- -i wlan0 --push-button-connect -b 00:90:4C:C1:AC:21
```bash
sudo python PyDust-OneShot/pydust.py -i wlan0 -l --push-button-connect
```

 # Usage
```
 pydust.py <arguments>
 Required arguments:
     -i, --interface=<wlan0>  : Name of the interface to use

 Optional arguments:
     -b, --bssid=<mac>        : BSSID of the target AP
     -p, --pin=<wps pin>      : Use the specified pin (arbitrary string or 4/8 digit pin)
     -K, --pixie-dust         : Run Pixie Dust attack
     -B, --bruteforce         : Run online bruteforce attack
     --push-button-connect    : Run WPS push button connection

 Advanced arguments:
     -d, --delay=<n>          : Set the delay between pin attempts [0]
     -w, --write              : Write AP credentials to the file on success
     -F, --pixie-force        : Run Pixiewps with --force option (bruteforce full range)
     -X, --show-pixie-cmd     : Alway print Pixiewps command
     --vuln-list=<filename>   : Use custom file with vulnerable devices list ['vulnwsc.txt']
     --iface-down             : Down network interface when the work is finished
     -l, --loop               : Run in a loop
     -r, --reverse-scan       : Reverse order of networks in the list of networks. Useful on small displays
     --mtk-wifi               : Activate MediaTek Wi-Fi interface driver on startup and deactivate it on exit
                                (for internal Wi-Fi adapters implemented in MediaTek SoCs). Turn off Wi-Fi in the system settings before using this.
     -v, --verbose            : Verbose output
 ```

# Acknowledgements
## Special Thanks
* `rofl0r` for initial implementation;
* `Monohrom` for testing, help in catching bugs, some ideas;
* `Wiire` for developing Pixiewps;
* `drydryg` for his amazing work on `rofl0r` repo.
* mff aing cuman nempel nama hehe

#### Another good repo
-