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

- [Massscan](https://github.com/robertdavidgraham/masscan)
```bash
sudo apt-get --assume-yes install git make gcc
git clone https://github.com/robertdavidgraham/masscan
cd masscan
make install
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

## Links

- [Certifacte Transparancy crt](https://crt.sh/)
- [Search Engine shodan](https://www.shodan.io/)
- [IP Information ipinfo](https://ipinfo.io/)
- [Redirect Checker wheregoes](https://wheregoes.com/)

- [Website Headers securityheaders](https://securityheaders.com/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
- [Redirect Checker wheregoes](https://wheregoes.com/)
## Quote
> You, me, or nobody is gonna hit as hard as life. But it ain't about how hard you hit. It's about how hard you can get hit and keep moving forward; how much you can take and keep moving forward. That's how winning is done! - Rocky Balboa
