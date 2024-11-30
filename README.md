# WORSKHOP-EwilTwin
WORKSHOP du BGI présenté par Samuel NUEZ et Benjamin WAGNER le 30 Novembre 2024

## Installation du pilote RTL8188EU pour Linux

## Prérequis

Avant de commencer, assurez-vous que votre système dispose des outils suivants :

- `git`
- `make`
- `gcc`
  
### Installation des outils requis (Debian/Ubuntu)

```bash
sudo apt update
sudo apt install -y git build-essential linux-headers-$(uname -r)
git clone https://github.com/aircrack-ng/rtl8188eus.git
cd rtl8188eus
echo "blacklist rtl8xxxu" | sudo tee /etc/modprobe.d/blacklist-rtl8xxxu.conf
sudo modprobe -r rtl8xxxu
make
sudo make install
sudo modprobe 8188eu
```
