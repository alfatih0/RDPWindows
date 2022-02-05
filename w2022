#! /bin/bash
# Make Instance Ready for Remote Desktop or RDP
apt-get update
rm -rf w2022 w2022.img w2022.gz ngrok ngrok.zip ng.sh > /dev/null 2>&1
echo "Download windows files"
wget -O w2022.gz https://go.aank.me/win/windows2022.gz
gunzip w2022.gz
echo "Proses..."
echo "ditunggu.."
mv w2022 w2022.img
wget -O ng.sh https://raw.githubusercontent.com/alfatih0/RDPWindows/main/ngrok.sh > /dev/null 2>&1
chmod +x ng.sh
./ng.sh
clear
echo "==========================="
echo Pilih Wilayah dengan kode dibawah
echo "==========================="
echo "us - United States (Ohio)"
echo "eu - Europe (Frankfurt)"
echo "ap - Asia/Pacific (Singapore)"
echo "au - Australia (Sydney)"
echo "sa - South America (Sao Paulo)"
echo "jp - Japan (Tokyo)"
echo "in - India (Mumbai)"
read -p "choose ngrok region: " CRP
./ngrok tcp --region $CRP 3388 &>/dev/null &
clear
echo Download File
apt-get install qemu-system-x86 -y
echo "proses..."
echo "Starting Windows"
qemu-system-x86_64 -hda w2022.img -m 8G -smp cores=4 -net user,hostfwd=tcp::3388-:3389 -net nic -object rng-random,id=rng0,filename=/dev/urandom -device virtio-rng-pci,rng=rng0 -vga vmware -nographic &>/dev/null &
clear
echo RDP Address:
curl --silent --show-error http://127.0.0.1:4040/api/tunnels | sed -nE 's/.*public_url":"tcp:..([^"]*).*/\1/p'
echo "===================================="
echo "Username: Administrator"
echo "Password: Lingg@H0sting"
echo "===================================="
echo "===================================="
echo "Don't closse this Tab"
echo "bagi yang mau bacot bareng"
echo "Dan berbagi"
echo "Silahkan ke grub -> https://t.me/uplah123"
echo "jangan jualan dan jangan pelit"
echo "===================================="
b='\033[1m'
r='\E[31m'
g='\E[32m'
c='\E[36m'
endc='\E[0m'
enda='\033[0m'
# Branding

printf """$c$b
                                                                       
                                                                      
$$\   $$\  $$$$$$\         $$$$$$$\  $$$$$$\   $$$$$$\  $$\  $$\  $$\ 
$$ |  $$ |$$  __$$\       $$  _____|$$  __$$\ $$  __$$\ $$ | $$ | $$ |
$$ |  $$ |$$ /  $$ |      $$ /      $$ |  \__|$$$$$$$$ |$$ | $$ | $$ |
$$ |  $$ |$$ |  $$ |      $$ |      $$ |      $$   ____|$$ | $$ | $$ |
\$$$$$$  |$$$$$$$  |      \$$$$$$$\ $$ |      \$$$$$$$\ \$$$$$\$$$$  |
 \______/ $$  ____/        \_______|\__|       \_______| \_____\____/ 
          $$ |                                                        
          $$ |                                                        
          \__|                                                        
          
$endc$enda""";
sleep 43200
