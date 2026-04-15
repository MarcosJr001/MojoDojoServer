# MojoDojoServer

# 🧊 Minecraft Cloud Server | GitHub Codespaces

<p align="center">
  <img src="https://img.shields.io/badge/Minecraft-1.20.1-green?style=for-the-badge&logo=minecraft" alt="Minecraft Version">
  <img src="https://img.shields.io/badge/Platform-Linux-orange?style=for-the-badge&logo=linux" alt="Platform">
  <img src="https://img.shields.io/badge/Status-Online-brightgreen?style=for-the-badge" alt="Status">
</p>

Este projeto utiliza a infraestrutura do **GitHub Codespaces** para hospedar um servidor de Minecraft de alta performance de forma gratuita, utilizando o painel **CraftControl** para gestão e **Playit.gg** para o túnel de conexão.

---

## 🚀 Tecnologias Utilizadas

* **Host:** GitHub Codespaces (4 vCPUs, 8GB RAM)
* **Gerenciamento:** [CraftControl](https://craftcontrol.com/)
* **Network Tunnel:** [Playit.gg](https://playit.gg/)
* **Engine:** Forge / Fabric (Foco em Mods como *Create* e *RPG*)

---

## 🛠️ Instalação e Setup

### 1. Inicialização do Ambiente
Crie um Codespace utilizando a máquina de **4 Cores** para garantir que o modpack (especialmente o *Create*) rode sem gargalos de CPU.

### 2. Comandos de Instalação (Terminal)
Execute os comandos abaixo para configurar as dependências de rede e o painel:

```bash
# Dependências e CraftControl
curl -sSL [https://raw.githubusercontent.com/CraftControl/CraftControl/master/install.sh](https://raw.githubusercontent.com/CraftControl/CraftControl/master/install.sh) | sudo bash
pip install distro

# Instalação do Túnel Playit.gg
curl -SsL [https://playit-cloud.github.io/ppa/key.gpg](https://playit-cloud.github.io/ppa/key.gpg) | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/playit.gpg > /dev/null
echo "deb [signed-by=/etc/apt/trusted.gpg.d/playit.gpg] [https://playit-cloud.github.io/ppa/data-stable](https://playit-cloud.github.io/ppa/data-stable) /" | sudo tee /etc/apt/sources.list.d/playit-cloud.list
sudo apt update && sudo apt install playit -y
