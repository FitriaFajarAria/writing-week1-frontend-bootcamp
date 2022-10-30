# writing-week1-frontend-bootcamp

# React JS

React adalah library JavaScript yang deklaratif, efisien, dan fleksibel untuk membangun antarmuka pengguna yang dibuat oleh tim engineer dari Facebook, React memungkinkan kita untuk membuat antarmuka kompleks dari kumpulan kode. Beberapa alasan menggunakan react :
1. React Js memiliki performa yang lebih cepat dalam membangun sebuah user interface walaupun harus menghandle berbagai data.
2. Konsep modular pada Javascript dapat diterapkan pada react, react dapat membagi 1 tampilan pada website menjadi komponen-komponen yang lebih kecil).
3. React dapat digunakan pada aplikasi kecil maupun berskala besar dan kompleks.
4. Penggunaan react yang populer diseluruh dunia seperti pada perusahaan-perusahaan teknologi.

use library pada react :
- npx adalah Node Package Runner. Fungsinya untuk mengeksekusi package Nodejs.

          npx-creat-react-app nama-project

- npm adalah Node Package Manager. Sebuah program berbasis teks untuk manajemen paket Nodejs.

          npm init-react-app nama-project
          
- yarn 

          yarn creat react-app nama-project
          cd nama-project
          yarn start
          
### Keunggulan React Js

Ada beberapa fitur yang menjadi keunggulan React Js. Berikut beberapa di antaranya.
- Declarative
React dapat membuat UI (User Interfaces) yang interaktif, sehingga dapat dengan mudah membuat desain yang simple untuk di setiap state di dalam aplikasi. Declarative views dapat membuat kode lebih mudah untuk di prediksi dan lebih mudah untuk di debug.

- Component – Based
React dapat membuat Encapsulated Component yang dapat mengatur setiap tahapannya, lalu dapat membuat complex UIs berdasarkan kemampuan itu.

- Learn Once, Write Anywhere
Developer dapat mengembangkan fitur baru menggunakan react tanpa mengubah kode sebelumnya, react juga dapat bekerja menggunakan Node JS dan mobile apps menggunakan React Native.
React memiliki yang namanya component, component yaitu sesuatu yang UI dalam satua-satuan yang kecil (dalam 1 page terdapat beberapa component yang dapat kita buat). Component dapat dibuat menggunakan function dan class. Component menerima beberapa masukan/Props (singkatan dari properti) dan mengembalikan element React yang mendeskripsikan apa yang seharusnya tampil pada layar.

### Membuat UI Element dengan React js 

       import React from 'react';
       function HelloWorld() {
       return (
       <h1>HelloWorld</h1>
        );
       }
    
        Export default HelloWorld;
