# <h2 align=center>Hyper Space Nodes AI</h2>
- Buy VPS di : [t.me/skuycloud](t.me/skuycloud)
- Trakteer buat buy Kopi : https://trakteer.id/brrrskuy/tip `<---`

## Minimum Requirements

| **Requirement**         |
|-------------------------|
|  8GB RAM                |
|  4 cores                |


## Guide Install
1. Install Hyperspace Nodes AI
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
6. Jalankan script, Setelah Selesai pergi ke Home screen lagi `CTRL+A+D`
    ```
    aios-cli start
    ```
7. Tambahkan models default

   `Buat Screen baruu lagiii`
    ```
    screen -S inference
    ```
    Lanjut
    ```
    aios-cli models add hf:TheBloke/Mistral-7B-Instruct-v0.1-GGUF:mistral-7b-instruct-v0.1.Q4_K_S.gguf
    ```
9. Run inference 
    ```
    aios-cli infer --model hf:TheBloke/Mistral-7B-Instruct-v0.1-GGUF:mistral-7b-instruct-v0.1.Q4_K_S.gguf --prompt "Can you explain how to write an HTTP server in Rust?"
    ```
10. Import PV.key 
    ```
    aios-cli hive import-keys ./my.pem
    ```
11. Login ke hive
    ```
    aios-cli hive login
    ```
12. Start Nodes
    ```
    aios-cli hive connect
    ```
13. Pilih tier untuk spec VPSmu (Saya 8GB/4core tier 3-5) sesuaikan saja
    ```
    aios-cli hive select-tier 3
    ```
    - Setelah sudah selesai tinggal saja Detached screen `CTRL+A+D`
    
  ![image](https://github.com/user-attachments/assets/5c4acd4a-b158-49d9-a567-d6e1c937df62)

14. Run an inference through

    Buat Screen baru lagii
    ```
    screen -S inference
    ```
    ```
    aios-cli hive infer --model hf:TheBloke/Mistral-7B-Instruct-v0.1-GGUF:mistral-7b-instruct-v0.1.Q4_K_S.gguf --prompt "Can you explain how to write an HTTP server in Rust?"
    ```
    Setelah sudah selesai tinggal saja Detached screen `CTRL+A+D`
16. Check Hyper Nodes AI Points
    ```
    aios-cli hive points
    ```
17. Check your Pv.Keys & Pub.Keys
    ```
    aios-cli hive whoami
    ```
18. Jika tidak ingin RUN lagi `STOP NODE` 
    ```
    aios-cli kill
    ```
