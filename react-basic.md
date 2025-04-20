# KURIKULUM DEVELOPER REACT EXPERT

## OVERVIEW

**Nama Program**: React Expert Developer Path  
**Durasi**: 6 bulan (24 minggu)  
**Level**: Basic hingga Expert  
**Metode Pembelajaran**: Teori dan Praktek (Project-based)

## TIMELINE PEMBELAJARAN

- **Level Basic** (Minggu 1-6): 6 minggu
- **Level Intermediate** (Minggu 7-14): 8 minggu 
- **Level Advanced** (Minggu 15-20): 6 minggu
- **Level Expert** (Minggu 21-24): 4 minggu

## DAFTAR MODUL

### LEVEL BASIC (Minggu 1-6)

#### MODUL 1: PENGENALAN WEB DEVELOPMENT (Minggu 1)
- **Durasi**: 1 minggu
- **Tujuan**: Memahami fondasi web development dan JavaScript modern yang diperlukan untuk React
- **Materi**:
  - HTML5 dan Semantic Elements
  - CSS3, Flexbox dan Grid
  - JavaScript Fundamentals dan ES6+
  - DOM Manipulation
  - Browser Developer Tools
- **Project**: Landing page sederhana dengan JavaScript interaktif

#### MODUL 2: PENGENALAN REACT (Minggu 2-3)
- **Durasi**: 2 minggu
- **Tujuan**: Memahami konsep dasar React dan cara kerjanya
- **Materi**:
  - Apa itu React dan Virtual DOM
  - Setting up React environment (Create React App)
  - JSX Syntax
  - Function Components vs Class Components
  - Props dan Component Composition
  - Event Handling di React
- **Project**: Konversi landing page dari Modul 1 ke React

#### MODUL 3: REACT FUNDAMENTALS (Minggu 4-6)
- **Durasi**: 3 minggu
- **Tujuan**: Menguasai konsep state, lifecycle, dan rendering di React
- **Materi**:
  - React Hooks: useState dan useEffect
  - Conditional Rendering
  - Lists dan Keys
  - Forms dan Controlled Components
  - Styling di React
  - Component Lifecycle
- **Project**: To-Do List Application

### LEVEL INTERMEDIATE (Minggu 7-14)

#### MODUL 4: REACT ECOSYSTEM & ROUTING (Minggu 7-8)
- **Durasi**: 2 minggu
- **Tujuan**: Memahami ekosistem React dan implementasi routing
- **Materi**:
  - React Router
  - Navigation dan URL Parameters
  - Nested Routes
  - Protected Routes
  - Code Splitting
  - Lazy Loading
- **Project**: Multi-page Application dengan React Router

#### MODUL 5: STATE MANAGEMENT (Minggu 9-11)
- **Durasi**: 3 minggu
- **Tujuan**: Menguasai state management di aplikasi React yang kompleks
- **Materi**:
  - Context API dan useContext
  - React Redux
  - Redux Toolkit
  - Immutability Patterns
  - Middleware dan Side Effects
  - Redux Thunk vs Redux Saga
- **Project**: E-Commerce App dengan state management kompleks

#### MODUL 6: DATA FETCHING & API INTEGRATION (Minggu 12-14)
- **Durasi**: 3 minggu
- **Tujuan**: Menguasai teknik fetching data dan integrasi API
- **Materi**:
  - Fetch API dan Axios
  - Custom Hooks untuk Data Fetching
  - React Query dan SWR
  - Loading States dan Error Handling
  - Caching dan Optimistic Updates
  - Authentication Flow
- **Project**: Dashboard App dengan integrasi API

### LEVEL ADVANCED (Minggu 15-20)

#### MODUL 7: ADVANCED HOOKS & PATTERNS (Minggu 15-16)
- **Durasi**: 2 minggu
- **Tujuan**: Memahami hooks lanjutan dan pattern design React
- **Materi**:
  - useCallback, useMemo, dan useRef
  - Custom Hooks Development
  - Higher-Order Components
  - Render Props Pattern
  - Compound Components
  - Control Props Pattern
- **Project**: Library of reusable React components

#### MODUL 8: PERFORMANCE OPTIMIZATION (Minggu 17-18)
- **Durasi**: 2 minggu
- **Tujuan**: Mengoptimalkan performa aplikasi React
- **Materi**:
  - React Profiler & Chrome DevTools
  - Code Splitting & Lazy Loading
  - React.memo dan PureComponent
  - Virtualization dengan React Window
  - Web Vitals Optimization
  - Bundle Analysis dan Optimization
- **Project**: Optimizing an existing React application

#### MODUL 9: TESTING & DEBUGGING (Minggu 19-20)
- **Durasi**: 2 minggu
- **Tujuan**: Menguasai teknik testing dan debugging di React
- **Materi**:
  - Jest dan React Testing Library
  - Component Testing
  - Integration Testing
  - Snapshot Testing
  - Mocking API Calls
  - Advanced Debugging Techniques
- **Project**: Test suite untuk aplikasi React

### LEVEL EXPERT (Minggu 21-24)

#### MODUL 10: SERVER-SIDE RENDERING & STATIC SITE GENERATION (Minggu 21-22)
- **Durasi**: 2 minggu
- **Tujuan**: Memahami SSR dan SSG dengan React
- **Materi**:
  - Next.js Fundamentals
  - SSR vs SSG vs ISR
  - Data Fetching in Next.js
  - API Routes
  - SEO Optimization
  - Deployment Strategies
- **Project**: Blog platform dengan Next.js

#### MODUL 11: ADVANCED STATE MANAGEMENT & ARCHITECTURE (Minggu 23)
- **Durasi**: 1 minggu
- **Tujuan**: Menguasai arsitektur state management tingkat lanjut
- **Materi**:
  - State Machines dengan XState
  - Zustand dan Jotai
  - Redux vs Context API (Tradeoffs)
  - Micro Frontends
  - Monorepo Architecture
  - Module Federation
- **Project**: Enterprise-level application architecture

#### MODUL 12: CAPSTONE PROJECT & ADVANCED TOPICS (Minggu 24)
- **Durasi**: 1 minggu
- **Tujuan**: Menggabungkan semua pembelajaran dalam proyek kompleks
- **Materi**:
  - React 18 Features
  - Concurrent Mode
  - React Server Components
  - Suspense for Data Fetching
  - Web Animations API integration
  - WebAssembly dengan React
- **Project**: Full-stack application dengan fitur modern React

---
# MODUL 1: PENGENALAN WEB DEVELOPMENT

## Informasi Umum
- **Durasi**: 1 minggu
- **Tujuan**: Memahami fondasi web development dan JavaScript modern yang diperlukan untuk React
- **Project Akhir**: Landing page sederhana dengan JavaScript interaktif

## Daftar Isi
1. [HTML5 dan Semantic Elements](#html5-dan-semantic-elements)
2. [CSS3, Flexbox dan Grid](#css3-flexbox-dan-grid)
3. [JavaScript Fundamentals dan ES6+](#javascript-fundamentals-dan-es6)
4. [DOM Manipulation](#dom-manipulation)
5. [Browser Developer Tools](#browser-developer-tools)
6. [Project Akhir](#project-akhir)

---

## HTML5 dan Semantic Elements

### Apa itu HTML?
HTML (HyperText Markup Language) adalah bahasa markup standar yang digunakan untuk membuat struktur sebuah halaman web. HTML terdiri dari serangkaian elemen yang memberitahu browser cara menampilkan konten.

### Struktur Dasar HTML5
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Judul Halaman</title>
</head>
<body>
    <!-- Konten halaman web di sini -->
</body>
</html>
```

### Semantic Elements
Semantic elements adalah elemen HTML yang memiliki arti atau makna yang jelas tentang konten yang dikandungnya. Ini membantu browser, developer, dan teknologi assistive untuk memahami struktur halaman web.

#### Keuntungan Semantic Elements:
- Meningkatkan SEO (Search Engine Optimization)
- Membuat kode lebih mudah dibaca dan dipelihara
- Meningkatkan aksesibilitas

#### Contoh Semantic Elements:
- `<header>` - Menandai bagian header halaman
- `<nav>` - Berisi menu navigasi utama
- `<main>` - Berisi konten utama halaman
- `<section>` - Mengelompokkan konten berdasarkan tema
- `<article>` - Konten yang berdiri sendiri
- `<aside>` - Konten yang berhubungan dengan konten utama
- `<footer>` - Menandai bagian footer halaman

### Contoh Penggunaan Semantic Elements
```html
<header>
    <h1>Judul Website</h1>
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>
</header>

<main>
    <section id="about">
        <h2>About Us</h2>
        <p>Informasi tentang perusahaan kami...</p>
    </section>
    
    <section id="services">
        <h2>Our Services</h2>
        <article>
            <h3>Web Development</h3>
            <p>Deskripsi layanan web development...</p>
        </article>
        <article>
            <h3>Mobile Development</h3>
            <p>Deskripsi layanan mobile development...</p>
        </article>
    </section>
    
    <aside>
        <h3>Related Information</h3>
        <p>Informasi tambahan yang relevan...</p>
    </aside>
</main>

<footer>
    <p>&copy; 2025 Company Name. All rights reserved.</p>
</footer>
```

### Latihan:
1. Buatlah struktur HTML dasar untuk halaman profil pribadi
2. Gunakan minimal 5 semantic elements berbeda
3. Tambahkan konten seperti judul, paragraf, gambar, dan link

---

## CSS3, Flexbox dan Grid

### Apa itu CSS?
CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mengatur tampilan dan format elemen HTML. CSS memisahkan konten (HTML) dari presentasi (CSS).

### Cara Menambahkan CSS ke HTML
1. **Inline CSS** - Menggunakan atribut `style` pada elemen HTML
   ```html
   <p style="color: blue; font-size: 16px;">Ini adalah paragraf berwarna biru.</p>
   ```

2. **Internal CSS** - Menggunakan tag `<style>` di dalam `<head>`
   ```html
   <head>
       <style>
           p {
               color: blue;
               font-size: 16px;
           }
       </style>
   </head>
   ```

3. **External CSS** (Direkomendasikan) - Membuat file CSS terpisah
   ```html
   <head>
       <link rel="stylesheet" href="styles.css">
   </head>
   ```

### CSS Selectors
CSS Selectors digunakan untuk memilih elemen HTML yang ingin kita styling.

```css
/* Element selector */
p {
    color: blue;
}

/* Class selector */
.highlight {
    background-color: yellow;
}

/* ID selector */
#header {
    font-size: 24px;
}

/* Descendant selector */
nav a {
    text-decoration: none;
}

/* Pseudo-class */
a:hover {
    color: red;
}
```

### Flexbox
Flexbox adalah model layout CSS yang memudahkan pengaturan elemen dalam satu dimensi (baris atau kolom). Flexbox sangat berguna untuk membuat layout yang responsif.

#### Properti Utama Flexbox:
- `display: flex` - Mengaktifkan flexbox
- `flex-direction` - Menentukan arah (row, column)
- `justify-content` - Mengatur perataan horizontal
- `align-items` - Mengatur perataan vertikal
- `flex-wrap` - Mengatur apakah items bisa wrap ke baris berikutnya

#### Contoh Flexbox:
```css
.container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
}

.item {
    flex: 1;
    margin: 10px;
}
```

### CSS Grid
CSS Grid adalah sistem layout dua dimensi yang memungkinkan pengaturan elemen dalam baris dan kolom secara bersamaan. Grid sangat powerful untuk layout kompleks.

#### Properti Utama Grid:
- `display: grid` - Mengaktifkan grid
- `grid-template-columns` - Mendefinisikan kolom
- `grid-template-rows` - Mendefinisikan baris
- `grid-gap` - Jarak antar sel grid
- `grid-template-areas` - Layout visual untuk grid

#### Contoh Grid:
```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: auto;
    grid-gap: 20px;
}

.header {
    grid-column: 1 / -1;  /* Dari kolom pertama sampai terakhir */
}
```

### Latihan:
1. Buatlah layout dengan flexbox untuk menu navigasi horizontal
2. Buatlah layout grid dengan 3 kolom untuk bagian galeri foto
3. Buat layout responsif yang berubah dari 3 kolom ke 1 kolom pada layar kecil

---

## JavaScript Fundamentals dan ES6+

### Apa itu JavaScript?
JavaScript adalah bahasa pemrograman yang memungkinkan website menjadi interaktif. JavaScript dapat memanipulasi konten HTML, merespon interaksi user, mengambil data dari server, dan banyak lagi.

### Cara Menambahkan JavaScript ke HTML
```html
<!-- Internal JavaScript -->
<script>
    console.log("Hello World!");
</script>

<!-- External JavaScript (Direkomendasikan) -->
<script src="script.js"></script>
```

### Variabel dan Tipe Data
```javascript
// var (hindari penggunaan var, gunakan let dan const)
var nama = "John";

// let - untuk variabel yang nilainya bisa berubah
let umur = 25;
umur = 26; // OK

// const - untuk variabel yang nilainya tetap
const PI = 3.14;
// PI = 3.15; // Error!

// Tipe data
let nama = "John";               // String
let umur = 25;                   // Number
let isActive = true;             // Boolean
let hobbies = ["Coding", "Reading"];  // Array
let person = {                   // Object
    name: "John",
    age: 25
};
let nothing = null;              // Null
let notDefined;                  // Undefined
```

### Operator
```javascript
// Arithmetic operators
let a = 10 + 5;  // 15 (addition)
let b = 10 - 5;  // 5 (subtraction)
let c = 10 * 5;  // 50 (multiplication)
let d = 10 / 5;  // 2 (division)
let e = 10 % 3;  // 1 (modulus - remainder)

// Comparison operators
let f = (10 > 5);   // true
let g = (10 < 5);   // false
let h = (10 >= 10); // true
let i = (10 == 10); // true
let j = (10 === "10"); // false (strict equality - checks type)

// Logical operators
let k = (true && false); // false (AND)
let l = (true || false); // true (OR)
let m = !true;           // false (NOT)
```

### Conditional Statements
```javascript
// if statement
let age = 18;

if (age >= 18) {
    console.log("Anda dewasa");
} else if (age >= 13) {
    console.log("Anda remaja");
} else {
    console.log("Anda anak-anak");
}

// Ternary operator
let status = age >= 18 ? "dewasa" : "belum dewasa";

// Switch statement
let day = 1;
switch (day) {
    case 1:
        console.log("Senin");
        break;
    case 2:
        console.log("Selasa");
        break;
    default:
        console.log("Hari lain");
}
```

### Loops
```javascript
// For loop
for (let i = 0; i < 5; i++) {
    console.log(i); // 0, 1, 2, 3, 4
}

// While loop
let i = 0;
while (i < 5) {
    console.log(i); // 0, 1, 2, 3, 4
    i++;
}

// For...of (untuk Array)
const fruits = ["Apple", "Banana", "Orange"];
for (const fruit of fruits) {
    console.log(fruit);
}

// For...in (untuk Object)
const person = {name: "John", age: 25};
for (const key in person) {
    console.log(key + ": " + person[key]);
}
```

### Functions
```javascript
// Function declaration
function greet(name) {
    return "Hello, " + name + "!";
}

// Function expression
const greet = function(name) {
    return "Hello, " + name + "!";
};

// Arrow function (ES6+)
const greet = (name) => {
    return "Hello, " + name + "!";
};

// Simplified arrow function (single return)
const greet = name => "Hello, " + name + "!";

// Calling a function
console.log(greet("John")); // "Hello, John!"
```

### ES6+ Features

#### 1. Template Literals
```javascript
const name = "John";
const greeting = `Hello, ${name}!`; // "Hello, John!"
```

#### 2. Destructuring
```javascript
// Array destructuring
const [first, second] = [1, 2];
console.log(first); // 1

// Object destructuring
const person = { name: "John", age: 25 };
const { name, age } = person;
console.log(name); // "John"
```

#### 3. Spread Operator
```javascript
// Spread pada array
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5]; // [1, 2, 3, 4, 5]

// Spread pada object
const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 }; // { a: 1, b: 2, c: 3 }
```

#### 4. Default Parameters
```javascript
function greet(name = "Guest") {
    return `Hello, ${name}!`;
}

console.log(greet()); // "Hello, Guest!"
```

#### 5. Array Methods
```javascript
const numbers = [1, 2, 3, 4, 5];

// map - membuat array baru dengan transformasi
const doubled = numbers.map(num => num * 2); // [2, 4, 6, 8, 10]

// filter - membuat array baru dengan filter
const evens = numbers.filter(num => num % 2 === 0); // [2, 4]

// reduce - mereduksi array menjadi satu nilai
const sum = numbers.reduce((total, num) => total + num, 0); // 15
```

### Latihan:
1. Buat fungsi untuk menghitung faktorial
2. Buat program untuk memfilter array angka menjadi array angka genap saja
3. Buat program untuk menampilkan daftar nama dari array objek pengguna

---

## DOM Manipulation

### Apa itu DOM?
DOM (Document Object Model) adalah representasi struktur dari dokumen HTML dalam bentuk objek yang dapat dimanipulasi dengan JavaScript. DOM memungkinkan JavaScript untuk mengubah konten, struktur, dan style halaman web secara dinamis.

### Mengakses Elemen DOM
```javascript
// Mengakses elemen berdasarkan ID
const header = document.getElementById("header");

// Mengakses elemen berdasarkan nama tag
const paragraphs = document.getElementsByTagName("p");

// Mengakses elemen berdasarkan nama class
const highlights = document.getElementsByClassName("highlight");

// Mengakses elemen menggunakan CSS selector (lebih modern)
const firstParagraph = document.querySelector("p");
const allButtons = document.querySelectorAll("button");
```

### Memanipulasi Konten DOM
```javascript
// Mengubah text content
element.textContent = "Teks baru";

// Mengubah HTML content
element.innerHTML = "<strong>Teks tebal</strong>";

// Mengubah atribut
element.setAttribute("href", "https://example.com");
element.id = "newId";

// Mengubah style
element.style.color = "blue";
element.style.fontSize = "16px";
```

### Memanipulasi Class
```javascript
// Tambah class
element.classList.add("active");

// Hapus class
element.classList.remove("disabled");

// Toggle class (tambah jika tidak ada, hapus jika ada)
element.classList.toggle("highlight");

// Cek apakah elemen memiliki class tertentu
const hasClass = element.classList.contains("active");
```

### Membuat dan Menghapus Elemen
```javascript
// Membuat elemen baru
const newParagraph = document.createElement("p");
newParagraph.textContent = "Ini adalah paragraf baru";

// Menambahkan elemen ke DOM
parentElement.appendChild(newParagraph);

// Menambahkan elemen sebelum elemen lain
parentElement.insertBefore(newParagraph, referenceElement);

// Menghapus elemen
element.remove();
// atau
parentElement.removeChild(element);
```

### Event Handling
```javascript
// Metode addEventListener
const button = document.querySelector("button");
button.addEventListener("click", function() {
    alert("Button diklik!");
});

// Menggunakan arrow function
button.addEventListener("click", () => {
    alert("Button diklik!");
});

// Menambahkan event dengan atribut HTML
// <button onclick="handleClick()">Klik Saya</button>
function handleClick() {
    alert("Button diklik!");
}

// Event object
button.addEventListener("click", function(event) {
    console.log(event.target); // Elemen yang memicu event
    event.preventDefault(); // Mencegah default action
});
```

### Common DOM Events
- `click` - Ketika elemen diklik
- `dblclick` - Ketika elemen diklik dua kali
- `mouseenter` - Ketika mouse masuk ke area elemen
- `mouseleave` - Ketika mouse keluar dari area elemen
- `keydown` - Ketika keyboard key ditekan
- `keyup` - Ketika keyboard key dilepas
- `submit` - Ketika form di-submit
- `load` - Ketika halaman selesai dimuat
- `resize` - Ketika window diubah ukurannya
- `scroll` - Ketika user melakukan scroll

### Latihan:
1. Buat form dengan validasi JavaScript sederhana
2. Buat toggle button yang mengubah tema halaman (light/dark)
3. Buat to-do list sederhana yang bisa menambah dan menghapus item

---

## Browser Developer Tools

### Apa itu Browser Developer Tools?
Browser Developer Tools adalah sekumpulan alat pengembangan yang sudah terintegrasi di dalam browser modern. Tools ini sangat membantu developer untuk melakukan debugging, testing, dan optimization website.

### Cara Membuka Developer Tools
- **Chrome/Edge**: Tekan F12 atau Ctrl+Shift+I (Windows/Linux) atau Cmd+Option+I (Mac)
- **Firefox**: Tekan F12 atau Ctrl+Shift+I (Windows/Linux) atau Cmd+Option+I (Mac)
- **Safari**: Aktifkan Developer Menu dari Preferences > Advanced, lalu pilih Show Develop menu in menu bar. Kemudian tekan Cmd+Option+I

### Komponen Utama Developer Tools

#### 1. Elements/Inspector Panel
- Melihat dan memanipulasi DOM
- Melihat dan mengubah CSS
- Menguji perubahan secara langsung
- Melihat box model

#### 2. Console Panel
- Menjalankan JavaScript secara langsung
- Melihat error dan warning
- Output dari console.log()
- Debugging interaktif

#### 3. Network Panel
- Memantau request dan response
- Melihat HTTP headers
- Menganalisis waktu loading
- Melihat size resources

#### 4. Sources/Debugger Panel
- Melihat source code website
- Debugging JavaScript dengan breakpoints
- Melacak perubahan variabel
- Testing kode secara langsung

#### 5. Performance Panel
- Menganalisis performa website
- Melihat CPU usage
- Melihat rendering performance
- Mencari bottleneck

#### 6. Application/Storage Panel
- Melihat dan mengelola cookies
- Melihat dan mengelola localStorage dan sessionStorage
- Mengelola cache
- Melihat service workers

### Debugging dengan Developer Tools
1. **Cek HTML**: Gunakan Elements panel untuk memeriksa struktur HTML
2. **Cek CSS**: Gunakan Elements > Styles untuk memeriksa dan memodifikasi CSS
3. **Cek JavaScript**: Gunakan Console untuk melihat error dan output console.log()
4. **Debugging JavaScript**:
   - Tambahkan `debugger;` pada kode JavaScript
   - Atau tambahkan breakpoint via Sources panel
   - Jalankan kode step by step untuk melihat perubahan
5. **Cek Performance**: Gunakan Lighthouse atau Performance panel untuk menganalisis performa

### Tips Menggunakan Developer Tools
- Gunakan `console.log()`, `console.table()`, dan `console.dir()` untuk debugging
- Gunakan fitur "device emulation" untuk menguji responsive design
- Gunakan Network Throttling untuk menguji performa pada koneksi lambat
- Gunakan fitur screenshot untuk mengambil gambar halaman web atau elemen tertentu
- Simpan perubahan lokal dengan fitur Workspace

### Latihan:
1. Debugging JavaScript: Temukan dan perbaiki error pada sebuah kode JavaScript menggunakan Console dan Sources panel
2. CSS Debugging: Ubah tampilan elemen menggunakan Inspector dan CSS panel
3. Network Analysis: Analisis waktu loading website dan identifikasi resource yang bisa dioptimasi

---

## Project Akhir

### Landing Page Sederhana dengan JavaScript Interaktif

#### Tujuan Project:
Membuat landing page sederhana untuk produk atau jasa fiktif dengan fitur interaktif menggunakan JavaScript.

#### Persyaratan:
1. **Struktur HTML5** yang rapi dengan semantic elements
2. **Layout Responsif** menggunakan Flexbox atau Grid
3. **Styling** yang menarik dengan CSS3
4. **Fitur Interaktif** yang diimplementasikan dengan JavaScript:
   - Form validasi
   - Galeri gambar/slideshow
   - Navigasi sticky/smooth scroll
   - Toggle menu untuk mobile
   - Fitur counter/timer/animasi sederhana
5. **Clean Code** dengan komentar yang jelas
6. **Cross Browser Compatibility** (Chrome, Firefox, Edge)

#### Langkah-langkah:
1. Buat struktur dasar HTML dengan semantic elements
2. Buat wireframe/sketsa layout
3. Implementasikan CSS untuk styling dan layout
4. Tambahkan interaktivitas dengan JavaScript
5. Uji responsivitas dan fungsionalitas
6. Debug dan optimasi

#### Contoh Struktur Project:
```
/project
  index.html
  /css
    style.css
  /js
    script.js
  /images
    logo.png
    banner.jpg
    ...
```

#### Tips:
- Mulai dengan mobile-first approach
- Gunakan variables CSS untuk konsistensi warna dan font
- Implementasikan fitur satu per satu
- Gunakan developer tools untuk debugging
- Terapkan best practices yang telah dipelajari

#### Kriteria Penilaian:
- Kerapihan dan keterbacaan kode
- Struktur HTML yang semantik
- Responsivitas pada berbagai ukuran layar
- Fungsionalitas JavaScript yang berjalan dengan baik
- Kreativitas dan desain visual
- Optimasi performa

---

Selamat belajar Web Development! Modul ini merupakan fondasi penting untuk melanjutkan ke tahap React Development pada modul berikutnya.
# MODUL 7: ADVANCED HOOKS & PATTERNS

## Informasi Umum
- **Durasi**: 2 minggu (Minggu 15-16)
- **Tujuan**: Memahami hooks lanjutan dan pattern design React
- **Project Akhir**: Library of reusable React components

## Daftar Isi
1. [useCallback, useMemo, dan useRef](#1-usecallback-usememo-dan-useref)
2. [Custom Hooks Development](#2-custom-hooks-development)
3. [Higher-Order Components](#3-higher-order-components)
4. [Render Props Pattern](#4-render-props-pattern)
5. [Compound Components](#5-compound-components)
6. [Control Props Pattern](#6-control-props-pattern)
7. [Project: Library of Reusable Components](#7-project-library-of-reusable-components)

---

## 1. useCallback, useMemo, dan useRef

### useCallback

`useCallback` adalah hook React yang memungkinkan kita menyimpan fungsi dalam memori (memoize) sehingga fungsi tersebut tidak dibuat ulang pada setiap render kecuali dependensinya berubah.

#### Kenapa menggunakan useCallback?

- Mencegah re-render yang tidak perlu pada child components
- Meningkatkan performa aplikasi terutama untuk fungsi yang dioper sebagai props
- Mencegah side effect yang tidak diinginkan

#### Contoh penggunaan:

```jsx
import React, { useState, useCallback } from 'react';

function ParentComponent() {
  const [count, setCount] = useState(0);
  
  // Tanpa useCallback - fungsi ini dibuat ulang setiap render
  // const handleClick = () => {
  //   setCount(count + 1);
  // };
  
  // Dengan useCallback - fungsi hanya dibuat ulang jika dependensi berubah
  const handleClick = useCallback(() => {
    setCount(prevCount => prevCount + 1);
  }, []);
  
  return (
    <div>
      <p>Count: {count}</p>
      <ChildComponent onClick={handleClick} />
    </div>
  );
}

function ChildComponent({ onClick }) {
  console.log('Child component rendered');
  return <button onClick={onClick}>Increment</button>;
}
```

### useMemo

`useMemo` adalah hook yang memungkinkan kita menyimpan hasil perhitungan dalam memori dan hanya menghitung ulang ketika dependensinya berubah.

#### Kenapa menggunakan useMemo?

- Menghindari perhitungan yang mahal pada setiap render
- Mengoptimalkan performa untuk operasi yang berat
- Menjaga referential equality untuk objek kompleks

#### Contoh penggunaan:

```jsx
import React, { useState, useMemo } from 'react';

function ExpensiveCalculation({ list, filter }) {
  // Tanpa useMemo - perhitungan dilakukan setiap render
  // const filteredList = list.filter(item => item.includes(filter));
  
  // Dengan useMemo - perhitungan hanya dilakukan jika list atau filter berubah
  const filteredList = useMemo(() => {
    console.log('Filtering list...');
    return list.filter(item => item.includes(filter));
  }, [list, filter]);
  
  return (
    <ul>
      {filteredList.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  );
}
```

### useRef

`useRef` adalah hook yang memberikan kita objek ref yang stabil (tidak berubah antar render) dengan property `.current` yang dapat dimutasi.

#### Penggunaan useRef:

1. **Mengakses DOM elements**:
   Mendapatkan akses langsung ke elemen DOM

2. **Menyimpan nilai yang persistant**:
   Menyimpan data yang tetap ada antar render tanpa menyebabkan re-render

3. **Menyimpan nilai previous**:
   Menyimpan nilai sebelumnya dari suatu state

#### Contoh penggunaan:

```jsx
import React, { useRef, useEffect, useState } from 'react';

function TextInputWithFocusButton() {
  // 1. Mengakses DOM element
  const inputRef = useRef(null);
  
  const focusInput = () => {
    inputRef.current.focus();
  };

  // 2. Menyimpan nilai yang persistent
  const [count, setCount] = useState(0);
  const countRef = useRef(0);
  
  const incrementWithState = () => {
    setCount(count + 1); // Menyebabkan re-render
  };
  
  const incrementWithRef = () => {
    countRef.current += 1; // Tidak menyebabkan re-render
    console.log('Current ref value:', countRef.current);
  };
  
  // 3. Menyimpan nilai previous
  const prevCountRef = useRef();
  
  useEffect(() => {
    prevCountRef.current = count;
  }, [count]);
  
  return (
    <div>
      <input ref={inputRef} type="text" />
      <button onClick={focusInput}>Focus Input</button>
      
      <div>
        <p>State Count: {count}</p>
        <p>Previous State Count: {prevCountRef.current}</p>
        <button onClick={incrementWithState}>Increment State</button>
      </div>
      
      <div>
        <p>Ref Count (check console): {countRef.current}</p>
        <button onClick={incrementWithRef}>Increment Ref</button>
      </div>
    </div>
  );
}
```

---

## 2. Custom Hooks Development

Custom hooks adalah fungsi JavaScript yang dimulai dengan `use` dan dapat memanfaatkan hooks lain dari React. Mereka memungkinkan kita untuk mengekstrak logika komponen ke fungsi yang dapat digunakan kembali.

### Keuntungan Custom Hooks:

- **Reusability**: Menggunakan kembali logika antar komponen
- **Separation of Concerns**: Memisahkan logika dari tampilan UI
- **Clean Code**: Membuat komponen lebih ringkas dan fokus

### Contoh Basic Custom Hook:

```jsx
// 1. useToggle - untuk menangani toggle state (on/off)
import { useState } from 'react';

function useToggle(initialValue = false) {
  const [value, setValue] = useState(initialValue);
  
  const toggle = () => {
    setValue(prevValue => !prevValue);
  };
  
  return [value, toggle];
}

// Cara penggunaan:
function ToggleComponent() {
  const [isOn, toggleIsOn] = useToggle();
  
  return (
    <button onClick={toggleIsOn}>
      {isOn ? 'ON' : 'OFF'}
    </button>
  );
}
```

### Contoh Custom Hook untuk Data Fetching:

```jsx
import { useState, useEffect } from 'react';

function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);

  useEffect(() => {
    const fetchData = async () => {
      try {
        setLoading(true);
        const response = await fetch(url);
        
        if (!response.ok) {
          throw new Error(`HTTP error! Status: ${response.status}`);
        }
        
        const result = await response.json();
        setData(result);
        setError(null);
      } catch (err) {
        setError(err.message);
        setData(null);
      } finally {
        setLoading(false);
      }
    };

    fetchData();
  }, [url]);

  return { data, loading, error };
}

// Cara penggunaan:
function UserComponent() {
  const { data: user, loading, error } = useFetch('https://api.example.com/user/1');
  
  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error}</p>;
  
  return (
    <div>
      <h1>{user.name}</h1>
      <p>{user.email}</p>
    </div>
  );
}
```

### Custom Hook untuk Form:

```jsx
import { useState } from 'react';

function useForm(initialValues) {
  const [values, setValues] = useState(initialValues);
  
  const handleChange = (e) => {
    const { name, value } = e.target;
    setValues({
      ...values,
      [name]: value
    });
  };
  
  const resetForm = () => {
    setValues(initialValues);
  };
  
  return {
    values,
    handleChange,
    resetForm
  };
}

// Cara penggunaan:
function ContactForm() {
  const { values, handleChange, resetForm } = useForm({
    name: '',
    email: '',
    message: ''
  });
  
  const handleSubmit = (e) => {
    e.preventDefault();
    console.log('Form submitted with values:', values);
    resetForm();
  };
  
  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        name="name"
        value={values.name}
        onChange={handleChange}
        placeholder="Name"
      />
      <input
        type="email"
        name="email"
        value={values.email}
        onChange={handleChange}
        placeholder="Email"
      />
      <textarea
        name="message"
        value={values.message}
        onChange={handleChange}
        placeholder="Message"
      />
      <button type="submit">Submit</button>
    </form>
  );
}
```

---

## 3. Higher-Order Components

Higher-Order Component (HOC) adalah fungsi yang menerima sebuah komponen dan mengembalikan komponen baru dengan fungsionalitas tambahan.

### Keuntungan HOC:

- **Code Reuse**: Menggunakan kembali logika antar komponen
- **Separation of Concerns**: Memisahkan logika dari tampilan UI
- **Komposisi**: Dapat menggabungkan beberapa HOC

### Contoh Basic HOC:

```jsx
// HOC untuk menambahkan props extraData ke komponen
function withExtraData(WrappedComponent) {
  // Mengembalikan komponen baru
  return function WithExtraData(props) {
    const extraData = { message: "This is extra data from HOC" };
    
    // Menggabungkan props dan extraData
    return <WrappedComponent {...props} extraData={extraData} />;
  };
}

// Komponen original
function DisplayMessage({ message, extraData }) {
  return (
    <div>
      <p>Original message: {message}</p>
      <p>Extra data: {extraData.message}</p>
    </div>
  );
}

// Komponen yang sudah di-enhance dengan HOC
const EnhancedDisplayMessage = withExtraData(DisplayMessage);

// Penggunaan
function App() {
  return <EnhancedDisplayMessage message="Hello World!" />;
}
```

### HOC untuk Loading State:

```jsx
function withLoading(WrappedComponent) {
  return function WithLoading({ isLoading, ...props }) {
    if (isLoading) {
      return <div>Loading...</div>;
    }
    
    return <WrappedComponent {...props} />;
  };
}

// Komponen asli
function UserList({ users }) {
  return (
    <ul>
      {users.map(user => (
        <li key={user.id}>{user.name}</li>
      ))}
    </ul>
  );
}

// Komponen yang ditingkatkan
const UserListWithLoading = withLoading(UserList);

// Penggunaan
function App() {
  const [isLoading, setIsLoading] = useState(true);
  const [users, setUsers] = useState([]);
  
  useEffect(() => {
    // Fetch users
    fetch('https://api.example.com/users')
      .then(response => response.json())
      .then(data => {
        setUsers(data);
        setIsLoading(false);
      });
  }, []);
  
  return <UserListWithLoading isLoading={isLoading} users={users} />;
}
```

### HOC untuk Authentication:

```jsx
function withAuth(WrappedComponent) {
  return function WithAuth(props) {
    // Logika authentication
    const [isAuthenticated, setIsAuthenticated] = useState(false);
    
    // Cek apakah user terautentikasi
    useEffect(() => {
      const token = localStorage.getItem('token');
      setIsAuthenticated(!!token);
    }, []);
    
    // Jika tidak terautentikasi, redirect ke login
    if (!isAuthenticated) {
      return (
        <div>
          <p>Please login to view this page</p>
          <button onClick={() => console.log('Navigate to login')}>
            Login
          </button>
        </div>
      );
    }
    
    // Jika terautentikasi, render komponen yang di-wrap
    return <WrappedComponent {...props} />;
  };
}

// Komponen Dashboard yang memerlukan authentication
function Dashboard() {
  return <div>Welcome to your Dashboard!</div>;
}

// Dashboard dengan authentication
const AuthenticatedDashboard = withAuth(Dashboard);
```

---

## 4. Render Props Pattern

Render Props adalah pattern dimana sebuah komponen menerima fungsi sebagai prop yang merender apa yang akan ditampilkan komponen tersebut.

### Keuntungan Render Props:

- **Reusability**: Memungkinkan penggunaan ulang logika antar komponen
- **Flexibility**: Memberikan kontrol yang lebih besar kepada komponen parent
- **Composition**: Mudah dikombinasikan dengan pattern lain

### Contoh Basic Render Props:

```jsx
import React, { useState } from 'react';

// Komponen dengan Render Props
function Counter({ render }) {
  const [count, setCount] = useState(0);
  
  const increment = () => setCount(count + 1);
  const decrement = () => setCount(count - 1);
  
  // Memanggil fungsi render dengan data yang dibutuhkan
  return render({ count, increment, decrement });
}

// Penggunaan
function App() {
  return (
    <Counter
      render={({ count, increment, decrement }) => (
        <div>
          <h1>Count: {count}</h1>
          <button onClick={increment}>Increment</button>
          <button onClick={decrement}>Decrement</button>
        </div>
      )}
    />
  );
}
```

### Alternatif dengan Children sebagai Function:

```jsx
function Counter({ children }) {
  const [count, setCount] = useState(0);
  
  const increment = () => setCount(count + 1);
  const decrement = () => setCount(count - 1);
  
  // Memanggil children sebagai fungsi
  return children({ count, increment, decrement });
}

// Penggunaan
function App() {
  return (
    <Counter>
      {({ count, increment, decrement }) => (
        <div>
          <h1>Count: {count}</h1>
          <button onClick={increment}>Increment</button>
          <button onClick={decrement}>Decrement</button>
        </div>
      )}
    </Counter>
  );
}
```

### Mouse Position dengan Render Props:

```jsx
function MouseTracker({ render }) {
  const [position, setPosition] = useState({ x: 0, y: 0 });
  
  useEffect(() => {
    const handleMouseMove = (event) => {
      setPosition({
        x: event.clientX,
        y: event.clientY
      });
    };
    
    window.addEventListener('mousemove', handleMouseMove);
    
    return () => {
      window.removeEventListener('mousemove', handleMouseMove);
    };
  }, []);
  
  return render(position);
}

// Penggunaan
function App() {
  return (
    <div>
      <h1>Move your mouse around!</h1>
      <MouseTracker
        render={({ x, y }) => (
          <p>Current mouse position: ({x}, {y})</p>
        )}
      />
    </div>
  );
}
```

---

## 5. Compound Components

Compound Components adalah pattern yang memungkinkan kita membuat komponen yang bekerja sama untuk menyediakan state dan fungsionalitas bersama, namun tetap mempertahankan flexibilitas dalam komposisi tampilan.

### Keuntungan Compound Components:

- **Flexibilitas**: Memberikan kontrol lebih kepada developer dalam menentukan struktur komponen
- **Implicit State Sharing**: Component children dapat mengakses state tanpa prop drilling
- **Semantic API**: Membuat API komponen lebih intuitif dan mudah dibaca

### Contoh Compound Components:

```jsx
import React, { createContext, useContext, useState } from 'react';

// Buat context
const TabsContext = createContext();

// Komponen utama
function Tabs({ children, defaultIndex = 0 }) {
  const [activeIndex, setActiveIndex] = useState(defaultIndex);
  
  // Nilai yang dishare ke komponen lain
  const value = {
    activeIndex,
    setActiveIndex
  };
  
  return (
    <TabsContext.Provider value={value}>
      <div className="tabs">{children}</div>
    </TabsContext.Provider>
  );
}

// Sub komponen untuk Tab List
Tabs.List = function TabList({ children }) {
  return <div className="tabs-list">{children}</div>;
};

// Sub komponen untuk Tab
Tabs.Tab = function Tab({ children, index }) {
  const { activeIndex, setActiveIndex } = useContext(TabsContext);
  const isActive = activeIndex === index;
  
  return (
    <button
      className={`tab ${isActive ? 'active' : ''}`}
      onClick={() => setActiveIndex(index)}
    >
      {children}
    </button>
  );
};

// Sub komponen untuk Tab Panels
Tabs.Panels = function TabPanels({ children }) {
  return <div className="tabs-panels">{children}</div>;
};

// Sub komponen untuk Tab Panel
Tabs.Panel = function TabPanel({ children, index }) {
  const { activeIndex } = useContext(TabsContext);
  
  if (activeIndex !== index) return null;
  
  return <div className="tab-panel">{children}</div>;
};

// Penggunaan
function App() {
  return (
    <Tabs defaultIndex={0}>
      <Tabs.List>
        <Tabs.Tab index={0}>Tab 1</Tabs.Tab>
        <Tabs.Tab index={1}>Tab 2</Tabs.Tab>
        <Tabs.Tab index={2}>Tab 3</Tabs.Tab>
      </Tabs.List>
      
      <Tabs.Panels>
        <Tabs.Panel index={0}>Content for Tab 1</Tabs.Panel>
        <Tabs.Panel index={1}>Content for Tab 2</Tabs.Panel>
        <Tabs.Panel index={2}>Content for Tab 3</Tabs.Panel>
      </Tabs.Panels>
    </Tabs>
  );
}
```

### Contoh Dropdown dengan Compound Components:

```jsx
import React, { createContext, useContext, useState } from 'react';

const DropdownContext = createContext();

function Dropdown({ children }) {
  const [isOpen, setIsOpen] = useState(false);
  
  return (
    <DropdownContext.Provider value={{ isOpen, setIsOpen }}>
      <div className="dropdown">{children}</div>
    </DropdownContext.Provider>
  );
}

Dropdown.Toggle = function Toggle({ children }) {
  const { isOpen, setIsOpen } = useContext(DropdownContext);
  
  return (
    <button onClick={() => setIsOpen(!isOpen)}>
      {children}
    </button>
  );
};

Dropdown.Menu = function Menu({ children }) {
  const { isOpen } = useContext(DropdownContext);
  
  if (!isOpen) return null;
  
  return <div className="dropdown-menu">{children}</div>;
};

Dropdown.Item = function Item({ children, onClick }) {
  const { setIsOpen } = useContext(DropdownContext);
  
  const handleClick = () => {
    onClick?.();
    setIsOpen(false);
  };
  
  return (
    <div className="dropdown-item" onClick={handleClick}>
      {children}
    </div>
  );
};

// Penggunaan
function App() {
  return (
    <Dropdown>
      <Dropdown.Toggle>Options ▼</Dropdown.Toggle>
      <Dropdown.Menu>
        <Dropdown.Item onClick={() => console.log('Option 1 clicked')}>
          Option 1
        </Dropdown.Item>
        <Dropdown.Item onClick={() => console.log('Option 2 clicked')}>
          Option 2
        </Dropdown.Item>
        <Dropdown.Item onClick={() => console.log('Option 3 clicked')}>
          Option 3
        </Dropdown.Item>
      </Dropdown.Menu>
    </Dropdown>
  );
}
```

---

## 6. Control Props Pattern

Control Props Pattern adalah teknik dimana komponen dapat dikontrol sepenuhnya oleh parent component tetapi juga bisa berfungsi secara independen (uncontrolled).

### Keuntungan Control Props Pattern:

- **Flexibility**: Memberikan opsi untuk mengontrol state dari luar
- **Integration**: Memudahkan integrasi dengan form libraries
- **Uncontrolled Fallback**: Berfungsi dengan baik bahkan tanpa eksternal state

### Contoh Basic Control Props:

```jsx
import React, { useState } from 'react';

function Counter({ count: controlledCount, onChange }) {
  // Internal state untuk uncontrolled mode
  const [internalCount, setInternalCount] = useState(0);
  
  // Cek apakah komponen controlled atau uncontrolled
  const isControlled = controlledCount !== undefined;
  const count = isControlled ? controlledCount : internalCount;
  
  const handleIncrement = () => {
    if (isControlled) {
      // Jika controlled, panggil callback
      onChange?.(count + 1);
    } else {
      // Jika uncontrolled, update internal state
      setInternalCount(internalCount + 1);
    }
  };
  
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={handleIncrement}>Increment</button>
    </div>
  );
}

// Penggunaan sebagai Controlled Component
function ControlledExample() {
  const [count, setCount] = useState(0);
  
  return (
    <div>
      <h2>Controlled Counter:</h2>
      <Counter count={count} onChange={setCount} />
      <button onClick={() => setCount(0)}>Reset</button>
    </div>
  );
}

// Penggunaan sebagai Uncontrolled Component
function UncontrolledExample() {
  return (
    <div>
      <h2>Uncontrolled Counter:</h2>
      <Counter />
    </div>
  );
}
```

### Switch/Toggle Component dengan Control Props:

```jsx
import React, { useState } from 'react';

function Toggle({ checked: controlledChecked, onChange, defaultChecked = false }) {
  // Internal state untuk uncontrolled mode
  const [internalChecked, setInternalChecked] = useState(defaultChecked);
  
  // Cek apakah controlled atau uncontrolled
  const isControlled = controlledChecked !== undefined;
  const checked = isControlled ? controlledChecked : internalChecked;
  
  const handleChange = () => {
    if (isControlled) {
      // Jika controlled, panggil callback
      onChange?.(!checked);
    } else {
      // Jika uncontrolled, update internal state
      setInternalChecked(!internalChecked);
    }
  };
  
  return (
    <label className="toggle">
      <input
        type="checkbox"
        checked={checked}
        onChange={handleChange}
      />
      <span className="slider" />
    </label>
  );
}

// Penggunaan sebagai Controlled Component
function ControlledExample() {
  const [checked, setChecked] = useState(false);
  
  return (
    <div>
      <h2>Controlled Toggle:</h2>
      <Toggle checked={checked} onChange={setChecked} />
      <p>Status: {checked ? 'ON' : 'OFF'}</p>
      <button onClick={() => setChecked(!checked)}>
        Toggle from outside
      </button>
    </div>
  );
}

// Penggunaan sebagai Uncontrolled Component
function UncontrolledExample() {
  return (
    <div>
      <h2>Uncontrolled Toggle:</h2>
      <Toggle defaultChecked={true} />
    </div>
  );
}
```

---

## 7. Project: Library of Reusable Components

Untuk mengaplikasikan semua pattern yang telah dipelajari, Anda akan membuat library komponen React yang dapat digunakan kembali.

### Tujuan Project:

- Menerapkan semua pattern yang telah dipelajari
- Membuat komponen yang reusable, maintainable, dan extensible
- Membangun dokumentasi dan contoh penggunaan

### Komponen yang Akan Dibuat:

1. **Button Component**
   - Berbagai variant (primary, secondary, danger)
   - Berbagai ukuran
   - Support untuk icons

2. **Form Components**
   - Input dengan validasi
   - Select
   - Checkbox
   - Radio button
   - Form group

3. **Modal/Dialog**
   - Menggunakan compound components pattern
   - Support untuk berbagai ukuran dan animasi

4. **Tabs Component**
   - Menggunakan compound components pattern
   - Support untuk berbagai styles

5. **Dropdown Menu**
   - Menggunakan compound components pattern
   - Support untuk nested menus

6. **Pagination**
   - Menggunakan control props pattern
   - Customizable appearance

### Langkah-langkah Project:

1. **Setup Project**
   - Inisialisasi project React
   - Setup development environment
   - Setup testing library

2. **Desain Komponen**
   - Tentukan API dan perilaku komponen
   - Buat prototype UI

3. **Implementasi**
   - Bangun komponen menggunakan pattern yang tepat
   - Tulis unit tests untuk setiap komponen

4. **Dokumentasi**
   - Buat dokumentasi penggunaan
   - Buat contoh implementasi

5. **Publikasi**
   - Publish ke npm (opsional)
   - Share code di GitHub

### Tips Implementasi:

- Gunakan hooks yang tepat untuk setiap use case
- Pertimbangkan aksesibilitas (a11y) untuk setiap komponen
- Pastikan komponen berfungsi dengan baik di berbagai browser
- Pertimbangkan dukungan untuk server-side rendering

---

## Kesimpulan

Setelah menyelesaikan modul ini, Anda telah mempelajari beberapa pattern dan teknik lanjutan dalam pengembangan React:

1. **Advanced Hooks**: useCallback, useMemo, dan useRef untuk mengoptimalkan performa dan menangani side-effects
2. **Custom Hooks**: Untuk mengekstrak dan menggunakan kembali logika komponen
3. **Higher-Order Components**: Untuk meningkatkan komponen dengan fungsionalitas tambahan
4. **Render Props Pattern**: Untuk berbagi logika antar komponen dengan fleksibilitas
5. **Compound Components**: Untuk membuat API komponen yang intuitif dan fleksibel
6. **Control Props Pattern**: Untuk mengelola state komponen dengan fleksibilitas

Pattern-pattern ini akan membantu Anda membangun aplikasi React yang lebih maintainable, reusable, dan scalable. Dengan menguasai pattern ini, Anda dapat membuat komponen-komponen yang kompleks namun tetap mudah digunakan dan dikembangkan.

---

## Referensi Tambahan

- [React Hooks Documentation](https://reactjs.org/docs/hooks-intro.html)
- [React Patterns](https://reactpatterns.com/)
- [Advanced React Patterns](https://kentcdodds.com/blog/advanced-react-patterns)
- [React Hooks Cookbook](https://usehooks.com/)
- [Building a Design System with React](https://www.learnstorybook.com/design-systems-for-developers/)

# MODUL 8: PERFORMANCE OPTIMIZATION REACT

## Daftar Isi
- [Pendahuluan](#pendahuluan)
- [Minggu 1: Dasar-dasar Optimasi React](#minggu-1-dasar-dasar-optimasi-react)
  - [React Profiler & Chrome DevTools](#react-profiler--chrome-devtools)
  - [Code Splitting & Lazy Loading](#code-splitting--lazy-loading)
  - [React.memo dan PureComponent](#reactmemo-dan-purecomponent)
- [Minggu 2: Teknik Optimasi Lanjutan](#minggu-2-teknik-optimasi-lanjutan)
  - [Virtualization dengan React Window](#virtualization-dengan-react-window)
  - [Web Vitals Optimization](#web-vitals-optimization)
  - [Bundle Analysis dan Optimization](#bundle-analysis-dan-optimization)
- [Project: Optimasi Aplikasi React](#project-optimasi-aplikasi-react)
- [Referensi dan Sumber Belajar Tambahan](#referensi-dan-sumber-belajar-tambahan)

## Pendahuluan

Performance Optimization (optimasi performa) adalah proses meningkatkan kecepatan, responsifitas, dan efisiensi aplikasi React. Sebagai developer, penting untuk memastikan aplikasi kita tidak hanya berfungsi dengan benar tetapi juga berjalan dengan cepat dan efisien.

Mengapa optimasi performa penting?
- Pengalaman pengguna yang lebih baik
- Mengurangi bounce rate (tingkat pentalan) pengunjung
- Meningkatkan SEO (Search Engine Optimization)
- Mengurangi biaya hosting dan bandwidth
- Aplikasi yang lebih hemat daya baterai pada perangkat mobile

Dalam modul ini, kita akan mempelajari berbagai teknik untuk mengoptimalkan aplikasi React, mulai dari mengidentifikasi masalah performa hingga menerapkan solusi yang tepat.

## Minggu 1: Dasar-dasar Optimasi React

### React Profiler & Chrome DevTools

#### Apa itu React Profiler?

React Profiler adalah fitur bawaan React Developer Tools yang memungkinkan kita untuk mengukur seberapa sering aplikasi React melakukan rendering dan "biaya" (waktu) yang dibutuhkan untuk rendering.

#### Cara Menggunakan React Profiler:

1. **Instal React Developer Tools**
   
   React Developer Tools adalah ekstensi browser yang tersedia untuk Chrome dan Firefox.

   ```bash
   # Atau install melalui toko ekstensi browser
   ```

2. **Mengakses React Profiler**
   
   Setelah menginstal, buka DevTools browser (F12 atau klik kanan -> Inspect) dan pilih tab "Profiler".

3. **Merekam Performa**
   
   - Klik tombol "Record" (lingkaran merah)
   - Lakukan interaksi dengan aplikasi
   - Klik "Stop" untuk menghentikan perekaman

4. **Menganalisis Hasil**
   
   Profiler akan menampilkan "commit" (pembaruan) yang dilakukan oleh React. Untuk setiap commit, Anda dapat melihat:
   - Waktu yang dibutuhkan
   - Flame chart (diagram yang menunjukkan waktu rendering setiap komponen)
   - Ranked chart (komponen yang diurutkan berdasarkan waktu rendering)
   - Component chart (menampilkan berapa kali komponen di-render)

#### Chrome DevTools untuk React

Chrome DevTools memiliki beberapa fitur yang berguna untuk mengoptimasi aplikasi React:

1. **Performance Tab**
   
   Memungkinkan analisis mendalam terhadap performa halaman web, termasuk:
   - Waktu loading
   - JavaScript execution time
   - Layout dan render time
   - Memory usage

2. **Lighthouse**
   
   Alat audit dalam Chrome DevTools yang memberikan skor dan rekomendasi untuk:
   - Performance
   - Accessibility
   - Best Practices
   - SEO
   - Progressive Web App

3. **Memory Tab**
   
   Membantu mendeteksi memory leaks dengan:
   - Heap Snapshot (menganalisis memory usage saat ini)
   - Allocation Instrumentation (melacak alokasi objek JavaScript)

#### Contoh Penggunaan Performance Tab

```javascript
// Contoh kode yang bisa dianalisis
function SlowComponent() {
  // Lakukan operasi yang berat
  const startTime = performance.now();
  while (performance.now() - startTime < 100) {
    // Block thread selama 100ms (simulasi operasi berat)
  }
  
  return <div>Komponen yang lambat</div>;
}
```

Langkah analisis:
1. Buka Chrome DevTools -> Performance tab
2. Klik "Record"
3. Render komponen SlowComponent
4. Stop recording
5. Analisis hasilnya untuk melihat berapa lama JavaScript berjalan

### Code Splitting & Lazy Loading

#### Apa itu Code Splitting?

Code Splitting adalah teknik untuk memecah bundle JavaScript menjadi beberapa file yang lebih kecil, sehingga browser hanya perlu memuat kode yang dibutuhkan pada saat itu. Ini sangat membantu untuk aplikasi besar dengan banyak halaman.

#### Implementasi Code Splitting dengan React.lazy dan Suspense

React.lazy dan Suspense memungkinkan kita untuk melakukan code splitting dengan mudah:

```javascript
// Sebelum code splitting
import BigComponent from './BigComponent';

// Setelah code splitting
import React, { Suspense, lazy } from 'react';
const BigComponent = lazy(() => import('./BigComponent'));

function App() {
  return (
    <div>
      <Suspense fallback={<div>Loading...</div>}>
        <BigComponent />
      </Suspense>
    </div>
  );
}
```

#### Lazy Loading untuk Routes

Contoh penggunaan dengan React Router:

```javascript
import React, { Suspense, lazy } from 'react';
import { BrowserRouter as Router, Routes, Route } from 'react-router-dom';

// Lazy load komponen halaman
const Home = lazy(() => import('./routes/Home'));
const About = lazy(() => import('./routes/About'));
const Dashboard = lazy(() => import('./routes/Dashboard'));

function App() {
  return (
    <Router>
      <Suspense fallback={<div>Loading...</div>}>
        <Routes>
          <Route path="/" element={<Home />} />
          <Route path="/about" element={<About />} />
          <Route path="/dashboard" element={<Dashboard />} />
        </Routes>
      </Suspense>
    </Router>
  );
}
```

#### Dynamic Import untuk Komponen Besar

```javascript
import React, { useState } from 'react';

function App() {
  const [showChart, setShowChart] = useState(false);
  const [ChartComponent, setChartComponent] = useState(null);
  
  const loadChart = async () => {
    // Hanya muat komponen chart ketika dibutuhkan
    const module = await import('./HeavyChartComponent');
    setChartComponent(() => module.default);
    setShowChart(true);
  };
  
  return (
    <div>
      <button onClick={loadChart}>Tampilkan Chart</button>
      {showChart && ChartComponent && <ChartComponent />}
    </div>
  );
}
```

### React.memo dan PureComponent

#### Apa itu Rendering yang Tidak Perlu?

React akan me-render ulang komponen ketika:
- Props berubah
- State berubah
- Parent component di-render ulang

Namun, jika props dan state tidak berubah, seringkali tidak perlu me-render ulang komponen.

#### React.memo untuk Function Components

React.memo adalah higher-order component (HOC) yang memungkinkan kita untuk "memoize" komponen fungsi. Ini berarti React akan melewati proses rendering jika props tidak berubah.

```javascript
import React from 'react';

// Tanpa React.memo
function ExpensiveComponent(props) {
  console.log('Rendering ExpensiveComponent');
  // Komponen dengan kalkulasi yang berat
  return <div>{props.value}</div>;
}

// Dengan React.memo
const MemoizedExpensiveComponent = React.memo(function ExpensiveComponent(props) {
  console.log('Rendering ExpensiveComponent');
  // Komponen dengan kalkulasi yang berat
  return <div>{props.value}</div>;
});

// Penggunaan
function App() {
  const [count, setCount] = useState(0);
  return (
    <div>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <div>Count: {count}</div>
      {/* Akan selalu di-render ulang ketika count berubah */}
      <ExpensiveComponent value={42} />
      {/* Hanya di-render ulang jika value berubah */}
      <MemoizedExpensiveComponent value={42} />
    </div>
  );
}
```

#### PureComponent untuk Class Components

Untuk class components, kita dapat menggunakan PureComponent yang secara otomatis mengimplementasikan shouldComponentUpdate dengan shallow comparison terhadap props dan state.

```javascript
import React, { Component, PureComponent } from 'react';

// Regular Component
class RegularComponent extends Component {
  render() {
    console.log('Rendering RegularComponent');
    return <div>{this.props.value}</div>;
  }
}

// Pure Component
class OptimizedComponent extends PureComponent {
  render() {
    console.log('Rendering OptimizedComponent');
    return <div>{this.props.value}</div>;
  }
}
```

#### Custom Comparison dengan React.memo

Jika kita membutuhkan logika perbandingan yang lebih kompleks, kita bisa memberikan fungsi comparison custom ke React.memo:

```javascript
const MemoizedComponent = React.memo(
  function MyComponent(props) {
    /* render menggunakan props */
    return <div>{props.value}</div>;
  },
  (prevProps, nextProps) => {
    // Return true jika ingin mencegah re-render
    // Return false jika ingin memperbolehkan re-render
    
    // Contoh: hanya re-render jika nilai berubah lebih dari 5
    return Math.abs(prevProps.value - nextProps.value) <= 5;
  }
);
```

#### Memoizing Expensive Calculations dengan useMemo

Untuk kalkulasi yang berat, gunakan useMemo:

```javascript
import React, { useState, useMemo } from 'react';

function ExpensiveCalculation({ number }) {
  // Tanpa useMemo (akan dihitung ulang setiap render)
  const expensiveResult = calculateExpensiveValue(number);
  
  // Dengan useMemo (hanya dihitung ulang jika number berubah)
  const memoizedResult = useMemo(() => {
    return calculateExpensiveValue(number);
  }, [number]);
  
  return <div>Result: {memoizedResult}</div>;
}

function calculateExpensiveValue(number) {
  console.log('Calculating...');
  // Simulasi kalkulasi yang berat
  let result = 0;
  for (let i = 0; i < 1000000; i++) {
    result += number;
  }
  return result;
}
```

#### useCallback untuk Memoizing Functions

Untuk memoizing functions, gunakan useCallback:

```javascript
import React, { useState, useCallback } from 'react';

function ParentComponent() {
  const [count, setCount] = useState(0);
  
  // Tanpa useCallback (fungsi baru akan dibuat setiap render)
  const handleClick = () => {
    console.log('Clicked!');
  };
  
  // Dengan useCallback (fungsi yang sama akan digunakan kembali)
  const memoizedHandleClick = useCallback(() => {
    console.log('Clicked!');
  }, []); // Array dependency kosong berarti fungsi ini tidak akan pernah dibuat ulang
  
  return (
    <div>
      <button onClick={() => setCount(count + 1)}>Count: {count}</button>
      {/* Child akan selalu re-render karena handleClick selalu baru */}
      <ChildComponent onClick={handleClick} />
      {/* Child hanya re-render jika memoizedHandleClick berubah */}
      <MemoizedChildComponent onClick={memoizedHandleClick} />
    </div>
  );
}

const ChildComponent = React.memo(function ChildComponent(props) {
  console.log('Child rendering');
  return <button onClick={props.onClick}>Click me</button>;
});
```

## Minggu 2: Teknik Optimasi Lanjutan

### Virtualization dengan React Window

#### Apa itu Virtualization?

Virtualization adalah teknik untuk merender hanya item yang terlihat pada viewport, bukan seluruh daftar panjang. Ini sangat berguna untuk daftar dengan ribuan item.

#### Menggunakan React Window

React Window adalah library populer untuk virtualisasi di React.

Instalasi:
```bash
npm install react-window
# atau
yarn add react-window
```

Contoh penggunaan dasar:

```javascript
import React from 'react';
import { FixedSizeList as List } from 'react-window';

const ITEM_HEIGHT = 35; // Tinggi setiap item dalam pixel

function Row({ index, style }) {
  return (
    <div style={style}>
      Item {index}
    </div>
  );
}

function ExampleList({ items }) {
  return (
    <List
      height={400} // Tinggi viewport
      width={300} // Lebar list
      itemCount={items.length} // Jumlah total item
      itemSize={ITEM_HEIGHT} // Tinggi setiap item
    >
      {Row}
    </List>
  );
}

// Penggunaan:
function App() {
  // Simulasi daftar dengan 10,000 item
  const items = Array.from({ length: 10000 }, (_, i) => ({ id: i, text: `Item ${i}` }));
  
  return <ExampleList items={items} />;
}
```

#### FixedSizeList vs VariableSizeList

React Window menyediakan dua jenis list utama:

1. **FixedSizeList**: Untuk list dengan item berukuran sama
   ```javascript
   import { FixedSizeList } from 'react-window';
   
   <FixedSizeList
     height={400}
     width={300}
     itemCount={1000}
     itemSize={35}
   >
     {Row}
   </FixedSizeList>
   ```

2. **VariableSizeList**: Untuk list dengan item berukuran bervariasi
   ```javascript
   import { VariableSizeList } from 'react-window';
   
   // Function untuk menentukan tinggi item berdasarkan index
   const getItemSize = index => {
     return index % 2 === 0 ? 30 : 50; // Item genap: 30px, ganjil: 50px
   };
   
   <VariableSizeList
     height={400}
     width={300}
     itemCount={1000}
     itemSize={getItemSize}
   >
     {Row}
   </VariableSizeList>
   ```

#### Menggunakan dengan Data Kompleks

```javascript
import React from 'react';
import { FixedSizeList } from 'react-window';

// Data contoh
const users = Array.from({ length: 5000 }, (_, index) => ({
  id: index,
  name: `User ${index}`,
  email: `user${index}@example.com`,
  avatar: `https://randomuser.me/api/portraits/men/${index % 100}.jpg`
}));

// Komponen untuk setiap baris
function UserRow({ index, style }) {
  const user = users[index];
  
  return (
    <div style={{
      ...style,
      display: 'flex',
      alignItems: 'center',
      padding: '10px',
      borderBottom: '1px solid #eee'
    }}>
      <img 
        src={user.avatar} 
        alt={user.name}
        style={{ width: 40, height: 40, borderRadius: '50%', marginRight: 10 }}
      />
      <div>
        <div style={{ fontWeight: 'bold' }}>{user.name}</div>
        <div style={{ fontSize: '0.8em', color: '#666' }}>{user.email}</div>
      </div>
    </div>
  );
}

// Komponen list
function UserList() {
  return (
    <FixedSizeList
      height={500}
      width={400}
      itemCount={users.length}
      itemSize={60} // Tinggi setiap baris
    >
      {UserRow}
    </FixedSizeList>
  );
}
```

#### Infinite Loading dengan React Window

Menambahkan infinite loading:

```javascript
import React, { useState, useEffect } from 'react';
import { FixedSizeList } from 'react-window';
import InfiniteLoader from 'react-window-infinite-loader';

function InfiniteUserList() {
  const [users, setUsers] = useState([]);
  const [hasNextPage, setHasNextPage] = useState(true);
  const [isNextPageLoading, setIsNextPageLoading] = useState(false);
  
  // Simulasi loading data dari API
  const loadMoreItems = async (startIndex, stopIndex) => {
    setIsNextPageLoading(true);
    
    // Simulasi network request
    await new Promise(resolve => setTimeout(resolve, 1000));
    
    const newUsers = Array.from({ length: stopIndex - startIndex + 1 }, (_, i) => ({
      id: startIndex + i,
      name: `User ${startIndex + i}`,
      email: `user${startIndex + i}@example.com`
    }));
    
    setUsers(prevUsers => [...prevUsers, ...newUsers]);
    setIsNextPageLoading(false);
    
    // Simulasi akhir data setelah 500 item
    if (stopIndex >= 500) {
      setHasNextPage(false);
    }
  };
  
  // Item status: apakah sudah dimuat atau belum
  const isItemLoaded = index => index < users.length;
  
  // Render setiap item
  const Item = ({ index, style }) => {
    if (!isItemLoaded(index)) {
      return <div style={style}>Loading...</div>;
    }
    
    const user = users[index];
    return (
      <div style={style}>
        <div>{user.name}</div>
        <div>{user.email}</div>
      </div>
    );
  };
  
  return (
    <InfiniteLoader
      isItemLoaded={isItemLoaded}
      itemCount={hasNextPage ? users.length + 1 : users.length}
      loadMoreItems={loadMoreItems}
    >
      {({ onItemsRendered, ref }) => (
        <FixedSizeList
          height={400}
          width={300}
          itemCount={hasNextPage ? users.length + 1 : users.length}
          itemSize={50}
          onItemsRendered={onItemsRendered}
          ref={ref}
        >
          {Item}
        </FixedSizeList>
      )}
    </InfiniteLoader>
  );
}
```

### Web Vitals Optimization

#### Apa itu Web Vitals?

Web Vitals adalah inisiatif Google untuk menyediakan panduan terpadu tentang sinyal kualitas penting yang diperlukan untuk memberikan pengalaman pengguna yang baik di web.

#### Core Web Vitals

Ada tiga Core Web Vitals yang menjadi fokus utama:

1. **Largest Contentful Paint (LCP)**: Kecepatan loading
   - Mengukur waktu yang dibutuhkan untuk memuat konten terbesar yang terlihat
   - Target: < 2.5 detik

2. **First Input Delay (FID)**: Interaktivitas
   - Mengukur waktu dari interaksi pertama pengguna hingga browser dapat merespon
   - Target: < 100 ms

3. **Cumulative Layout Shift (CLS)**: Stabilitas visual
   - Mengukur seberapa banyak elemen halaman bergeser secara tidak terduga
   - Target: < 0.1

#### Mengukur Web Vitals

Kita dapat mengukur Web Vitals menggunakan:

1. **Lighthouse** (dalam Chrome DevTools)
2. **PageSpeed Insights**: https://pagespeed.web.dev/
3. **web-vitals library**

```bash
npm install web-vitals
# atau
yarn add web-vitals
```

```javascript
import { getCLS, getFID, getLCP } from 'web-vitals';

function sendToAnalytics(metric) {
  // Kirim data ke analytics
  console.log(metric);
}

getCLS(sendToAnalytics);
getFID(sendToAnalytics);
getLCP(sendToAnalytics);
```

#### Optimasi Largest Contentful Paint (LCP)

1. **Optimalkan Server Response Time**
   - Gunakan CDN
   - Implementasi caching server-side
   - Optimalkan database queries

2. **Preload Resource Penting**
   ```html
   <link rel="preload" href="critical-image.jpg" as="image" />
   ```

3. **Optimalkan dan Compress Gambar**
   - Gunakan format modern (WebP)
   - Gunakan lazy loading untuk gambar di bawah fold

4. **Minimalkan CSS yang Blocking**
   - Ekstrak CSS kritikal dan inlinekan
   - Defer CSS non-kritikal

#### Optimasi First Input Delay (FID)

1. **Minimalkan JavaScript yang Tidak Diperlukan**
   - Code splitting
   - Tree shaking
   - Lazy loading

2. **Break Up Long Tasks**
   ```javascript
   // Sebelum: Task yang panjang
   function processData() {
     for (let i = 0; i < 10000; i++) {
       // Operasi berat
     }
   }
   
   // Sesudah: Dipecah menjadi chunk-chunk kecil
   function processDataInChunks(i = 0) {
     // Proses hanya 100 item per waktu
     let end = Math.min(i + 100, 10000);
     
     for (let j = i; j < end; j++) {
       // Operasi berat
     }
     
     if (end < 10000) {
       // Jadwalkan chunk berikutnya
       setTimeout(() => processDataInChunks(end), 0);
     }
   }
   ```

3. **Gunakan Web Workers untuk Tugas Berat**
   ```javascript
   // main.js
   const worker = new Worker('worker.js');
   
   // Kirim data ke worker
   worker.postMessage({ data: complexData });
   
   // Terima hasil dari worker
   worker.onmessage = function(e) {
     console.log('Result:', e.data.result);
   };
   
   // worker.js
   self.onmessage = function(e) {
     // Lakukan kalkulasi berat di sini
     const result = doHeavyCalculation(e.data.data);
     
     // Kirim hasil kembali ke thread utama
     self.postMessage({ result });
   };
   ```

#### Optimasi Cumulative Layout Shift (CLS)

1. **Selalu Tentukan Dimensi Gambar**
   ```html
   <!-- Buruk: Tidak ada dimensi -->
   <img src="image.jpg" alt="Description">
   
   <!-- Baik: Ada dimensi -->
   <img src="image.jpg" width="640" height="360" alt="Description">
   ```

2. **Hindari Memasukkan Konten Dinamis di Atas Konten yang Sudah Ada**
   - Gunakan placeholder dengan ukuran yang tepat
   - Alokasikan space untuk iklan dan embeds

3. **Gunakan CSS transform untuk Animasi**
   ```css
   /* Buruk: Mengubah layout */
   .box:hover {
     margin-top: 20px;
   }
   
   /* Baik: Menggunakan transform */
   .box:hover {
     transform: translateY(20px);
   }
   ```

### Bundle Analysis dan Optimization

#### Menganalisis Bundle Size

Sebelum mengoptimasi bundle, kita perlu mengetahui apa yang menyebabkan bundle besar.

1. **webpack-bundle-analyzer**
   ```bash
   npm install --save-dev webpack-bundle-analyzer
   # atau
   yarn add --dev webpack-bundle-analyzer
   ```

   Konfigurasi untuk create-react-app:
   ```javascript
   // Buat file craco.config.js
   const BundleAnalyzerPlugin = require('webpack-bundle-analyzer').BundleAnalyzerPlugin;

   module.exports = {
     webpack: {
       plugins: {
         add: [
           new BundleAnalyzerPlugin({
             analyzerMode: 'server',
           }),
         ],
       },
     },
   };
   ```

2. **source-map-explorer**
   ```bash
   npm install --save-dev source-map-explorer
   # atau
   yarn add --dev source-map-explorer
   
   # Tambahkan script ke package.json
   "scripts": {
     "analyze": "source-map-explorer 'build/static/js/*.js'"
   }
   ```

#### Strategi Optimasi Bundle

1. **Mengurangi Ukuran Dependencies**
   - Gunakan [bundlephobia.com](https://bundlephobia.com/) untuk mencari alternativ package yang lebih kecil
   - Contoh: moment.js (329kB) vs date-fns (13kB) atau dayjs (2kB)

2. **Tree Shaking**
   
   Tree shaking adalah proses menghilangkan kode yang tidak digunakan dari bundle.

   ```javascript
   // Sebelum: Import seluruh lodash
   import _ from 'lodash';
   
   // Sesudah: Import hanya yang dibutuhkan
   import { debounce } from 'lodash-es';
   
   // Atau lebih baik lagi
   import debounce from 'lodash/debounce';
   ```

3. **Dynamic Imports**
   
   Selain untuk code splitting, dynamic imports juga mengurangi ukuran bundle awal.

   ```javascript
   // Sebelum
   import Chart from 'chart.js';
   
   function Dashboard() {
     return (
       <div>
         <h1>Dashboard</h1>
         <Chart data={...} />
       </div>
     );
   }
   
   // Sesudah
   function Dashboard() {
     const [Chart, setChart] = useState(null);
     
     useEffect(() => {
       import('chart.js').then(module => {
         setChart(() => module.default);
       });
     }, []);
     
     return (
       <div>
         <h1>Dashboard</h1>
         {Chart && <Chart data={...} />}
       </div>
     );
   }
   ```

4. **Optimasi Gambar dan Assets**
   - Compress gambar
   - Gunakan WebP untuk gambar
   - Sprite sheets untuk ikon
   - Minifikasi CSS dan JavaScript

5. **Mengurangi Polyfills**
   
   Jika tidak perlu mendukung browser lama, kurangi polyfills:

   ```javascript
   // Buat file .browserslistrc
   
   // Sebelum (mendukung banyak browser lama)
   > 0.5%
   last 2 versions
   Firefox ESR
   not dead
   
   // Sesudah (hanya browser modern)
   last 2 Chrome versions
   last 2 Firefox versions
   last 2 Edge versions
   last 2 Safari versions
   ```

6. **Menggunakan CDN untuk Libraries Besar**
   
   Untuk library besar, gunakan CDN dan externals:

   ```html
   <!-- Tambahkan di index.html -->
   <script src="https://unpkg.com/react@17/umd/react.production.min.js" crossorigin></script>
   <script src="https://unpkg.com/react-dom@17/umd/react-dom.production.min.js" crossorigin></script>
   ```

   ```javascript
   // Konfigurasi webpack
   module.exports = {
     //...
     externals: {
       'react': 'React',
       'react-dom': 'ReactDOM'
     }
   };
   ```

## Project: Optimasi Aplikasi React

### Tujuan Project

1. Mengidentifikasi dan memperbaiki masalah performa pada aplikasi React yang sudah ada
2. Menerapkan teknik optimasi yang telah dipelajari
3. Mengukur dampak optimasi yang dilakukan

### Langkah-langkah Project

#### 1. Analisis Awal

1. **Audit dengan Lighthouse**
   - Jalankan audit Lighthouse
   - Catat skor awal (Performance, Accessibility, Best Practices, SEO)
   - Identifikasi kesempatan perbaikan

2. **Profiling dengan React Profiler**
   - Identifikasi komponen yang sering di-render ulang
   - Catat waktu rendering setiap komponen
   - Identifikasi komponen yang membutuhkan waktu rendering lama

3. **Analisis Bundle Size**
   - Gunakan webpack-bundle-analyzer atau source-map-explorer
   - Identifikasi package/dependencies yang besar
   - Identifikasi code yang bisa di-split atau lazy load

#### 2. Implementasi Optimasi

1. **Optimasi Rendering**
   - Terapkan React.memo atau PureComponent untuk komponen yang sering di-render
   - Gunakan useMemo untuk kalkulasi berat
   - Gunakan useCallback untuk memoizing functions

2. **Code Splitting dan Lazy Loading**
   - Identifikasi bagian aplikasi yang bisa di-lazy load
   - Implementasikan React.lazy dan Suspense
   - Gunakan dynamic imports untuk komponen besar

3. **Virtualisasi untuk Daftar Panjang**
   - Implementasikan React Window untuk daftar dengan banyak item
   - Optimalkan rendering list yang kompleks

4. **Optimasi Bundle Size**
   - Kurangi size dependencies dengan alternative yang lebih kecil
   - Implementasikan tree shaking
   - Hapus dependencies yang tidak digunakan
   - Minifikasi assets (gambar, fonts, dll)

5. **Optimasi Web Vitals**
   - Perbaiki Largest Contentful Paint (LCP)
   - Tingkatkan First Input Delay (FID)
   - Minimalkan Cumulative Layout Shift (CLS)

#### 3. Pengukuran Hasil

1. **Ukur Ulang dengan Lighthouse**
   - Bandingkan skor sebelum dan sesudah optimasi
   - Dokumentasikan peningkatan

2. **Profiling Ulang dengan React Profiler**
   - Bandingkan waktu rendering sebelum dan sesudah optimasi
   - Catat komponen yang berhasil dioptimasi

3. **Analisis Bundle Size Ulang**
   - Bandingkan ukuran bundle sebelum dan sesudah optimasi
   - Dokumentasikan pengurangan ukuran

### Contoh Implementasi Project

Berikut adalah contoh kerangka implementasi untuk project optimasi aplikasi React:

#### 1. Identifikasi Masalah

```javascript
// Contoh komponen yang tidak optimal
function UserList({ users }) {
  // Tidak menggunakan virtualisasi
  return (
    <div>
      {users.map(user => (
        <UserCard key={user.id} user={user} />
      ))}
    </div>
  );
}

// Komponen yang di-render ulang meskipun props tidak berubah
function UserCard({ user }) {
  // Tidak menggunakan memoization
  return (
    <div className="user-card">
      <img src={user.avatar} alt={user.name} />
      <h3>{user.name}</h3>
      <p>{user.email}</p>
    </div>
  );
}
```

#### 2. Solusi Optimasi

```javascript
import React, { useMemo } from 'react';
import { FixedSizeList } from 'react-window';

// Optimasi dengan virtualisasi
function OptimizedUserList({ users }) {
  const Row = ({ index, style }) => {
    const user = users[index];
    return <MemoizedUserCard style={style} user={user} />;
  };

  return (
    <FixedSizeList
      height={500}
      width="100%"
      itemCount={users.length}
      itemSize={80}
    >
      {Row}
    </FixedSizeList>
  );
}

// Optimasi dengan memoization
const MemoizedUserCard = React.memo(function UserCard({ user, style }) {
  return (
    <div className="user-card" style={style}>
      <img src={user.avatar} alt={user.name} />
      <h3>{user.name}</h3>
      <p>{user.email}</p>
    </div>
  );
});

// Optimasi dengan useMemo untuk heavy calculations
function UserStats({ users }) {
  // Kalkulasi statistik yang berat
  const stats = useMemo(() => {
    console.log('Calculating stats...');
    return {
      totalUsers: users.length,
      activeUsers: users.filter(u => u.isActive).length,
      averageAge: users.reduce((acc, u) => acc + u.age, 0) / users.length
    };
  }, [users]); // Hanya hitung ulang jika users berubah

  return (
    <div className="stats">
      <div>Total Users: {stats.totalUsers}</div>
      <div>Active Users: {stats.activeUsers}</div>
      <div>Average Age: {stats.averageAge.toFixed(1)}</div>
    </div>
  );
}
```

#### 3. Implementasi Code Splitting

```javascript
// App.js sebelum
import React from 'react';
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import Home from './pages/Home';
import Dashboard from './pages/Dashboard';
import Analytics from './pages/Analytics';
import Settings from './pages/Settings';
import NotFound from './pages/NotFound';

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/dashboard" element={<Dashboard />} />
        <Route path="/analytics" element={<Analytics />} />
        <Route path="/settings" element={<Settings />} />
        <Route path="*" element={<NotFound />} />
      </Routes>
    </BrowserRouter>
  );
}

// App.js sesudah dengan code splitting
import React, { Suspense, lazy } from 'react';
import { BrowserRouter, Routes, Route } from 'react-router-dom';

// Eager load homepage untuk pengalaman awal yang lebih baik
import Home from './pages/Home';

// Lazy load halaman lainnya
const Dashboard = lazy(() => import('./pages/Dashboard'));
const Analytics = lazy(() => import('./pages/Analytics'));
const Settings = lazy(() => import('./pages/Settings'));
const NotFound = lazy(() => import('./pages/NotFound'));

function App() {
  return (
    <BrowserRouter>
      <Suspense fallback={<div className="loading-spinner">Loading...</div>}>
        <Routes>
          <Route path="/" element={<Home />} />
          <Route path="/dashboard" element={<Dashboard />} />
          <Route path="/analytics" element={<Analytics />} />
          <Route path="/settings" element={<Settings />} />
          <Route path="*" element={<NotFound />} />
        </Routes>
      </Suspense>
    </BrowserRouter>
  );
}
```

## Referensi dan Sumber Belajar Tambahan

### Dokumentasi Resmi
- [React Documentation: Optimizing Performance](https://reactjs.org/docs/optimizing-performance.html)
- [React Developer Tools](https://reactjs.org/blog/2019/08/15/new-react-devtools.html)
- [React.memo](https://reactjs.org/docs/react-api.html#reactmemo)
- [Code Splitting in React](https://reactjs.org/docs/code-splitting.html)
- [Web Vitals](https://web.dev/vitals/)

### Library dan Tools
- [React Window](https://github.com/bvaughn/react-window)
- [webpack-bundle-analyzer](https://github.com/webpack-contrib/webpack-bundle-analyzer)
- [source-map-explorer](https://github.com/danvk/source-map-explorer)
- [Lighthouse](https://developers.google.com/web/tools/lighthouse)
- [web-vitals library](https://github.com/GoogleChrome/web-vitals)

### Artikel dan Tutorial
- [A Complete Guide to useCallback](https://dmitripavlutin.com/react-usecallback/)
- [When to useMemo and useCallback](https://kentcdodds.com/blog/usememo-and-usecallback)
- [React Performance Optimization](https://medium.com/@ariklevliber/react-performance-optimization-techniques-in-2023-46a574f0d12a)
- [Understanding Tree Shaking](https://developers.google.com/web/fundamentals/performance/optimizing-javascript/tree-shaking)
- [The Ultimate Guide to Web Performance](https://developers.google.com/web/fundamentals/performance/get-started)

### Video Courses
- [Frontend Masters: React Performance](https://frontendmasters.com/courses/react-performance/)
- [Egghead.io: Optimize React Apps](https://egghead.io/courses/optimize-react-apps)
- [Pluralsight: React Performance Playbook](https://www.pluralsight.com/courses/react-performance-playbook)

---

Semoga modul ini membantu Anda memahami dan mengimplementasikan teknik-teknik optimasi performa pada aplikasi React. Ingat bahwa optimasi performa sebaiknya dilakukan setelah aplikasi berfungsi dengan benar, dan sebaiknya fokus pada perbaikan yang paling berdampak terlebih dahulu. Happy coding!
