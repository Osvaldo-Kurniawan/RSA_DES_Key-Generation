# RSA_DES_Key-Generation

Untuk menjalankan simulasi komunikasi saya menggunakan GNS3 dengan menginstall g++. Pada project GNS3 saya membuat topologi sebagai berikut :

<img width="561" alt="image" src="https://github.com/Osvaldo-Kurniawan/Enc_Dcy_Keamanan-Informasi/assets/108170210/425354a2-fa02-4773-bc97-71f1819bd60c">

Dengan catatan ip sebagai berikut :
- ubuntu 1-3 (192.185.1.0) sebagai router penghubung client ke internet (NAT1)
- ubuntu 1-2 (192.185.1.2) sebagai client (membuat random key, menerima input user kemudian melakukan encrypt dan mengirim ke server)
- ubuntu 1-1 (192.185.1.1) sebagai server (melakukan decrypt key, menerima pesan client dan melakukan decrypty kemudian menampilkannya)

Adapun fungsi masing masing device :
1. Kedua device membuat socket untuk berkomunikasi
2. Klien membuat sebuah random key pada array integer (ASCII code).
3. Lakukan enkripsi Key DES, setelah terenkripsi dikirim dari klien ke server.
4. Server mendekripsi key DES yang diterima menggunakan private key.
5. Key DES yang telah didekripsi ditampilkan dalam format ASCII.
6. Server juga mencetak key DES terenkripsi asli dan key yang telah didekripsi sebagai string.
7. Key yang didapat dari hasil sharing menggunakan RSA algorithm digunakan untuk proses DES.
8. Client menerima input dan melakukan DES menggunakan key yang dibuat sebelumnya kemudian mengirim ke server.
9. Server menerima pesan terenkripsi kemudian melakukan decrypt dari key hasil decrypt RSA.
10. Close connection.
