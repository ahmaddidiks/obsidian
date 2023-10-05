Sumber : https://www.youtube.com/watch?v=JOXbresHhIk&list=PL-CtdCApEFH-0i9dzMzLw6FKVrFWv3QvQ&index=1
Go module sangat mudah diintegrasikan. Secara umum dalam membuta aplikasi kita membuat dua hal, yang pertama module, yang kedua membuat aplikasinya itu sendiri yang menggunakan module yang kita buat.

## Cara membuat module
1. Buat repository github
2. Inisiasi module ```go mod init github.com/ahmaddidiks/first-module```
3. Push repo
4. Tambahkan tag untuk release module, biasanya dimulai dengan huruf 'v'. Contohnya adalah v1.0.0 
5. ```git tag v1.0.0```
6. ```git push origin v1.0.0```
7. Membuat aplikasinya
8. ```go mod init github/ahmaddidiks/app-first-app```
9. Menambahkan dependency
10. ```go get github.com/ahmaddidiks/first-module```
11. Melakukan upgrade module
12. ```upgrade code```
13. Tambah tag baru
14. ```git tag v1.0.1```
15. ```git push origin v1.0.1```
16. Upgrade dendency di aplikasi --> bisa langsung ubah v tag di file go mod nya dan lanjut go get di terminal
17. ```go get```
18. Jika ada major upgrade module, maka yang perlu dilakukan adalah merubah nama modulenya menjadi github.com/ahmaddidiks/first-module/v2 di go mod repo module dan menaikan versi tag nya
19. ```git tag v2.0.0```
20. ```git push origin v2.0.0```
21. Upgrade module di aplikasi, hapus module di file go mod
22. ```go get github.com/ahmaddidiks/first-module/v2```
23. 
24. 