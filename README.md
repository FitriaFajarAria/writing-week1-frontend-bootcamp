# writing-week1-frontend-bootcamp

# React JS

React adalah library JavaScript yang deklaratif, efisien, dan fleksibel untuk membangun antarmuka pengguna yang dibuat oleh tim engineer dari Facebook, React memungkinkan kita untuk membuat antarmuka kompleks dari kumpulan kode. Beberapa alasan menggunakan react :
1. React Js memiliki performa yang lebih cepat dalam membangun sebuah user interface walaupun harus menghandle berbagai data.
2. Konsep modular pada Javascript dapat diterapkan pada react, react dapat membagi 1 tampilan pada website menjadi komponen-komponen yang lebih kecil).
3. React dapat digunakan pada aplikasi kecil maupun berskala besar dan kompleks.
4. Penggunaan react yang populer diseluruh dunia seperti pada perusahaan-perusahaan teknologi.

Kita membutuhkan create-react-app untuk membuat project Reactjs, create-react-app adalah program berbasis CLI yang memang khusus digunakan untuk membuat proyek React. Program ini akan meng-generate semua hal yang kita butuhkan untuk proyek awal (aturan penulisan nama project, harus menggunakan huruf kecil. Jika ada dua suku kata, maka bisa dipisah dengan '-'), use library pada react :

- npx adalah Node Package Runner. Fungsinya untuk mengeksekusi package Nodejs.

          npx-creat-react-app nama-project

- npm adalah Node Package Manager. Sebuah program berbasis teks untuk manajemen paket Nodejs.

          npm init-react-app nama-project
          
- yarn 

          yarn creat react-app nama-project
          cd nama-project
          yarn start
          
Pada dasarnya Reacjs hanya melakukan render komponen saat ada data yang berubah. Seperti namanya “React” ia akan breaksi saat ada perubahan data (reaktif). Komponen adalah bagian-bagian dari UI, contohnya seperti tombol, label, input, dll. Komponen juga bisa dibentuk dari komponen yang lain, langkah-langkah yang harus dilakukan untuk membuat aplikasi react adalah sebagai berikut:
1. Menambahkan library react ke HTML;
2. Membuat elemen HTML untuk wadah aplikasi;
3. Membuat komponen;
4. Me-render komponen ke HTML;
5. Setiap aplikasi react membutuhkan sebuah wadah.
Kita membuat sebuah elemen div dengan id="app".Setiap komponen yang kita buat di React akan di-render atau ditampilkan ke dalam div tersebut.

           <div id="app"></div>


#### Memahami Struktur Direktori Project React

Berikut ini adalah struktur direktori dari proyek React;

1. node_modules berisi paket-paket modul Nodejs; semua libaray yang kita install dengan npm akan disimpan di sini.
2. public berisi file untuk publik seperti HTML, CSS, icon, dan gambar, dan aset publik lainnya;
3. index.html adalah file HTML yang akan digunakan aplikasi React untuk render komponen.
4. src berisi kode dari aplikasi Reactjs, di sinilah kita akan membuat komponen;
5. App.js berisi kode untuk komponen App atau komponen utama dari aplikasi;
6. App.test.js berisi kode untuk testing komponen App;
7. index.js berisi kode untuk render komponen App ke Real DOM;
8. serviceWorker.js berisi kode untuk service worker, ini kita butuhkan nanti saat membuat aplikasi PWA (Progressive Web Apps);
9. setTests.js berisi kode untuk testing aplikasi.
10. .gitignore berisi kode-kode yang akan diabaikan oleh Git.
11. package.json file JSON yang berisi keterangan proyek dan daftar modul-modul yang dibutuhkan.
12. yarn.lock adalah file yang digunakan Yarn untuk mengunci versi-versi modul Nodejs yang digunakan.


#### Membuat Komponen React

1. Komponen React dapat dibuat dengan ketentuan umum sebagai berikut ini:

- Import library React
- Nama Fungsi diawali dengan huruf kapital
- Return value dari fungsi berupa JSX dengan satu child
- Mari kita bahas masing-masing ketentuan di atas.

2. Library React Harus Berada di Dalam Scope

Dikarenakan JSX akan di-transform ke dalam bentuk javascript oleh compiler (babel). maka kita perlu mengikut sertakan library React di setiap scope atau cakupan kode yang menggunakan JSX.

3. Nama Fungsi Diawali dengan Huruf Kapital

Sebuah fungsi dengan nama yang diawali dengan huruf kapital dan me-return JSX disebut React function component, selanjutnya kita bisa menggunakan custom tag html dengan nama fungsi tersebut.

### Keunggulan React Js

Ada beberapa fitur yang menjadi keunggulan React Js. Berikut beberapa di antaranya.
- Declarative
React dapat membuat UI (User Interfaces) yang interaktif, sehingga dapat dengan mudah membuat desain yang simple untuk di setiap state di dalam aplikasi. Declarative views dapat membuat kode lebih mudah untuk di prediksi dan lebih mudah untuk di debug.

- Component – Based
React dapat membuat Encapsulated Component yang dapat mengatur setiap tahapannya, lalu dapat membuat complex UIs berdasarkan kemampuan itu.

- Learn Once, Write Anywhere
Developer dapat mengembangkan fitur baru menggunakan react tanpa mengubah kode sebelumnya, react juga dapat bekerja menggunakan Node JS dan mobile apps menggunakan React Native.
React memiliki yang namanya component, component yaitu sesuatu yang UI dalam satua-satuan yang kecil (dalam 1 page terdapat beberapa component yang dapat kita buat). Component dapat dibuat menggunakan function dan class. Component menerima beberapa masukan/Props (singkatan dari properti) dan mengembalikan element React yang mendeskripsikan apa yang seharusnya tampil pada layar.

### Component di React

Komponen di Reactjs dapat kita buat dengan dua cara pertama menggunakan fungsi, dan kedua menggunakan class. Komponen yang dibuat dengan fungsi disebut juga dengan function components dan yang menggunakan class disebut class components.

![functionComponents](https://www.petanikode.com/img/react/komponen/function-component.png)

Sedangkan untuk class component, cara membuatnya harus melakukan extends dari class React.Component.

![classComponents](https://www.petanikode.com/img/react/komponen/class-component.png)

### Membuat UI Element dengan React js 

Buat file pada direktori src dengan .js

       import React from 'react';
       function HelloWorld() {
       return (
          <h1>HelloWorld</h1>
        );
       }
    
        Export default HelloWorld;


Edit file App.js

          import React from 'react';
          import HelloWorld from '.HelloWorld';

          function App() {
          return (
           <div>
              <HelloWorld />
          </div>
           );
          }
          
          export default App;

### JSX in React

          const element = (
                <div>
                     <h1>Halo!</h1>
                     <h2>Senang melihatmu di sini.</h2>
                </div>
          );
          
Sintaksis ini di kenal dengan sebutan JSX (Javascript XML) adalah extension dari Javasript. JSX membuat kita bisa menggunakan HTML di dalam Javascript, sama seperti XML dan HTML, ia juga memiliki nama tag, atribut, dan elemen anak. JSX akan menghasilkan "elemen" React. Kita dapat menggunakan JSX di dalam pernyataan if dan perulangan for, memasukkannya ke dalam variabel, menerimanya sebagai argumen, dan mengembalikannya dari sebuah fungsi. 

Pada JSX class akan menjadi className serta di JSX sendiri hanya memiliki 1 element parent (gunakan tag <div></div> atau fragment kosong <></> sebagai parent dari element lain), dengan JSX kita dapat menggunakan tag HTML didalam file extention .js.
Tanpa JSX, kita bisa membuat elemen React dengan method:

                    React.createElement();
                    
                    
 ![React.createElement](https://www.petanikode.com/img/reactjs-jsx/react-element.png)
 
Method ini punya tiga parameter yang wajib diisi:

- Type elemen dalam bentuk string;
- Properti element dalam bentuk object;
- Children dalam bentuk string dan juga object react element;

#### Aturan Penulisan JSX

1. Tempat Penulisan JSX
JSX biasnaya ditulis di dalam method render() pada class component dan pada statement return di function component.

2. JSX yang punya banyak element
Mengguakan induk, menggunakan fragment.

3. Penulisan Atribut di JSX
Penulisan atribut di JSX sama seperti penulisan atribut di HTML biasa, hanya saja beberapa atribut harus ditulis dengan aturan JSX. Misalnya seperti atribut class, pada pada JSX ditulis dengan className (class adalah kata kunci yang sudah ada di Javascript untuk membuat class. Sebenarnya bisa juga kita pakai atribut class saja di JSX, tapi nanti akan dapat warning. Karena itu, untuk menghindari ambigu disarankan pakai className saja).

Pada HTML biasa kita tulis dengan huruf kecil semua, sedangkan pada JSX ditulis dengan format CamelCase. Di dalam sintaks JSX, kita bisa membuat ekspresi Javascript dengan kurung kurawal { ... }. Ekspresi ini dapat ditulis di dalam nilai atribut maupun di dalam konten elemen.

#### Conditional di JSX

Conditional react berfungsi sama halnya dengan operator bersyarat pada Javascript. Gunakan JavaScript operator seperti if atau operator bersyarat untuk membuat representasi elemen dari state saat ini, dan React akan memperbarui UI sesuai dengan state tersebut.

### Virtual DOM 

Virtual DOM (VDOM) adalah duplikasi dari real DOM dan merupakan sebuah konsep dalam pemrograman di mana representasi ideal atau virtual dari antarmuka pengguna disimpan dalam memori dan disinkronkan dengan DOM oleh library seperti ReactDOM, istilah “virtual DOM” biasanya dikaitkan dengan elemen React karena mereka adalah objek yang mewakili antarmuka pengguna. 

![Virtual DOM](https://www.petanikode.com/img/react/komponen/virtualdom.png)

### State dan Props

Props (kependekan dari properti) dan state adalah objek JavaScript biasa. Meskipun keduanya menyimpan informasi yang mempengaruhi keluaran dari render, keduanya berbeda satu sama lain, props diteruskan ke komponen (mirip dengan function parameters) sedangkan state dikelola dalam komponen (mirip dengan variabel yang dideklarasikan dalam suatu function). Kedua objek ini memiliki cara kerja yang berbeda.

State adalah objek yang digunakan untuk menyimpan data di dalam komponen, sedangkan props adalah objek yang digunakan untuk menyimpan data yang diterima dari luar komponen. Data yang disimpan di dalam state bisa kita ubah-ubah, sedangkan data yang disimpan di dalam props tidak bisa diubah karena sifatnya read-only. Nah untuk mengubah nilai pada state, kita bisa menggunakan method setState().

#### Stateful Component dengan Stateless Component

Stateful components adalah komponen yang menggunakan state. Sedangkan Stateless adalah komponen yang tidak menggunakan state.
Stateful components juga dikenal dengan sebutan Container dan Smart components. Stateless juga dikenal dengan sebutan Presentation dan Dumb Components.

![stateful and stateless Component](https://www.petanikode.com/img/react/komponen/stateful-stateless.png)

