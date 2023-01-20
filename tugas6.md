Task : Web Server & Load Balancing

1. Definisi Web Server

Aplikasi yang menerima request HTTP/S dari client dan memberikan layanan berupa data sebagai responsnya.

2. Jalankan 2 VM (Optional)
  - VM 1 = appserver
  - VM 2 = nginx

3. VM1 :
  - jalankan aplikasi dumbflix-frontend
  
   ![image](https://user-images.githubusercontent.com/45737074/213403207-782936a6-80da-4e61-b448-ccfd2601ba61.png)
   
   ![image](https://user-images.githubusercontent.com/45737074/213403245-d317f198-9deb-449b-8b26-317d82565aac.png)
   
   ![image](https://user-images.githubusercontent.com/45737074/213403297-d62c00ec-8d03-41dc-b038-cae09c60e123.png)


  - gunakan PM2 (Challenge)
  
  ![image](https://user-images.githubusercontent.com/45737074/213403339-0922b6fa-2458-42ec-9cba-4bafa1a9d5b4.png)
  
  ![image](https://user-images.githubusercontent.com/45737074/213403373-7902b93f-b678-4106-9f78-348671c6dd36.png)

  
4. VM2 :
  - jalankan nginx 
  - buat konfigurasi reverse proxy dengan domain (gunakan nama kalian) mengarah ke app di VM1
  ![image](https://user-images.githubusercontent.com/45737074/213546067-3ee4db62-5543-41d8-ac06-3ee5458e8c14.png)
  
  ![image](https://user-images.githubusercontent.com/45737074/213546097-79b1f0db-f0af-4962-b4c2-1e03ae0711d0.png)
  
  ![image](https://user-images.githubusercontent.com/45737074/213546123-8cb5340a-6dac-4410-aa8b-34763fbb6843.png)
  
  ![image](https://user-images.githubusercontent.com/45737074/213546161-493be6c4-d5ec-4dea-8d31-8dd829b8103e.png)
  
  ![image](https://user-images.githubusercontent.com/45737074/213546207-c9225061-8e14-47b0-82c1-2dd0dd0c03b2.png)


  - buat konfigurasi load balance antara VM1 dan VM2
  
  ![image](https://user-images.githubusercontent.com/45737074/213546249-9fe8f2f0-a4d2-4f3e-adfa-5f216b69148c.png)
  
  ![image](https://user-images.githubusercontent.com/45737074/213546296-f0877bd3-7ae8-492a-884e-f8c328f1061c.png)
  
  ![image](https://user-images.githubusercontent.com/45737074/213546319-c85de664-7ac5-4f47-be38-b7e847f80a09.png)

   
Note : kalau hanya bisa menjalankan 1 VM, kalian cukup jalankan task no 3 & 4 di 1 VM tersebut

5. Domain bisa diakses melalui web browser kalian (edit filenya di /etc/hosts)

 ![image](https://user-images.githubusercontent.com/45737074/213546354-6261cdcf-3a5e-4d71-8769-4f6f560dfe37.png)


Challenge
Load Balancer dapat berjalan dengan baik

