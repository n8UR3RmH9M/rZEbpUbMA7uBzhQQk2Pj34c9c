## RustScan Faster NMAP Scanning

Find all open ports fast with RustScan.
For more details see [RustScan Project](https://github.com/RustScan/RustScan).

### Installation
For this guide we use to install it the docker image. You can, however install it with different options on the [Github Project](https://github.com/RustScan/RustScan). 

To install, we select the stable version of the docker image [rustscan:alpine](https://hub.docker.com/r/rustscan/rustscan).


```sh
curl https://sh.rustup.rs -sSf | sh && \
sudo apt update && \
sudo apt install -y docker.io && \
sudo systemctl enable docker --now && \
sudo usermod -aG docker $USER && \
docker && \
docker pull rustscan:alpine && \
echo "alias rscan='sudo docker run -it --rm --name rustscan rustscan:alpine'" >> /home/kali/.zshrc && \
source /home/kali/.zshrc
```