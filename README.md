This repository is a collection of information of tools and commands for linux and penetration testing.

## Table of Contents

1. [Tools](#tools)
2. [Commands](#commands)
3. [Links](#links)
4. [Quote](#quote)

## Tools

- [TLSx](https://github.com/projectdiscovery/tlsx)
```bash
go install github.com/projectdiscovery/tlsx/cmd/tlsx@latest
```

- [Nuclei](https://github.com/projectdiscovery/nuclei)
```bash
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
```

- [HTTPx](https://github.com/projectdiscovery/httpx)
```bash
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
```

- [Subzy](https://github.com/PentestPad/subzy)
```bash
go install -v github.com/PentestPad/subzy@latest
```

- [Subzy](https://github.com/projectdiscovery/subfinder)
```bash
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
```

- [Naabu](https://github.com/projectdiscovery/naabu)
```bash
go install -v github.com/projectdiscovery/naabu/v2/cmd/naabu@latest
```

- [DNSx](https://github.com/projectdiscovery/dnsx)
```bash
go install -v github.com/projectdiscovery/dnsx/cmd/dnsx@latest
```

- [FFUF](https://github.com/ffuf/ffuf)
```bash
go install github.com/ffuf/ffuf/v2@latest
```

- [WAFW00F](https://github.com/EnableSecurity/wafw00f)
```bash
go install github.com/ffuf/ffuf/v2@latest
```

- [URLFinder](https://github.com/projectdiscovery/urlfinder)
```bash
go install -v github.com/projectdiscovery/urlfinder/cmd/urlfinder@latest
```

- [Massscan](https://github.com/robertdavidgraham/masscan)
```bash
sudo apt-get --assume-yes install git make gcc
git clone https://github.com/robertdavidgraham/masscan
cd masscan
make install
```

- [theHarvester](https://github.com/laramies/theHarvester/wiki/Installation)
```bash
git clone https://github.com/laramies/theHarvester
cd theHarvester
python3 -m pip install -r requirements/base.txt
python3 theHarvester.py -h
```
## Commands

- Install docker (Ubuntu)
```bash
apt update -y
apt upgrade -y
apt install apt-transport-https ca-certificates curl software-properties-common -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
apt update -y
apt install docker-ce -y
```

- Install golang
```bash
goversion="1.23.4"
wget "https://go.dev/dl/go$goversion.linux-amd64.tar.gz"
rm -rf /usr/local/go && tar -C /usr/local -xzf "go$goversion.linux-amd64.tar.gz"
export PATH=$PATH:/usr/local/go/bin
go version
```

- Create Custom Ubuntu 22.04 Image
```bash
apt install p7zip wget xorisso -y
mkdir ubuntu2204
cd ubuntu2204
mkdir source-files
wget https://cdimage.ubuntu.com/ubuntu-server/jammy/daily-live/current/jammy-live-server-amd64.iso
7z -y x jammy-live-server-amd64.iso -osource-files
mv  '[BOOT]' ../BOOT
nano source-files/boot/grub/grub.cfg 
menuentry "Autoinstall Ubuntu Server" {
    set gfxpayload=keep
    linux   /casper/vmlinuz quiet autoinstall ds=nocloud\;s=/cdrom/server/  ---
    initrd  /casper/initrd
}
mkdir source-files/server
touch source-files/server/meta-data
touch source-files/server/user-data
nano source-files/server/user-data
cd source-files
xorriso -as mkisofs -r \
  -V 'Ubuntu 22.04 CUSTOM (EFIBIOS)' \
  -o ../ubuntu-22.04-autoinstall.iso \
  --grub2-mbr ../BOOT/1-Boot-NoEmul.img \
  -partition_offset 16 \
  --mbr-force-bootable \
  -append_partition 2 28732ac11ff8d211ba4b00a0c93ec93b ../BOOT/2-Boot-NoEmul.img \
  -appended_part_as_gpt \
  -iso_mbr_part_type a2a0d0ebe5b9334487c068b6b72699c7 \
  -c '/boot.catalog' \
  -b '/boot/grub/i386-pc/eltorito.img' \
    -no-emul-boot -boot-load-size 4 -boot-info-table --grub2-boot-info \
  -eltorito-alt-boot \
  -e '--interval:appended_partition_2:::' \
  -no-emul-boot \
  .
```
## Links

- [Certifacte Transparancy crt](https://crt.sh/)
- [Search Engine shodan](https://www.shodan.io/)
- [IP Information ipinfo](https://ipinfo.io/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
- [Website Headers securityheaders](https://securityheaders.com/)
- [Google Dorking](https://gist.github.com/sundowndev/283efaddbcf896ab405488330d1bbc06)
- [WebCheck](https://web-check.xyz/)
- [DNS Checker BGP](https://bgp.tools/)

## Quote
> You, me, or nobody is gonna hit as hard as life. But it ain't about how hard you hit. It's about how hard you can get hit and keep moving forward; how much you can take and keep moving forward. That's how winning is done! - Rocky Balboa
