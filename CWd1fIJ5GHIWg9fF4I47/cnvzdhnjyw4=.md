## RustScan Faster NMAP Scanning

Find all open ports fast with RustScan.
For more details see [RustScan Project](https://github.com/RustScan/RustScan).

### Installation
For this guide, we will install using a docker image. You can, however, install with different options on the [Github Project](https://github.com/RustScan/RustScan).

To install, using docker image as of writing the latest version is  [rustscan:2.0.0](https://hub.docker.com/r/rustscan/rustscan).


```sh
sudo apt update && \
sudo apt install -y docker.io && \
sudo systemctl enable docker --now && \
sudo usermod -aG docker $USER && \
docker && \
docker pull rustscan/rustscan:2.0.0 && \
docker images && \
echo "alias rscan='sudo docker run -it --rm --name rustscan rustscan/rustscan:2.0.0'" >> /home/kali/.zshrc && \
source /home/kali/.zshrc
```

Open the command rscan or rustscan --help to view options and details.

```sh
rscan --help

# scanning target mahcine
rscan 192.168.1.100 -b 500 -t 1024
```