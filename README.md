This repository is a collection of information of tools and commands for linux and penetration testing.

## Table of Contents

1. [Tools](#tools)
2. [Commands](#commands)
3. [Usefull URLs](#urls)
4. [Quote](#quote)

## Tools

- [TLSX](https://github.com/projectdiscovery/tlsx)
```bash
go install github.com/projectdiscovery/tlsx/cmd/tlsx@latest
```

- [Nuclei](https://github.com/projectdiscovery/nuclei)
```bash
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
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

## Quote
> You, me, or nobody is gonna hit as hard as life. But it ain't about how hard you hit. It's about how hard you can get hit and keep moving forward; how much you can take and keep moving forward. That's how winning is done! - Rocky Balboa
