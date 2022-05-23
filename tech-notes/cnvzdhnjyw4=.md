## Find all open ports fast with RustScan

For this guide we will install using a docker image. However you can install with different options check the [Github Project](https://github.com/RustScan/RustScan).

To install using docker image as of writing the latest version is  [rustscan:2.0.0](https://hub.docker.com/r/rustscan/rustscan).

```sh
sudo apt update && \
sudo apt install -y docker.io
sudo systemctl enable docker --now
sudo usermod -aG docker ${USER}
docker

# reboot the system

docker pull rustscan/rustscan:2.0.0 && \
docker images && \
echo "alias rscan='sudo docker run -it --rm --name rustscan rustscan/rustscan:2.0.0'" >> /home/${USER}/.zshrc && \
source /home/${USER}/.zshrc
```

Open the command `rscan --help` or `rustscan --help` to view options and details.

```sh
# scanning target machine
rscan 192.168.1.100 -b 500 -t 1024
```

For more details see [RustScan Project](https://github.com/RustScan/RustScan).
