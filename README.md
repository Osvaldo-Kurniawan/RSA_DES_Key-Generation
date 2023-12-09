# RSA_DES_Key-Generation

Untuk menjalankan simulasi komunikasi saya menggunakan GNS3 dengan menginstall g++. Pada project GNS3 saya membuat topologi sebagai berikut :

<img width="1002" alt="image" src="https://github.com/Osvaldo-Kurniawan/RSA_DES_Key-Generation/assets/108170210/cf11ba88-17c0-4094-8bf6-1049b8ad4c80">

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
