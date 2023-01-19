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
  
  - buat konfigurasi load balance antara VM1 dan VM2
   
Note : kalau hanya bisa menjalankan 1 VM, kalian cukup jalankan task no 3 & 4 di 1 VM tersebut

5. Domain bisa diakses melalui web browser kalian (edit filenya di /etc/hosts)
 

Challenge
Load Balancer dapat berjalan dengan baik

