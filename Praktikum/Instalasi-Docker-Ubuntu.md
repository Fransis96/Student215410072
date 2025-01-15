<h2>Instalasi dan persiapan </h2></br>  

> Dalam proses ini, kita akan menginstal beberapa library dan kebutuhan aplikasi. Diperlukan docker container dan docker compose.
- Lakukan update package dan repo pada ubuntu anda:
```bash
sudo apt update
```
- Selanjutnya lakukan penambahan library dan paket aplikasi https untuk kebutuhan container docker
```bash
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
- Kemudian tambahkan GPG key untuk proses instalasi official docker container
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
```
- Tambahkan docker repository pada repository ubuntu
```bash
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
- Update kembali repository ubuntu anda
```bash
sudo apt update
```  
 <br>  
 
<h2>Instalasi Docker Container dan docker compose</h2></br>

- Instalasi container docker dan docker compose pada mesin virtual compute anda. Perintah instalasi docker:
```bash
sudo apt install docker-ce
```
- Kemudian install docker compose sebagai orchestration tools. gunakan perintah berikut:  
```bash
sudo apt install docker-compose
```
- cek status docker anda dengan perintah:
```bash
sudo systemctl status docker
```
- Selanjutnya, kita coba cek hasil instalasi docker-compose. 
```bash
sudo docker-compose --version
```

</br>

### Menggunakan perintah docker tanpa menyertakan ``sudo`` di ubuntu 
> Opsional
```bash
sudo usermod -aG docker $USER
```
```bash
newgrp docker
```
