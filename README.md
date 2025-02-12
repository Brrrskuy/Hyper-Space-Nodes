# <h2 align=center>Hyper Space Nodes</h2>

- Buy VPS di : [t.me/skuycloud](t.me/skuycloud)
## Minimum Requirements

| **Requirement**         |
|-------------------------|
|  8GB RAM                |
|  4 cores                |


## Guide Install
1. Install Hyperspace Nodes
```
curl https://download.hyper.space/api/install | bash
```
2. Lanjut (tergantung posisi file dimana , klo default root pakai ini)
```
source /root/.bashrc
```
3. Buat file my.pem dan isi Priv.Keys ada digambar kunci, Paste didalam `nano my.pem` jika sudah `CTRL+S` + `CTRL+X` 
![image](https://github.com/user-attachments/assets/1b1fc174-0f82-47b1-a1da-ecb0d4eff684)
```
nano my.pem
```
4. Izinkan akses my.pem
```
chmod 600 my.pem
```
5. Buat screen 
```
screen -S Hypernodes
```
6. Jalankan script
```
aios-cli start
```
-Lalu kalau sudah pergi ke Home screen lagi `CTRL+A+D`

7. Tambahkan models default
```
aios-cli models add hf:TheBloke/phi-2-GGUF:phi-2.Q4_K_M.gguf
```
8. Run inference 
```
aios-cli infer --model hf:TheBloke/phi-2-GGUF:phi-2.Q4_K_M.gguf --prompt "Can you explain the concept of hyperspace and its applications in science fiction?"
```
9. Import PV.key 
```
aios-cli hive import-keys ./my.pem
```
10. Login ke hive
```
aios-cli hive login
```
11. Start Nodes
```
aios-cli hive connect
```
12. Pilih tier untuk spec VPSmu (Saya 8GB/4core tier 3-4) sesuaikan saja
```
aios-cli hive select-tier 3
```
![image](https://github.com/user-attachments/assets/5c4acd4a-b158-49d9-a567-d6e1c937df62)
13. Check Hyper Nodes Points
```
aios-cli hive points
```
14. Check your Pv.Keys & Pub.Keys
```
aios-cli hive whoami
```
15. Jika tidak ingin RUN lagi `STOP NODE` 
```
aios-cli kill
```
------------------
- Trakteer buat buy Kopi : https://trakteer.id/brrrskuy/tip
