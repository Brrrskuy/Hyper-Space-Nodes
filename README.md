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
2. Lanjut 
```
source /root/.bashrc
```
3. Buat file my.pem dan isi Privatekeys ada di gambar kunci, Paste di dalam `nano my.pem` jika sudah `CTRL+S` + `CTRL+X` 
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

7. Check ketersediaan models , bisa menggunakan models default / bawaan
```
aios-cli models available
```
8. Tambahkan models default
```
aios-cli models add hf:TheBloke/phi-2-GGUF:phi-2.Q4_K_M.gguf
```
9. Buat screen baru lagi
```
screen -S Hyper
```
10. Run inference ini didalam screen 
```
aios-cli infer --model hf:TheBloke/phi-2-GGUF:phi-2.Q4_K_M.gguf --prompt "Can you explain the concept of hyperspace and its applications in science fiction?"
```
-Jika sudah nanti pergi ke home screen lagi `CTRL+A+D`

11. Import PV.key dan Login
```
aios-cli hive import-keys ./my.pem
```
12. Login ke hive
```
aios-cli hive login
```
13. Pilih tier untuk spec VPSmu (Saya 8GB/4core tier 3-4) 
```
aios-cli hive select-tier 3
```
14. Check Hyper Nodes Point
```
aios-cli hive points
```
15. Check your Pv.Keys & Pub.Keys
```
aios-cli hive whoami
```
16. Jika tidak ingin RUN lagi Stop Node 
```
aios-cli kill
```
------------------
- Trakteer buat buy Kopi : https://trakteer.id/brrrskuy/tip
