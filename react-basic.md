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


# MODUL 2: PENGENALAN REACT (Minggu 2-3)

**Durasi**: 2 minggu  
**Tujuan**: Memahami konsep dasar React dan cara kerjanya

## Daftar Isi
1. [Apa itu React dan Virtual DOM](#1-apa-itu-react-dan-virtual-dom)
2. [Setting up React environment (Create React App)](#2-setting-up-react-environment-create-react-app)
3. [JSX Syntax](#3-jsx-syntax)
4. [Function Components vs Class Components](#4-function-components-vs-class-components)
5. [Props dan Component Composition](#5-props-dan-component-composition)
6. [Event Handling di React](#6-event-handling-di-react)
7. [Project: Konversi Landing Page ke React](#7-project-konversi-landing-page-ke-react)

---

## 1. Apa itu React dan Virtual DOM

### Pengenalan React

React adalah library JavaScript yang dikembangkan oleh Facebook (sekarang Meta) untuk membangun antarmuka pengguna (UI) yang interaktif dan efisien. Dirilis pada tahun 2013, React kini menjadi salah satu library frontend paling populer dan banyak digunakan oleh perusahaan-perusahaan besar seperti Netflix, Instagram, dan Airbnb.

#### Kelebihan React:

- **Component-Based**: UI dipecah menjadi komponen-komponen kecil yang reusable
- **Declarative**: Anda cukup mendeskripsikan UI dalam berbagai state, React akan otomatis memperbarui DOM saat data berubah
- **Learn Once, Write Anywhere**: Dapat digunakan untuk web (React), mobile (React Native), dan platform lainnya
- **Ekosistem yang besar**: Memiliki banyak library pendukung dan komunitas yang aktif

### Virtual DOM

Salah satu fitur utama React yang membuatnya sangat efisien adalah Virtual DOM.

#### Apa itu DOM?

DOM (Document Object Model) adalah representasi struktur HTML sebuah halaman web dalam bentuk pohon (tree) dari objek-objek. Browser menggunakan DOM untuk merender halaman web.

#### Masalah dengan manipulasi DOM langsung:

Memanipulasi DOM secara langsung bisa menjadi lambat, terutama pada aplikasi kompleks. Ketika satu elemen berubah, browser perlu merender ulang seluruh DOM.

#### Cara kerja Virtual DOM:

1. **Representasi Memori**: Virtual DOM adalah representasi ringan dari DOM asli yang disimpan dalam memori
2. **Proses Pembaruan**:
   - Saat state aplikasi berubah, React membuat Virtual DOM baru
   - React membandingkan (diffing) Virtual DOM baru dengan yang sebelumnya
   - React menghitung cara paling efisien untuk memperbarui DOM asli (reconciliation)
   - Kemudian hanya memperbarui bagian DOM asli yang berubah

#### Manfaat Virtual DOM:

- **Performa lebih baik**: Hanya memperbarui bagian yang berubah, bukan seluruh DOM
- **Proses rendering lebih efisien**: Manipulasi DOM digabungkan (batched) untuk mengurangi reflow dan repaint
- **Cross-browser compatibility**: React menangani perbedaan implementasi DOM antar browser

### React vs Framework lain

React sering disebut sebagai library, bukan framework. Perbedaannya:

- **Library**: Menyediakan fungsi-fungsi spesifik yang bisa digunakan dalam proyek (React fokus pada UI rendering)
- **Framework**: Lebih komprehensif, menyediakan struktur dan aturan untuk membangun aplikasi (seperti Angular atau Vue.js dengan router, state management dll)

React dapat dikombinasikan dengan library lain seperti React Router untuk routing dan Redux untuk state management.

---

## 2. Setting up React environment (Create React App)

### Node.js dan npm

Sebelum menggunakan React, pastikan komputer Anda sudah terinstal Node.js (termasuk npm - Node Package Manager). Node.js diperlukan untuk menjalankan JavaScript di sisi server dan npm untuk mengelola paket dan dependensi.

#### Cara menginstal Node.js dan npm:

1. Kunjungi [nodejs.org](https://nodejs.org/)
2. Download versi LTS (Long Term Support)
3. Ikuti instruksi instalasi
4. Verifikasi instalasi dengan menjalankan di terminal/command prompt:
   ```bash
   node -v
   npm -v
   ```

### Create React App

Create React App (CRA) adalah alat resmi yang dibuat oleh tim React untuk memudahkan pembuatan aplikasi React baru. CRA menyiapkan lingkungan pengembangan dengan konfigurasi dan struktur proyek yang sudah siap pakai.

#### Membuat proyek baru dengan Create React App:

1. Buka terminal atau command prompt
2. Jalankan perintah berikut:
   ```bash
   npx create-react-app nama-aplikasi-anda
   ```
3. Tunggu proses instalasi selesai
4. Pindah ke direktori proyek:
   ```bash
   cd nama-aplikasi-anda
   ```
5. Jalankan aplikasi:
   ```bash
   npm start
   ```
6. Aplikasi akan terbuka di browser pada `http://localhost:3000`

#### Struktur folder Create React App:

```
nama-aplikasi-anda/
  ├── node_modules/      # Folder berisi semua paket dependensi
  ├── public/            # File statis public, termasuk index.html
  │   ├── favicon.ico
  │   ├── index.html     # Template HTML utama
  │   └── manifest.json
  ├── src/               # Folder utama untuk kode aplikasi
  │   ├── App.css        # Styling untuk komponen App
  │   ├── App.js         # Komponen React utama
  │   ├── App.test.js    # Testing untuk App
  │   ├── index.css      # Styling global
  │   ├── index.js       # Entry point aplikasi
  │   ├── logo.svg
  │   └── serviceWorker.js
  ├── .gitignore         # File dan folder yang diabaikan git
  ├── package.json       # Daftar dependensi dan skrip
  └── README.md          # Dokumentasi dasar
```

#### Skrip npm yang tersedia:

- `npm start`: Menjalankan aplikasi dalam mode development
- `npm test`: Menjalankan test runner
- `npm run build`: Membuat build produksi untuk deployment
- `npm run eject`: Eject dari Create React App (tidak disarankan untuk pemula)

### Alternatif Create React App

Selain Create React App, ada beberapa alternatif untuk memulai proyek React:

- **Vite**: Build tool yang lebih cepat dan lebih ringan
- **Next.js**: Framework React dengan fitur server-side rendering
- **Gatsby**: Untuk membuat static site dengan React

Namun, untuk pemula, Create React App adalah cara termudah dan resmi untuk memulai.

---

## 3. JSX Syntax

### Apa itu JSX?

JSX (JavaScript XML) adalah ekstensi sintaks untuk JavaScript yang memungkinkan kita menulis struktur HTML dalam kode JavaScript. JSX terlihat seperti HTML tetapi sebenarnya adalah JavaScript.

```jsx
const element = <h1>Hello, world!</h1>;
```

Meskipun terlihat seperti HTML, JSX sebenarnya lebih dekat dengan JavaScript. Behind the scenes, Babel akan mengkompilasi JSX menjadi panggilan fungsi `React.createElement()`.

### Keuntungan menggunakan JSX:

- **Intuitif**: Memudahkan visualisasi UI dalam kode
- **Struktur yang jelas**: Hubungan parent-child terlihat jelas
- **Mudah untuk debugging**: Error message yang lebih jelas
- **Memudahkan pemisahan concern**: Menjaga logika rendering bersama dengan UI

### Aturan dasar JSX:

1. **Elemen harus ditutup**:
   ```jsx
   <img src="image.jpg" /> // Self-closing tag
   <div>Content</div> // Opening dan closing tag
   ```

2. **Hanya satu root element**: JSX harus memiliki satu elemen root (atau gunakan fragment)
   ```jsx
   // Benar
   return (
     <div>
       <h1>Title</h1>
       <p>Paragraph</p>
     </div>
   );
   
   // Atau dengan fragment
   return (
     <>
       <h1>Title</h1>
       <p>Paragraph</p>
     </>
   );
   
   // Salah
   return (
     <h1>Title</h1>
     <p>Paragraph</p>
   );
   ```

3. **Atribut menggunakan camelCase**: Kebanyakan atribut HTML ditulis dalam camelCase di JSX
   ```jsx
   <div className="container" onClick={handleClick}></div>
   ```

4. **JavaScript dalam JSX**: Gunakan curly braces `{}` untuk menyisipkan ekspresi JavaScript
   ```jsx
   const name = "John";
   return <h1>Hello, {name}!</h1>;
   ```

5. **Styling inline**: Menggunakan objek dan camelCase untuk properti CSS
   ```jsx
   <div style={{ backgroundColor: 'blue', marginTop: '10px' }}></div>
   ```

6. **Komentar**: Menggunakan sintaks komentar JavaScript dalam curly braces
   ```jsx
   <div>
     {/* Ini adalah komentar dalam JSX */}
     <p>Some text</p>
   </div>
   ```

### Expressions di JSX

Anda bisa menyisipkan ekspresi JavaScript di dalam JSX menggunakan curly braces `{}`:

```jsx
// Variabel
const name = "John";
return <p>Hello, {name}</p>;

// Operasi matematika
return <p>2 + 2 = {2 + 2}</p>;

// Pemanggilan fungsi
return <p>Random number: {Math.random()}</p>;

// Ternary operator (conditional rendering)
return <p>{isLoggedIn ? 'Welcome back!' : 'Please log in'}</p>;
```

### Rendering bersyarat (Conditional Rendering)

Ada beberapa cara untuk melakukan rendering bersyarat di React:

1. **If statement** di luar JSX
   ```jsx
   let content;
   if (isLoggedIn) {
     content = <UserGreeting />;
   } else {
     content = <GuestGreeting />;
   }
   return <div>{content}</div>;
   ```

2. **Ternary operator** di dalam JSX
   ```jsx
   return (
     <div>
       {isLoggedIn ? <UserGreeting /> : <GuestGreeting />}
     </div>
   );
   ```

3. **Logical AND operator** (`&&`) untuk render kondisional
   ```jsx
   return (
     <div>
       {isLoggedIn && <UserGreeting />}
     </div>
   );
   ```

### Rendering list

Untuk me-render list di React, gunakan `map()` untuk mengubah array menjadi element JSX:

```jsx
const numbers = [1, 2, 3, 4, 5];

return (
  <ul>
    {numbers.map((number) => (
      <li key={number}>{number}</li>
    ))}
  </ul>
);
```

**Penting**: Selalu tambahkan atribut `key` yang unik untuk setiap element dalam list. Key membantu React mengidentifikasi item mana yang berubah, ditambahkan, atau dihapus.

---

## 4. Function Components vs Class Components

Di React, ada dua cara utama untuk mendefinisikan komponen: Function Components (Komponen Fungsi) dan Class Components (Komponen Kelas).

### Function Components

Function components adalah cara modern dan lebih sederhana untuk mendefinisikan komponen React. Mereka hanyalah fungsi JavaScript yang menerima props sebagai parameter dan mengembalikan elemen React.

#### Syntax Function Component:

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

// Atau dengan arrow function
const Welcome = (props) => {
  return <h1>Hello, {props.name}</h1>;
};

// Penggunaan
<Welcome name="Sara" />
```

#### Kelebihan Function Components:

- **Sintaks lebih sederhana dan ringkas**
- **Lebih mudah dibaca dan ditulis**
- **Performa lebih baik** (dalam kebanyakan kasus)
- **Lebih mudah diuji (test)**
- **Tidak perlu memahami `this` keyword**
- **Dukungan untuk Hooks**, fitur modern React untuk state dan lifecycle

### Class Components

Class components adalah cara tradisional untuk mendefinisikan komponen di React. Mereka didefinisikan dengan class JavaScript yang meng-extend `React.Component`.

#### Syntax Class Component:

```jsx
import React, { Component } from 'react';

class Welcome extends Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}

// Penggunaan
<Welcome name="Sara" />
```

#### Kelebihan Class Components:

- **State bawaan** (internal state)
- **Lifecycle methods** (componentDidMount, componentDidUpdate, dll)
- **Bisa menggunakan metode class** (untuk logic tambahan)

### Perbandingan

#### State Management:

**Class Component:**
```jsx
class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }
  
  increment = () => {
    this.setState({ count: this.state.count + 1 });
  }
  
  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.increment}>Increment</button>
      </div>
    );
  }
}
```

**Function Component (dengan Hooks):**
```jsx
function Counter() {
  const [count, setCount] = useState(0);
  
  const increment = () => {
    setCount(count + 1);
  }
  
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}
```

#### Lifecycle Methods:

**Class Component:**
```jsx
class DataFetcher extends Component {
  constructor(props) {
    super(props);
    this.state = { data: null, loading: true };
  }
  
  componentDidMount() {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => this.setState({ data, loading: false }));
  }
  
  render() {
    const { data, loading } = this.state;
    return loading ? <p>Loading...</p> : <p>Data: {JSON.stringify(data)}</p>;
  }
}
```

**Function Component (dengan Hooks):**
```jsx
function DataFetcher() {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  
  useEffect(() => {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => {
        setData(data);
        setLoading(false);
      });
  }, []); // Empty dependency array = run once on mount (like componentDidMount)
  
  return loading ? <p>Loading...</p> : <p>Data: {JSON.stringify(data)}</p>;
}
```

### Rekomendasi Modern

Sejak diperkenalkannya Hooks di React 16.8 (2019), tim React merekomendasikan penggunaan Function Components dengan Hooks untuk kode baru. Class components masih didukung penuh, namun Function components dengan Hooks lebih ringkas, mudah dibaca, dan lebih sesuai dengan perkembangan React masa depan.

---

## 5. Props dan Component Composition

### Props (Properties)

Props adalah cara untuk meneruskan data dari komponen parent ke komponen child di React. Props bersifat read-only dan tidak dapat diubah oleh komponen yang menerimanya.

#### Cara mengirim Props:

```jsx
// Parent Component
function App() {
  return <Welcome name="Sara" age={25} isAdmin={true} />;
}
```

#### Cara menerima Props di Function Component:

```jsx
// Child Component
function Welcome(props) {
  return (
    <div>
      <h1>Hello, {props.name}</h1>
      <p>Age: {props.age}</p>
      <p>{props.isAdmin ? 'Admin User' : 'Regular User'}</p>
    </div>
  );
}

// Dengan destructuring untuk lebih ringkas
function Welcome({ name, age, isAdmin }) {
  return (
    <div>
      <h1>Hello, {name}</h1>
      <p>Age: {age}</p>
      <p>{isAdmin ? 'Admin User' : 'Regular User'}</p>
    </div>
  );
}
```

#### Cara menerima Props di Class Component:

```jsx
class Welcome extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, {this.props.name}</h1>
        <p>Age: {this.props.age}</p>
        <p>{this.props.isAdmin ? 'Admin User' : 'Regular User'}</p>
      </div>
    );
  }
}
```

### Default Props

Anda bisa menetapkan nilai default untuk props jika tidak diberikan:

```jsx
// Function component
function Welcome({ name = 'Guest' }) {
  return <h1>Hello, {name}</h1>;
}

// Atau
Welcome.defaultProps = {
  name: 'Guest'
};

// Class component
class Welcome extends React.Component {
  static defaultProps = {
    name: 'Guest'
  };
  
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

### PropTypes untuk Type Checking

React menyediakan library PropTypes untuk verifikasi tipe pada props. Ini sangat membantu untuk debugging dan dokumentasi:

```jsx
import PropTypes from 'prop-types';

function Welcome({ name, age }) {
  return (
    <div>
      <h1>Hello, {name}</h1>
      <p>Age: {age}</p>
    </div>
  );
}

Welcome.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number
};
```

### Component Composition

Component Composition adalah pola di React untuk membangun komponen kompleks dari komponen yang lebih sederhana. Ini adalah salah satu prinsip utama React: membangun UI dari potongan-potongan kecil yang dapat digunakan kembali.

#### Containment:

Menggunakan `children` prop untuk "menyuntikkan" konten ke dalam komponen:

```jsx
// Generic container component
function Card({ title, children }) {
  return (
    <div className="card">
      <div className="card-header">{title}</div>
      <div className="card-body">
        {children}
      </div>
    </div>
  );
}

// Penggunaan
function App() {
  return (
    <Card title="Welcome">
      <h1>Hello, world!</h1>
      <p>This is a paragraph inside the card.</p>
    </Card>
  );
}
```

#### Specialization:

Membuat komponen khusus dari komponen yang lebih generik:

```jsx
// Generic component
function Button({ children, onClick, className }) {
  return (
    <button onClick={onClick} className={`btn ${className}`}>
      {children}
    </button>
  );
}

// Specialized components
function PrimaryButton({ children, onClick }) {
  return (
    <Button onClick={onClick} className="btn-primary">
      {children}
    </Button>
  );
}

function DangerButton({ children, onClick }) {
  return (
    <Button onClick={onClick} className="btn-danger">
      {children}
    </Button>
  );
}

// Penggunaan
function App() {
  return (
    <div>
      <PrimaryButton onClick={() => console.log('Saved')}>
        Save
      </PrimaryButton>
      <DangerButton onClick={() => console.log('Deleted')}>
        Delete
      </DangerButton>
    </div>
  );
}
```

### Komposisi vs Inheritance

React sangat menekankan pada komposisi daripada inheritance untuk membangun komponen yang reusable. Hampir semua kasus penggunaan inheritance dapat diatasi dengan komposisi komponen dengan lebih baik.

```jsx
// Menghindari inheritance complex
class SpecializedComponent extends BaseComponent {
  // ...kompleks, sulit dimengerti
}

// Lebih baik menggunakan komposisi
function SpecializedComponent() {
  return (
    <BaseComponent>
      <CustomContent />
    </BaseComponent>
  );
}
```

---

## 6. Event Handling di React

Event handling di React mirip dengan event handling di HTML, tetapi dengan beberapa perbedaan sintaks.

### Perbedaan dengan HTML tradisional:

1. Nama event menggunakan camelCase
   ```jsx
   // HTML: onclick, onchange
   // React: onClick, onChange
   ```

2. Meneruskan fungsi (bukan string) sebagai event handler
   ```jsx
   // HTML
   <button onclick="handleClick()">Click me</button>
   
   // React
   <button onClick={handleClick}>Click me</button>
   ```

3. Mencegah perilaku default dengan `preventDefault()` secara eksplisit
   ```jsx
   // HTML
   <a href="#" onclick="console.log('Clicked'); return false;">Click</a>
   
   // React
   function handleClick(e) {
     e.preventDefault();
     console.log('Clicked');
   }
   
   <a href="#" onClick={handleClick}>Click</a>
   ```

### Cara mendefinisikan event handler:

#### Di Function Component:

```jsx
function Button() {
  const handleClick = (e) => {
    console.log('Button clicked');
    console.log(e); // Event object
  };
  
  return <button onClick={handleClick}>Click me</button>;
}

// Atau langsung inline
function Button() {
  return <button onClick={() => console.log('Button clicked')}>Click me</button>;
}
```

#### Di Class Component:

```jsx
class Button extends React.Component {
  handleClick = (e) => {
    console.log('Button clicked');
    console.log(e); // Event object
  }
  
  render() {
    return <button onClick={this.handleClick}>Click me</button>;
  }
}
```

### Binding di Class Component

Perhatikan bahwa di class component, kita menggunakan arrow function (`handleClick = (e) => {...}`) untuk mendefinisikan method. Ini penting untuk mengikat `this` dengan benar.

Alternatif lain untuk binding:

```jsx
class Button extends React.Component {
  constructor(props) {
    super(props);
    // Bind di constructor
    this.handleClick = this.handleClick.bind(this);
  }
  
  handleClick(e) {
    console.log('Button clicked');
  }
  
  render() {
    return <button onClick={this.handleClick}>Click me</button>;
  }
}
```

### Mengirim Parameter ke Event Handler:

```jsx
function ItemList() {
  const deleteItem = (id) => {
    console.log(`Deleting item ${id}`);
  };
  
  return (
    <ul>
      <li>
        Item 1
        <button onClick={() => deleteItem(1)}>Delete</button>
      </li>
      <li>
        Item 2
        <button onClick={() => deleteItem(2)}>Delete</button>
      </li>
    </ul>
  );
}
```

### Jenis Event yang Umum Digunakan:

1. **Click events**:
   ```jsx
   <button onClick={handleClick}>Click Me</button>
   ```

2. **Form events**:
   ```jsx
   <form onSubmit={handleSubmit}>
     <input type="text" value={value} onChange={handleChange} />
     <button type="submit">Submit</button>
   </form>
   ```

3. **Keyboard events**:
   ```jsx
   <input onKeyDown={handleKeyDown} />
   ```

4. **Focus events**:
   ```jsx
   <input onFocus={handleFocus} onBlur={handleBlur} />
   ```

5. **Mouse events**:
   ```jsx
   <div 
     onMouseEnter={handleMouseEnter}
     onMouseLeave={handleMouseLeave}
   >
     Hover me
   </div>
   ```

### Event Bubbling (Gelembung Event)

Event di React mengikuti sistem propagasi yang sama dengan DOM biasa, di mana event "bubble up" dari anak ke parent.

```jsx
function Parent() {
  const handleParentClick = () => {
    console.log('Parent clicked');
  };
  
  const handleChildClick = (e) => {
    e.stopPropagation(); // Mencegah event bubbling
    console.log('Child clicked');
  };
  
  return (
    <div onClick={handleParentClick} style={{ padding: '20px', background: 'lightgray' }}>
      Parent
      <button onClick={handleChildClick}>Child</button>
    </div>
  );
}
```

### Synthetic Events

React membungkus event native browser dalam sebuah wrapper yang disebut SyntheticEvent untuk memastikan konsistensi lintas browser. SyntheticEvent memiliki antarmuka yang sama dengan event native browser, tetapi bekerja secara identik di semua browser.

```jsx
function Button() {
  const handleClick = (e) => {
    console.log(e); // SyntheticEvent object
    console.log(e.nativeEvent); // Underlying native browser event
  };
  
  return <button onClick={handleClick}>Click me</button>;
}
```

### Best Practices Event Handling:

1. **Gunakan nama yang deskriptif** untuk handler (`handleClick`, `handleSubmit`, dll.)
2. **Batasi inline functions** di JSX untuk performa yang lebih baik
3. **Dekonstruksi props** untuk event handler yang diteruskan
4. **Selalu handle errors** dalam event handlers
5. **Validasi data** sebelum melakukan tindakan

---

## 7. Project: Konversi Landing Page ke React

Sebagai proyek untuk memantapkan pemahaman Anda tentang React, kita akan mengkonversi landing page dari HTML dan CSS biasa ke React. Ini akan membantu Anda memahami cara berpikir dalam "React way" dan memecah UI menjadi komponen-komponen.

### Tahapan Konversi:

#### 1. Analisis dan Pecah UI menjadi Hierarki Komponen

Langkah pertama adalah menganalisis design landing page dan memecahnya menjadi komponen-komponen yang logis.

Contoh hierarki komponen untuk landing page sederhana:
- `<App />` (root component)
  - `<Header />` (logo, navigation, mungkin call-to-action)
  - `<Hero />` (banner utama dengan headline dan CTA)
  - `<Features />` (section fitur-fitur)
    - `<FeatureCard />` (komponen untuk setiap fitur)
  - `<Testimonials />` (section testimonial)
    - `<TestimonialCard />` (komponen untuk setiap testimonial)
  - `<Pricing />` (section pricing jika ada)
    - `<PricingCard />` (komponen untuk setiap paket)
  - `<Contact />` atau `<Newsletter />` (section untuk form kontak)
  - `<Footer />` (footer dengan links, copyright, dll)

#### 2. Setup Proyek React

```bash
npx create-react-app landing-page-react
cd landing-page-react
npm start
```

#### 3. Buat Struktur Folder

Organisasi kode yang baik:

```
src/
  ├── components/           # Folder untuk semua komponen
  │   ├── Header/          
  │   │   ├── Header.js    # Component code
  │   │   ├── Header.css   # Component-specific styling
  │   │   └── index.js     # Export file (optional)
  │   ├── Hero/
  │   ├── Features/
  │   └── ...
  ├── assets/               # Images, fonts, etc.
  ├── App.js                # Root component
  ├── App.css               # Global styles
  └── index.js              # Entry point
```

#### 4. Buat Static Version Terlebih Dahulu

Mulai dengan membuat versi statis tanpa interaktivitas. Fokus pada struktur komponen dan styling.

Contoh untuk Header component:

```jsx
// src/components/Header/Header.js
import React from 'react';
import './Header.css';
import logo from '../../assets/logo.png';

function Header() {
  return (
    <header className="header">
      <div className="logo-container">
        <img src={logo} alt="Company Logo" className="logo" />
      </div>
      <nav className="nav">
        <ul className="nav-list">
          <li className="nav-item"><a href="#features">Features</a></li>
          <li className="nav-item"><a href="#testimonials">Testimonials</a></li>
          <li className="nav-item"><a href="#pricing">Pricing</a></li>
          <li className="nav-item"><a href="#contact">Contact</a></li>
        </ul>
      </nav>
      <button className="cta-button">Get Started</button>
    </header>
  );
}

export default Header;
```

```css
/* src/components/Header/Header.css */
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background-color: #fff;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.logo {
  height: 40px;
}

.nav-list {
  display: flex;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-item {
  margin: 0 1rem;
}

.nav-item a {
  text-decoration: none;
  color: #333;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-item a:hover {
  color: #0070f3;
}

.cta-button {
  background-color: #0070f3;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.cta-button:hover {
  background-color: #0051cc;
}
```

Contoh untuk Feature Card component:

```jsx
// src/components/Features/FeatureCard.js
import React from 'react';
import './FeatureCard.css';

function FeatureCard({ icon, title, description }) {
  return (
    <div className="feature-card">
      <div className="feature-icon">{icon}</div>
      <h3 className="feature-title">{title}</h3>
      <p className="feature-description">{description}</p>
    </div>
  );
}

export default FeatureCard;
```

```css
/* src/components/Features/FeatureCard.css */
.feature-card {
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  padding: 2rem;
  margin: 1rem;
  transition: transform 0.3s ease;
  text-align: center;
}

.feature-card:hover {
  transform: translateY(-5px);
}

.feature-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  color: #0070f3;
}

.feature-title {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.feature-description {
  color: #666;
  line-height: 1.6;
}
```

#### 5. Tambahkan Interaktivitas

Setelah versi statis selesai, mulai tambahkan interaktivitas sesuai kebutuhan, seperti:

- Dropdown menu pada navigasi mobile
- Form validations
- Image sliders
- Modal popups
- Smooth scrolling ke section

Contoh navigasi mobile dengan toggle:

```jsx
// src/components/Header/Header.js dengan toggle untuk mobile
import React, { useState } from 'react';
import './Header.css';
import logo from '../../assets/logo.png';

function Header() {
  const [menuOpen, setMenuOpen] = useState(false);
  
  const toggleMenu = () => {
    setMenuOpen(!menuOpen);
  };
  
  return (
    <header className="header">
      <div className="logo-container">
        <img src={logo} alt="Company Logo" className="logo" />
      </div>
      
      <div className="menu-toggle" onClick={toggleMenu}>
        <div className={`hamburger ${menuOpen ? 'open' : ''}`}>
          <span></span>
          <span></span>
          <span></span>
        </div>
      </div>
      
      <nav className={`nav ${menuOpen ? 'open' : ''}`}>
        <ul className="nav-list">
          <li className="nav-item"><a href="#features">Features</a></li>
          <li className="nav-item"><a href="#testimonials">Testimonials</a></li>
          <li className="nav-item"><a href="#pricing">Pricing</a></li>
          <li className="nav-item"><a href="#contact">Contact</a></li>
        </ul>
      </nav>
      <button className="cta-button">Get Started</button>
    </header>
  );
}

export default Header;
```

Tambahan CSS untuk mobile menu:

```css
/* Add to Header.css */
.menu-toggle {
  display: none; /* Hidden on desktop */
}

@media (max-width: 768px) {
  .header {
    flex-wrap: wrap;
  }
  
  .menu-toggle {
    display: block;
    cursor: pointer;
  }
  
  .hamburger {
    width: 30px;
    height: 22px;
    position: relative;
  }
  
  .hamburger span {
    display: block;
    height: 3px;
    width: 100%;
    background: #333;
    position: absolute;
    transition: all 0.3s ease;
  }
  
  .hamburger span:nth-child(1) {
    top: 0;
  }
  
  .hamburger span:nth-child(2) {
    top: 9px;
  }
  
  .hamburger span:nth-child(3) {
    top: 18px;
  }
  
  .hamburger.open span:nth-child(1) {
    transform: rotate(45deg);
    top: 9px;
  }
  
  .hamburger.open span:nth-child(2) {
    opacity: 0;
  }
  
  .hamburger.open span:nth-child(3) {
    transform: rotate(-45deg);
    top: 9px;
  }
  
  .nav {
    width: 100%;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease;
  }
  
  .nav.open {
    max-height: 300px;
  }
  
  .nav-list {
    flex-direction: column;
    width: 100%;
  }
  
  .nav-item {
    margin: 0.5rem 0;
  }
  
  .cta-button {
    margin-top: 1rem;
  }
}
```

#### 6. Prop Drilling dan Komposisi Komponen

Saat aplikasi bertambah kompleks, gunakan props untuk meneruskan data ke komponen-komponen yang membutuhkannya.

```jsx
// src/components/Features/Features.js
import React from 'react';
import FeatureCard from './FeatureCard';
import { FaRocket, FaLock, FaClock } from 'react-icons/fa'; // Gunakan react-icons
import './Features.css';

function Features() {
  const featuresData = [
    {
      id: 1,
      icon: <FaRocket />,
      title: 'Lightning Fast',
      description: 'Our solution is optimized for speed and performance.'
    },
    {
      id: 2,
      icon: <FaLock />,
      title: 'Secure by Design',
      description: 'Built with security in mind at every level.'
    },
    {
      id: 3,
      icon: <FaClock />,
      title: 'Time Saving',
      description: 'Save hours of work with our automation tools.'
    }
  ];
  
  return (
    <section id="features" className="features-section">
      <h2 className="section-title">Our Features</h2>
      <div className="features-container">
        {featuresData.map(feature => (
          <FeatureCard 
            key={feature.id}
            icon={feature.icon}
            title={feature.title}
            description={feature.description}
          />
        ))}
      </div>
    </section>
  );
}

export default Features;
```

#### 7. App Assembly

Akhirnya, gabungkan semua komponen dalam App.js:

```jsx
// src/App.js
import React from 'react';
import Header from './components/Header/Header';
import Hero from './components/Hero/Hero';
import Features from './components/Features/Features';
import Testimonials from './components/Testimonials/Testimonials';
import Contact from './components/Contact/Contact';
import Footer from './components/Footer/Footer';
import './App.css';

function App() {
  return (
    <div className="App">
      <Header />
      <Hero 
        title="Modern Web Solutions"
        subtitle="Build beautiful, responsive websites with ease"
        ctaText="Get Started"
      />
      <Features />
      <Testimonials />
      <Contact />
      <Footer />
    </div>
  );
}

export default App;
```

### Tips untuk Konversi HTML/CSS ke React:

1. **Mulai dengan struktur**: Identifikasi bagian-bagian yang dapat dijadikan komponen
2. **Kode CSS**: Pindahkan CSS ke file terpisah untuk setiap komponen
3. **Assets**: Pindahkan gambar dan aset ke folder assets dan import sesuai kebutuhan
4. **Inline styles**: Ubah inline styles menjadi objek style React atau class
5. **Event handlers**: Ubah atribut event HTML menjadi event handlers React
6. **Form elements**: Ubah form elements jadi controlled components
7. **Components**: Pikirkan reusability — buat komponen generik yang dapat digunakan kembali

### Challenge dan Extensions:

1. **Buat landing page responsive** untuk semua ukuran layar
2. **Implementasikan dark mode** dengan context API
3. **Tambahkan animasi** dengan CSS transitions atau library seperti Framer Motion
4. **Buat form contact yang functional** dengan validasi
5. **Implementasikan lazy loading** untuk gambar atau komponen
6. **Tambahkan routing** dengan React Router untuk halaman multi-page

---

Dengan menyelesaikan proyek ini, Anda akan memperoleh pemahaman praktis tentang cara mengimplementasikan React dalam situasi nyata. Konversi dari HTML/CSS ke React akan membantu Anda memahami perbedaan pendekatan antara pengembangan web tradisional dengan model komponen React yang modular dan maintainable.

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
# MODUL 3: REACT FUNDAMENTALS

**Durasi**: 3 minggu  
**Tujuan**: Menguasai konsep state, lifecycle, dan rendering di React

## Daftar Isi
1. [Pendahuluan](#pendahuluan)
2. [React Hooks: useState dan useEffect](#react-hooks-usestate-dan-useeffect)
3. [Conditional Rendering](#conditional-rendering)
4. [Lists dan Keys](#lists-dan-keys)
5. [Forms dan Controlled Components](#forms-dan-controlled-components)
6. [Styling di React](#styling-di-react)
7. [Component Lifecycle](#component-lifecycle)
8. [Project: To-Do List Application](#project-to-do-list-application)

## Pendahuluan

React adalah library JavaScript yang dikembangkan oleh Facebook untuk membangun antarmuka pengguna (UI) yang interaktif. React menggunakan konsep "Component-Based Architecture" yang memungkinkan kita membangun UI kompleks dari komponen-komponen kecil yang dapat digunakan kembali.

Pada modul ini, kita akan mempelajari konsep fundamental React yang akan membantu kita membangun aplikasi web dinamis dan responsif.

## React Hooks: useState dan useEffect

### useState Hook

`useState` adalah hook paling dasar di React yang memungkinkan kita menambahkan state pada functional component.

**Pengertian State**: State adalah data yang disimpan di dalam komponen dan dapat berubah seiring waktu, mempengaruhi tampilan UI.

**Syntax dasar**:

```jsx
import React, { useState } from 'react';

function Counter() {
  // [variabelState, functionUntukUpdate] = useState(nilaiAwal)
  const [count, setCount] = useState(0);
  
  return (
    <div>
      <p>Anda sudah klik sebanyak {count} kali</p>
      <button onClick={() => setCount(count + 1)}>
        Klik saya
      </button>
    </div>
  );
}
```

**Penjelasan**:
- `useState(0)` menginisialisasi state dengan nilai awal 0
- Fungsi ini mengembalikan array dengan 2 elemen:
  1. Variabel state saat ini (`count`)
  2. Fungsi untuk mengupdate state tersebut (`setCount`)
- Setiap kali `setCount` dipanggil, komponen akan di-render ulang dengan nilai state yang baru

### useEffect Hook

`useEffect` memungkinkan kita melakukan "side effects" dalam functional component, seperti mengambil data dari API, berlangganan event, atau memanipulasi DOM secara langsung.

**Syntax dasar**:

```jsx
import React, { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // useEffect(fungsiEffect, [dependencyArray])
  useEffect(() => {
    // Kode yang dijalankan setelah render
    document.title = `Anda klik ${count} kali`;
    
    // Cleanup function (opsional)
    return () => {
      // Kode untuk membersihkan efek
      document.title = 'React App';
    };
  }, [count]); // Array dependencies
  
  return (
    <div>
      <p>Anda sudah klik sebanyak {count} kali</p>
      <button onClick={() => setCount(count + 1)}>
        Klik saya
      </button>
    </div>
  );
}
```

**Penjelasan**:
- `useEffect` menerima 2 parameter:
  1. Fungsi yang berisi efek yang ingin dijalankan
  2. Array dependencies (opsional)
- Array dependencies menentukan kapan effect akan dijalankan kembali:
  - Jika kosong `[]`: effect hanya dijalankan sekali saat mounting (mirip `componentDidMount`)
  - Jika berisi variabel `[count]`: effect dijalankan saat mounting dan saat nilai `count` berubah
  - Jika tidak ada array: effect dijalankan setiap kali komponen di-render

**Kasus penggunaan umum**:
1. Mengambil data dari API
2. Berlangganan pada event eksternal
3. Manipulasi DOM secara langsung
4. Logging dan analytics

## Conditional Rendering

Conditional rendering adalah teknik untuk menampilkan konten berbeda berdasarkan kondisi tertentu, mirip dengan pengkondisian pada JavaScript biasa.

### Menggunakan operator ternary

```jsx
function Greeting({ isLoggedIn }) {
  return (
    <div>
      {isLoggedIn 
        ? <h1>Selamat datang kembali!</h1>
        : <h1>Silakan login terlebih dahulu</h1>
      }
    </div>
  );
}
```

### Menggunakan operator &&

```jsx
function Notification({ messages }) {
  return (
    <div>
      {messages.length > 0 && 
        <p>Anda memiliki {messages.length} pesan baru</p>
      }
    </div>
  );
}
```

### Menggunakan if-else biasa dalam function

```jsx
function LoginStatus({ isLoggedIn }) {
  if (isLoggedIn) {
    return <p>Anda sudah login</p>;
  }
  return <p>Anda belum login</p>;
}
```

**Tips conditional rendering**:
- Gunakan operator ternary (`? :`) untuk kondisi sederhana
- Gunakan operator `&&` untuk menampilkan atau menyembunyikan elemen
- Gunakan if-else untuk logika yang lebih kompleks
- Pertimbangkan untuk memisahkan komponen jika kondisi terlalu kompleks

## Lists dan Keys

React memudahkan rendering list data menggunakan metode array seperti `map()` untuk mengubah array data menjadi array elemen React.

### Rendering List Sederhana

```jsx
function NumberList() {
  const numbers = [1, 2, 3, 4, 5];
  
  return (
    <ul>
      {numbers.map(number => (
        <li key={number}>{number}</li>
      ))}
    </ul>
  );
}
```

### Pentingnya Key

Key adalah atribut string khusus yang perlu disertakan saat membuat list elemen. Key membantu React mengidentifikasi item mana yang berubah, ditambahkan, atau dihapus.

**Aturan menggunakan key**:
1. Key harus unik di antara saudara-saudaranya (sibling), tidak perlu unik secara global
2. Gunakan ID dari data jika ada (seperti `id` dari database)
3. Gunakan indeks array hanya sebagai pilihan terakhir, dan hanya jika list statis

**Contoh dengan data yang lebih kompleks**:

```jsx
function BlogList({ posts }) {
  return (
    <div>
      {posts.map(post => (
        <div key={post.id}>
          <h3>{post.title}</h3>
          <p>{post.content}</p>
        </div>
      ))}
    </div>
  );
}
```

**Kenapa key penting?**:
- Membantu React mengidentifikasi perubahan elemen
- Meningkatkan performa saat melakukan re-rendering
- Mencegah bug aneh saat state elemen list berubah

## Forms dan Controlled Components

Di React, ada dua cara menangani form input:
1. **Controlled Components**: React mengontrol nilai input
2. **Uncontrolled Components**: DOM mengontrol nilai input

### Controlled Components

Dalam controlled component, nilai elemen form ditentukan oleh state React.

```jsx
import React, { useState } from 'react';

function SimpleForm() {
  const [name, setName] = useState('');
  
  const handleSubmit = (event) => {
    event.preventDefault();
    alert(`Nama yang dimasukkan: ${name}`);
  };
  
  return (
    <form onSubmit={handleSubmit}>
      <label>
        Nama:
        <input 
          type="text" 
          value={name} 
          onChange={(e) => setName(e.target.value)} 
        />
      </label>
      <button type="submit">Submit</button>
    </form>
  );
}
```

**Keuntungan Controlled Component**:
- React menjadi "single source of truth" untuk nilai input
- Memudahkan validasi langsung saat input
- Memungkinkan manipulasi input secara dinamis

### Form dengan Multiple Inputs

```jsx
import React, { useState } from 'react';

function ContactForm() {
  const [formData, setFormData] = useState({
    name: '',
    email: '',
    message: ''
  });
  
  const handleChange = (event) => {
    const { name, value } = event.target;
    setFormData({
      ...formData,
      [name]: value
    });
  };
  
  const handleSubmit = (event) => {
    event.preventDefault();
    console.log('Form data:', formData);
  };
  
  return (
    <form onSubmit={handleSubmit}>
      <div>
        <label htmlFor="name">Nama:</label>
        <input
          id="name"
          name="name"
          type="text"
          value={formData.name}
          onChange={handleChange}
        />
      </div>
      
      <div>
        <label htmlFor="email">Email:</label>
        <input
          id="email"
          name="email"
          type="email"
          value={formData.email}
          onChange={handleChange}
        />
      </div>
      
      <div>
        <label htmlFor="message">Pesan:</label>
        <textarea
          id="message"
          name="message"
          value={formData.message}
          onChange={handleChange}
        />
      </div>
      
      <button type="submit">Kirim</button>
    </form>
  );
}
```

**Menangani berbagai jenis input**:
- Input text, textarea, dan select bekerja dengan cara serupa
- Checkbox dan radio button menggunakan properti `checked` daripada `value`
- Select multiple memerlukan penanganan khusus

## Styling di React

Ada beberapa cara untuk menerapkan styling pada komponen React:

### 1. CSS biasa

```jsx
// Buat file CSS terpisah (App.css)
import './App.css';

function Button() {
  return <button className="primary-button">Klik Saya</button>;
}
```

### 2. Inline Styling

```jsx
function Button() {
  const buttonStyle = {
    backgroundColor: 'blue',
    color: 'white',
    padding: '10px 15px',
    borderRadius: '4px',
    border: 'none',
    cursor: 'pointer'
  };
  
  return <button style={buttonStyle}>Klik Saya</button>;
}
```

### 3. CSS Modules

CSS Modules membatasi scope CSS ke komponen tertentu.

```jsx
// Button.module.css
.button {
  background-color: blue;
  color: white;
  /* properti lainnya */
}

// Button.js
import styles from './Button.module.css';

function Button() {
  return <button className={styles.button}>Klik Saya</button>;
}
```

### 4. Styled Components (Librari pihak ketiga)

```jsx
import styled from 'styled-components';

const StyledButton = styled.button`
  background-color: ${props => props.primary ? 'blue' : 'gray'};
  color: white;
  padding: 10px 15px;
  border-radius: 4px;
  border: none;
  cursor: pointer;
`;

function Button({ primary }) {
  return <StyledButton primary={primary}>Klik Saya</StyledButton>;
}
```

**Perbandingan pendekatan styling**:
- **CSS biasa**: Sederhana, tapi bisa menyebabkan konflik nama class
- **Inline styling**: Cepat, tapi tidak mendukung pseudo-class dan media query
- **CSS Modules**: Mengatasi masalah scope, terintegrasi dengan React
- **Styled Components**: Komponen dan style jadi satu, dinamis berdasarkan props

## Component Lifecycle

Meskipun functional component dengan hooks tidak memiliki metode lifecycle seperti class component, kita masih bisa mengimplementasikan perilaku yang sama dengan useEffect.

### Fase Lifecycle di React

1. **Mounting**: Komponen ditambahkan ke DOM
2. **Updating**: Komponen di-render ulang karena perubahan props atau state
3. **Unmounting**: Komponen dihapus dari DOM

### Implementasi Lifecycle dengan Hooks

```jsx
import React, { useState, useEffect } from 'react';

function LifecycleDemo() {
  const [count, setCount] = useState(0);
  
  // componentDidMount
  useEffect(() => {
    console.log('Komponen di-mount');
    
    // componentWillUnmount
    return () => {
      console.log('Komponen akan di-unmount');
    };
  }, []);
  
  // componentDidUpdate (ketika count berubah)
  useEffect(() => {
    console.log('Count berubah:', count);
  }, [count]);
  
  // Dijalankan setiap render
  useEffect(() => {
    console.log('Komponen di-render');
  });
  
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Tambah</button>
    </div>
  );
}
```

**Memetakan class lifecycle ke hooks**:
- `componentDidMount` → `useEffect(() => {}, [])`
- `componentDidUpdate` → `useEffect(() => {}, [dependencies])`
- `componentWillUnmount` → `useEffect(() => { return () => {} }, [])`
- `shouldComponentUpdate` → `React.memo` + custom comparison

## Project: To-Do List Application

Untuk mengaplikasikan semua konsep yang telah dipelajari, kita akan membuat aplikasi To-Do List sederhana.

### Fitur aplikasi:
- Menambahkan tugas baru
- Menandai tugas sebagai selesai
- Menghapus tugas
- Memfilter tugas (semua, selesai, belum selesai)

### Struktur komponen:
1. `App`: Komponen utama
2. `TodoForm`: Form untuk menambahkan tugas baru
3. `TodoList`: List semua tugas
4. `TodoItem`: Item tugas individual
5. `FilterButtons`: Tombol untuk memfilter tugas

### Implementasi Dasar

```jsx
import React, { useState, useEffect } from 'react';
import './App.css';

// Component TodoForm
function TodoForm({ addTodo }) {
  const [text, setText] = useState('');
  
  const handleSubmit = (e) => {
    e.preventDefault();
    if (!text.trim()) return;
    addTodo(text);
    setText('');
  };
  
  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        value={text}
        onChange={(e) => setText(e.target.value)}
        placeholder="Tambahkan tugas baru..."
      />
      <button type="submit">Tambah</button>
    </form>
  );
}

// Component TodoItem
function TodoItem({ todo, toggleComplete, deleteTodo }) {
  return (
    <div className={`todo-item ${todo.completed ? 'completed' : ''}`}>
      <input
        type="checkbox"
        checked={todo.completed}
        onChange={() => toggleComplete(todo.id)}
      />
      <span>{todo.text}</span>
      <button onClick={() => deleteTodo(todo.id)}>Hapus</button>
    </div>
  );
}

// Component FilterButtons
function FilterButtons({ filter, setFilter }) {
  return (
    <div className="filter-buttons">
      <button 
        className={filter === 'all' ? 'active' : ''}
        onClick={() => setFilter('all')}
      >
        Semua
      </button>
      <button 
        className={filter === 'active' ? 'active' : ''}
        onClick={() => setFilter('active')}
      >
        Aktif
      </button>
      <button 
        className={filter === 'completed' ? 'active' : ''}
        onClick={() => setFilter('completed')}
      >
        Selesai
      </button>
    </div>
  );
}

// Component utama App
function App() {
  const [todos, setTodos] = useState([]);
  const [filter, setFilter] = useState('all');
  
  // Load todos dari localStorage saat aplikasi dimulai
  useEffect(() => {
    const savedTodos = JSON.parse(localStorage.getItem('todos') || '[]');
    setTodos(savedTodos);
  }, []);
  
  // Simpan todos ke localStorage saat berubah
  useEffect(() => {
    localStorage.setItem('todos', JSON.stringify(todos));
  }, [todos]);
  
  // Fungsi untuk menambah todo
  const addTodo = (text) => {
    const newTodo = {
      id: Date.now(),
      text,
      completed: false
    };
    setTodos([...todos, newTodo]);
  };
  
  // Fungsi untuk toggle status completed
  const toggleComplete = (id) => {
    setTodos(
      todos.map(todo =>
        todo.id === id ? { ...todo, completed: !todo.completed } : todo
      )
    );
  };
  
  // Fungsi untuk menghapus todo
  const deleteTodo = (id) => {
    setTodos(todos.filter(todo => todo.id !== id));
  };
  
  // Filter todos sesuai status
  const filteredTodos = todos.filter(todo => {
    if (filter === 'all') return true;
    if (filter === 'completed') return todo.completed;
    if (filter === 'active') return !todo.completed;
    return true;
  });
  
  return (
    <div className="todo-app">
      <h1>To-Do List</h1>
      <TodoForm addTodo={addTodo} />
      <FilterButtons filter={filter} setFilter={setFilter} />
      
      <div className="todo-list">
        {filteredTodos.length === 0 ? (
          <p>Tidak ada tugas</p>
        ) : (
          filteredTodos.map(todo => (
            <TodoItem
              key={todo.id}
              todo={todo}
              toggleComplete={toggleComplete}
              deleteTodo={deleteTodo}
            />
          ))
        )}
      </div>
    </div>
  );
}

export default App;
```

### Langkah-langkah Pengembangan:

1. **Setup Project**:
   - Buat project React baru dengan `create-react-app`
   - Hapus file yang tidak perlu
   - Buat struktur folder yang rapi

2. **Implementasi Komponen Dasar**:
   - Buat komponen `App` dengan state untuk todos
   - Buat komponen `TodoForm` untuk input
   - Buat komponen `TodoItem` untuk menampilkan setiap item

3. **Tambahkan Fungsionalitas**:
   - Implementasi fungsi untuk menambah todo
   - Implementasi fungsi untuk menandai todo sebagai selesai
   - Implementasi fungsi untuk menghapus todo

4. **Tambahkan Filtering**:
   - Buat komponen `FilterButtons`
   - Implementasi logic untuk filtering

5. **Tambahkan Persistensi Data**:
   - Gunakan `localStorage` untuk menyimpan todos
   - Load todos dari localStorage saat aplikasi dimulai

6. **Styling**:
   - Tambahkan CSS untuk membuat aplikasi lebih menarik

7. **Testing dan Debugging**:
   - Uji semua fitur
   - Perbaiki bug yang ditemukan

### Bonus Challenge:
- Tambahkan fitur drag-and-drop untuk mengubah urutan todos
- Implementasi kategori atau label untuk todos
- Tambahkan fitur deadline atau reminder
- Implementasi dark mode / light mode

---

Dengan menyelesaikan modul ini dan project To-Do List, Anda akan memiliki pemahaman yang kuat tentang konsep fundamental React seperti state, props, hooks, rendering, dan lifecycle. Kemampuan ini akan menjadi dasar yang solid untuk mempelajari topik React yang lebih lanjut seperti Context API, Redux, dan React Router.

END MODULE 3
# MODUL 4: REACT ECOSYSTEM & ROUTING

**Durasi**: 2 minggu  
**Tujuan**: Memahami ekosistem React dan implementasi routing  

## Daftar Isi
1. [Pendahuluan](#pendahuluan)
2. [React Router](#react-router)
3. [Navigation dan URL Parameters](#navigation-dan-url-parameters)
4. [Nested Routes](#nested-routes)
5. [Protected Routes](#protected-routes)
6. [Code Splitting](#code-splitting)
7. [Lazy Loading](#lazy-loading)
8. [Project: Multi-page Application dengan React Router](#project-multi-page-application-dengan-react-router)
9. [Referensi Tambahan](#referensi-tambahan)

## Pendahuluan

Setelah mempelajari dasar-dasar React, saatnya kita memahami bagaimana membangun aplikasi React multi-halaman yang lebih kompleks. Pada modul ini, kita akan mempelajari konsep **routing** di React, yang memungkinkan kita membuat aplikasi dengan banyak halaman tanpa harus me-refresh browser.

React sendiri berfokus hanya pada pembuatan UI dan tidak menyediakan sistem routing bawaan. Oleh karena itu, kita akan menggunakan library tambahan bernama **React Router** yang menjadi standar de facto untuk routing di aplikasi React.

## React Router

### Apa itu React Router?

React Router adalah library paling populer untuk menangani routing di aplikasi React. Dengan React Router, kita dapat:

- Membuat aplikasi multi-halaman dengan Single Page Application (SPA)
- Menampilkan komponen berbeda berdasarkan URL
- Mengelola navigasi antar halaman tanpa refresh browser
- Membuat UI yang sinkron dengan URL

### Instalasi React Router

Untuk menginstal React Router, jalankan perintah berikut:

```bash
# Menggunakan npm
npm install react-router-dom

# Menggunakan yarn
yarn add react-router-dom
```

### Komponen Dasar React Router

React Router menyediakan beberapa komponen utama:

1. **BrowserRouter**: Wrapper utama yang harus membungkus seluruh aplikasi yang menggunakan React Router
2. **Routes**: Container untuk mengelompokkan rute-rute yang berbeda
3. **Route**: Mendefinisikan pemetaan antara path URL dan komponen yang akan dirender
4. **Link**: Untuk navigasi antar halaman (pengganti tag `<a>`)
5. **Navigate**: Untuk navigasi melalui kode (redirect programatis)

### Contoh Dasar React Router

```jsx
import { BrowserRouter, Routes, Route, Link } from 'react-router-dom';

// Komponen halaman
const Home = () => <h1>Halaman Beranda</h1>;
const About = () => <h1>Tentang Kami</h1>;
const Contact = () => <h1>Kontak Kami</h1>;

function App() {
  return (
    <BrowserRouter>
      {/* Navigasi */}
      <nav>
        <ul>
          <li><Link to="/">Beranda</Link></li>
          <li><Link to="/about">Tentang</Link></li>
          <li><Link to="/contact">Kontak</Link></li>
        </ul>
      </nav>

      {/* Konfigurasi Rute */}
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </BrowserRouter>
  );
}

export default App;
```

Dalam contoh di atas:
- `BrowserRouter` membungkus seluruh aplikasi
- `Routes` berisi definisi rute-rute aplikasi
- `Route` mendefinisikan komponen yang akan ditampilkan untuk path tertentu
- `Link` digunakan untuk navigasi antar halaman

## Navigation dan URL Parameters

### Navigation dengan Link dan NavLink

React Router menyediakan dua komponen untuk navigasi:

1. **Link**: Komponen dasar untuk navigasi
2. **NavLink**: Versi Link yang lebih canggih dengan kemampuan styling saat aktif

```jsx
import { Link, NavLink } from 'react-router-dom';

const Navigation = () => {
  return (
    <nav>
      {/* Link dasar */}
      <Link to="/">Beranda</Link>
      
      {/* NavLink dengan styling saat aktif */}
      <NavLink 
        to="/products" 
        style={({ isActive }) => isActive ? { fontWeight: 'bold' } : {}}
      >
        Produk
      </NavLink>
    </nav>
  );
};
```

### Navigasi Programatis dengan useNavigate

Kadang kita perlu melakukan navigasi melalui kode, misalnya setelah submit form atau setelah operasi asinkron:

```jsx
import { useNavigate } from 'react-router-dom';

const LoginForm = () => {
  const navigate = useNavigate();

  const handleSubmit = async (e) => {
    e.preventDefault();
    // Logic login
    const success = await loginUser(/* ... */);
    
    if (success) {
      // Arahkan ke dashboard setelah login berhasil
      navigate('/dashboard');
    }
  };

  return (
    <form onSubmit={handleSubmit}>
      {/* Form fields */}
      <button type="submit">Login</button>
    </form>
  );
};
```

### URL Parameters

URL Parameters memungkinkan kita menangkap nilai dinamis dari URL. Ini sangat berguna untuk halaman detail atau filter.

```jsx
// Definisi rute dengan parameter
<Route path="/products/:productId" element={<ProductDetail />} />

// Komponen untuk mengakses parameter
import { useParams } from 'react-router-dom';

const ProductDetail = () => {
  const { productId } = useParams();
  
  return <h1>Detail Produk ID: {productId}</h1>;
};
```

### Query Parameters

Query parameters (seperti `?search=term&category=books`) dapat diakses menggunakan hook `useSearchParams`:

```jsx
import { useSearchParams } from 'react-router-dom';

const ProductList = () => {
  const [searchParams, setSearchParams] = useSearchParams();
  
  // Mendapatkan nilai query parameter
  const search = searchParams.get('search') || '';
  const category = searchParams.get('category') || 'all';
  
  // Mengubah query parameter
  const updateCategory = (newCategory) => {
    setSearchParams({ search, category: newCategory });
  };
  
  return (
    <div>
      <h1>Daftar Produk</h1>
      <p>Pencarian: {search}</p>
      <p>Kategori: {category}</p>
      <button onClick={() => updateCategory('books')}>Buku</button>
      <button onClick={() => updateCategory('electronics')}>Elektronik</button>
    </div>
  );
};
```

## Nested Routes

Nested Routes (Rute Bersarang) memungkinkan kita membuat layout bersarang di mana beberapa komponen UI memiliki rute anaknya sendiri. Ini sangat berguna untuk membuat layout yang konsisten dengan area konten yang berubah.

### Definisi Nested Routes

```jsx
import { BrowserRouter, Routes, Route, Outlet, Link } from 'react-router-dom';

// Layout komponen
const Dashboard = () => {
  return (
    <div>
      <h1>Dashboard</h1>
      <nav>
        <Link to="/dashboard">Overview</Link>
        <Link to="/dashboard/stats">Statistik</Link>
        <Link to="/dashboard/profile">Profil</Link>
      </nav>
      
      {/* Outlet adalah tempat di mana rute anak akan dirender */}
      <Outlet />
    </div>
  );
};

// Komponen anak
const DashboardOverview = () => <div>Overview Dashboard</div>;
const DashboardStats = () => <div>Statistik Dashboard</div>;
const DashboardProfile = () => <div>Profil User</div>;

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        
        {/* Nested routes untuk Dashboard */}
        <Route path="/dashboard" element={<Dashboard />}>
          <Route index element={<DashboardOverview />} />
          <Route path="stats" element={<DashboardStats />} />
          <Route path="profile" element={<DashboardProfile />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}
```

Dalam contoh di atas:
- `Dashboard` adalah komponen induk yang menyediakan layout umum
- `Outlet` menentukan di mana komponen anak akan dirender
- `index` route ditampilkan saat parent path cocok secara tepat

### Keuntungan Nested Routes

1. **Membuat layout bersama** yang konsisten untuk beberapa halaman
2. **Mengurangi duplikasi kode** untuk elemen UI yang sama (header, sidebar, dll)
3. **Membuat kode lebih modular** dan mudah dikelola
4. **Mengelompokkan fungsionalitas terkait** dalam struktur hirarki yang jelas

## Protected Routes

Protected Routes (Rute Terproteksi) adalah rute yang hanya dapat diakses jika kondisi tertentu terpenuhi, biasanya jika pengguna sudah login atau memiliki izin tertentu.

### Implementasi Protected Routes

```jsx
import { Navigate, Outlet, useLocation } from 'react-router-dom';

// Komponen untuk protected route
const ProtectedRoute = ({ isAuthenticated }) => {
  const location = useLocation();
  
  if (!isAuthenticated) {
    // Redirect ke login dengan menyimpan lokasi yang ingin dikunjungi
    return <Navigate to="/login" state={{ from: location }} replace />;
  }
  
  // Render children route jika terautentikasi
  return <Outlet />;
};

// Penggunaan dalam config route
function App() {
  const [isAuthenticated, setIsAuthenticated] = useState(false);
  
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/login" element={<Login setIsAuthenticated={setIsAuthenticated} />} />
        
        {/* Protected routes */}
        <Route element={<ProtectedRoute isAuthenticated={isAuthenticated} />}>
          <Route path="/dashboard" element={<Dashboard />} />
          <Route path="/settings" element={<Settings />} />
          <Route path="/profile" element={<Profile />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}
```

### Menangani Redirect Setelah Login

Saat user dialihkan ke halaman login, kita bisa menyimpan halaman yang ingin mereka kunjungi dan mengarahkannya kembali setelah login:

```jsx
import { useNavigate, useLocation } from 'react-router-dom';

const Login = ({ setIsAuthenticated }) => {
  const navigate = useNavigate();
  const location = useLocation();
  
  // Ambil URL yang ingin dikunjungi dari state
  const from = location.state?.from?.pathname || "/dashboard";
  
  const handleLogin = async (e) => {
    e.preventDefault();
    // Logic login
    const success = await loginUser(/* ... */);
    
    if (success) {
      setIsAuthenticated(true);
      // Arahkan ke halaman yang diinginkan sebelumnya
      navigate(from, { replace: true });
    }
  };
  
  return (
    <form onSubmit={handleLogin}>
      {/* Form fields */}
      <button type="submit">Login</button>
    </form>
  );
};
```

### Role-Based Access Control

Protected Routes juga bisa dikembangkan untuk mendukung akses berdasarkan peran (role):

```jsx
const ProtectedRoute = ({ isAuthenticated, allowedRoles, userRole }) => {
  if (!isAuthenticated) {
    return <Navigate to="/login" replace />;
  }
  
  // Cek apakah user memiliki peran yang diizinkan
  if (allowedRoles && !allowedRoles.includes(userRole)) {
    return <Navigate to="/unauthorized" replace />;
  }
  
  return <Outlet />;
};

// Penggunaan:
<Route 
  element={
    <ProtectedRoute 
      isAuthenticated={isAuthenticated} 
      allowedRoles={['admin']} 
      userRole={userRole} 
    />
  }
>
  <Route path="/admin" element={<AdminDashboard />} />
</Route>
```

## Code Splitting

Code Splitting adalah teknik untuk memecah bundle JavaScript aplikasi menjadi beberapa chunk yang lebih kecil yang dapat dimuat secara terpisah sesuai kebutuhan. Ini sangat penting untuk aplikasi besar untuk meningkatkan performa loading awal.

### Mengapa Code Splitting Penting?

1. **Mengurangi ukuran bundle awal** yang harus dimuat
2. **Mempercepat waktu loading pertama** dari aplikasi
3. **Menunda loading kode** yang tidak dibutuhkan segera
4. **Mengoptimalkan penggunaan bandwidth** pengguna

### Dynamic Import dengan React

React mendukung dynamic import menggunakan sintaks ES:

```jsx
// Tanpa code splitting
import HeavyComponent from './HeavyComponent';

// Dengan code splitting (dynamic import)
import { useState } from 'react';

const MyComponent = () => {
  const [HeavyComponent, setHeavyComponent] = useState(null);
  
  const loadHeavyComponent = async () => {
    // Dynamic import
    const module = await import('./HeavyComponent');
    setHeavyComponent(() => module.default);
  };
  
  return (
    <div>
      <button onClick={loadHeavyComponent}>Load Heavy Component</button>
      {HeavyComponent && <HeavyComponent />}
    </div>
  );
};
```

### Code Splitting dengan Route-Based Splitting

Cara paling umum menggunakan code splitting adalah dengan memecah kode berdasarkan rute, sehingga setiap halaman dimuat secara terpisah. Ini akan dibahas lebih lanjut di bagian Lazy Loading.

## Lazy Loading

Lazy Loading adalah implementasi code splitting yang memungkinkan kita memuat komponen hanya ketika benar-benar dibutuhkan. React menyediakan `React.lazy` dan `Suspense` untuk mengimplementasikan lazy loading dengan mudah.

### React.lazy dan Suspense

```jsx
import React, { Suspense, lazy } from 'react';
import { BrowserRouter, Routes, Route } from 'react-router-dom';

// Komponen yang di-lazy load
const Home = lazy(() => import('./pages/Home'));
const About = lazy(() => import('./pages/About'));
const Dashboard = lazy(() => import('./pages/Dashboard'));
const Profile = lazy(() => import('./pages/Profile'));

function App() {
  return (
    <BrowserRouter>
      <Suspense fallback={<div>Loading...</div>}>
        <Routes>
          <Route path="/" element={<Home />} />
          <Route path="/about" element={<About />} />
          <Route path="/dashboard" element={<Dashboard />} />
          <Route path="/profile" element={<Profile />} />
        </Routes>
      </Suspense>
    </BrowserRouter>
  );
}
```

Dalam contoh di atas:
- `lazy()` membuat komponen yang dimuat secara lazy (saat dibutuhkan)
- `Suspense` menampilkan fallback selama komponen dimuat
- Setiap halaman akan menjadi chunk JavaScript terpisah

### Prefetching untuk UX yang Lebih Baik

Untuk meningkatkan UX, kita bisa melakukan prefetch komponen saat user mengarahkan mouse ke link sebelum mengklik:

```jsx
import { Link } from 'react-router-dom';
import { lazy } from 'react';

// Referensi ke komponen yang akan diprefetch
const Dashboard = lazy(() => import('./pages/Dashboard'));

const NavLink = ({ to, children }) => {
  const prefetchComponent = () => {
    // Prefetch saat hover
    if (to === '/dashboard') {
      import('./pages/Dashboard');
    }
  };
  
  return (
    <Link 
      to={to} 
      onMouseEnter={prefetchComponent}
      onFocus={prefetchComponent}
    >
      {children}
    </Link>
  );
};
```

### Error Boundary dengan Lazy Loading

Untuk menangani error saat loading komponen, kita bisa menggunakan Error Boundary:

```jsx
import { Component } from 'react';

class ErrorBoundary extends Component {
  state = { hasError: false };
  
  static getDerivedStateFromError(error) {
    return { hasError: true };
  }
  
  componentDidCatch(error, errorInfo) {
    console.error('Error loading component:', error, errorInfo);
  }
  
  render() {
    if (this.state.hasError) {
      return <div>Terjadi kesalahan saat memuat halaman. Silakan coba lagi.</div>;
    }
    
    return this.props.children;
  }
}

// Penggunaan:
<ErrorBoundary>
  <Suspense fallback={<div>Loading...</div>}>
    <Routes>
      {/* Routes */}
    </Routes>
  </Suspense>
</ErrorBoundary>
```

## Project: Multi-page Application dengan React Router

Saatnya mengaplikasikan semua yang telah dipelajari dengan membuat project multi-page application menggunakan React Router.

### Deskripsi Project

Kita akan membuat aplikasi **E-Learning Platform** sederhana dengan fitur:

- Halaman Home untuk menampilkan highlight kursus
- Halaman Courses untuk menjelajahi daftar kursus
- Halaman Course Detail untuk detail kursus tertentu
- Halaman Dashboard untuk pengguna yang sudah login
- Halaman Login/Register
- Protected routes untuk area member

### Struktur Project

```
src/
├── components/            # Shared components
│   ├── Header.jsx
│   ├── Footer.jsx
│   ├── CourseCard.jsx
│   └── ...
├── pages/                 # Page components
│   ├── Home.jsx
│   ├── Courses.jsx
│   ├── CourseDetail.jsx
│   ├── Dashboard.jsx
│   ├── Login.jsx
│   └── Register.jsx
├── layouts/               # Layout components
│   ├── MainLayout.jsx
│   └── DashboardLayout.jsx
├── context/               # Context for state management
│   └── AuthContext.jsx
├── hooks/                 # Custom hooks
│   └── useAuth.jsx
├── data/                  # Mock data
│   └── courses.js
├── App.jsx                # Main App component with routes
└── index.js               # Entry point
```

### Langkah-langkah Implementasi

1. **Setup Project**

```bash
npx create-react-app elearning-platform
cd elearning-platform
npm install react-router-dom
```

2. **Membuat Context untuk Autentikasi**

```jsx
// src/context/AuthContext.jsx
import { createContext, useState, useEffect } from 'react';

export const AuthContext = createContext();

export const AuthProvider = ({ children }) => {
  const [user, setUser] = useState(null);
  const [loading, setLoading] = useState(true);
  
  useEffect(() => {
    // Cek localStorage untuk user yang tersimpan
    const storedUser = localStorage.getItem('user');
    if (storedUser) {
      setUser(JSON.parse(storedUser));
    }
    setLoading(false);
  }, []);
  
  const login = (userData) => {
    setUser(userData);
    localStorage.setItem('user', JSON.stringify(userData));
  };
  
  const logout = () => {
    setUser(null);
    localStorage.removeItem('user');
  };
  
  return (
    <AuthContext.Provider value={{ user, login, logout, loading }}>
      {children}
    </AuthContext.Provider>
  );
};
```

3. **Membuat Custom Hook untuk Autentikasi**

```jsx
// src/hooks/useAuth.jsx
import { useContext } from 'react';
import { AuthContext } from '../context/AuthContext';

export const useAuth = () => {
  return useContext(AuthContext);
};
```

4. **Membuat Layout Components**

```jsx
// src/layouts/MainLayout.jsx
import { Outlet } from 'react-router-dom';
import Header from '../components/Header';
import Footer from '../components/Footer';

const MainLayout = () => {
  return (
    <div className="main-layout">
      <Header />
      <main>
        <Outlet />
      </main>
      <Footer />
    </div>
  );
};

export default MainLayout;

// src/layouts/DashboardLayout.jsx
import { Outlet, Link } from 'react-router-dom';
import { useAuth } from '../hooks/useAuth';

const DashboardLayout = () => {
  const { user } = useAuth();
  
  return (
    <div className="dashboard-layout">
      <aside className="sidebar">
        <div className="user-info">
          <img src={user.avatar || '/default-avatar.png'} alt={user.name} />
          <h3>{user.name}</h3>
        </div>
        <nav>
          <ul>
            <li><Link to="/dashboard">Overview</Link></li>
            <li><Link to="/dashboard/courses">My Courses</Link></li>
            <li><Link to="/dashboard/profile">Profile</Link></li>
          </ul>
        </nav>
      </aside>
      <main className="dashboard-content">
        <Outlet />
      </main>
    </div>
  );
};

export default DashboardLayout;
```

5. **Membuat Protected Route Component**

```jsx
// src/components/ProtectedRoute.jsx
import { Navigate, Outlet, useLocation } from 'react-router-dom';
import { useAuth } from '../hooks/useAuth';

const ProtectedRoute = () => {
  const { user, loading } = useAuth();
  const location = useLocation();
  
  if (loading) {
    return <div>Loading...</div>;
  }
  
  if (!user) {
    return <Navigate to="/login" state={{ from: location }} replace />;
  }
  
  return <Outlet />;
};

export default ProtectedRoute;
```

6. **Setup App dengan Routes**

```jsx
// src/App.jsx
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import { Suspense, lazy } from 'react';
import { AuthProvider } from './context/AuthContext';

// Layouts
import MainLayout from './layouts/MainLayout';
import DashboardLayout from './layouts/DashboardLayout';

// Components
import ProtectedRoute from './components/ProtectedRoute';

// Lazy loaded pages
const Home = lazy(() => import('./pages/Home'));
const Courses = lazy(() => import('./pages/Courses'));
const CourseDetail = lazy(() => import('./pages/CourseDetail'));
const Login = lazy(() => import('./pages/Login'));
const Register = lazy(() => import('./pages/Register'));
const Dashboard = lazy(() => import('./pages/Dashboard'));
const MyCourses = lazy(() => import('./pages/MyCourses'));
const Profile = lazy(() => import('./pages/Profile'));
const NotFound = lazy(() => import('./pages/NotFound'));

function App() {
  return (
    <AuthProvider>
      <BrowserRouter>
        <Suspense fallback={<div className="loading">Loading...</div>}>
          <Routes>
            {/* Public routes with MainLayout */}
            <Route element={<MainLayout />}>
              <Route path="/" element={<Home />} />
              <Route path="/courses" element={<Courses />} />
              <Route path="/courses/:courseId" element={<CourseDetail />} />
              <Route path="/login" element={<Login />} />
              <Route path="/register" element={<Register />} />
            </Route>
            
            {/* Protected routes with DashboardLayout */}
            <Route element={<ProtectedRoute />}>
              <Route element={<DashboardLayout />}>
                <Route path="/dashboard" element={<Dashboard />} />
                <Route path="/dashboard/courses" element={<MyCourses />} />
                <Route path="/dashboard/profile" element={<Profile />} />
              </Route>
            </Route>
            
            {/* 404 route */}
            <Route path="*" element={<NotFound />} />
          </Routes>
        </Suspense>
      </BrowserRouter>
    </AuthProvider>
  );
}

export default App;
```

7. **Implementasikan Komponen-komponen Halaman**

Sekarang kita perlu mengimplementasikan setiap halaman yang telah kita definisikan:
- Home.jsx
- Courses.jsx
- CourseDetail.jsx
- Login.jsx
- Register.jsx
- Dashboard.jsx
- MyCourses.jsx
- Profile.jsx
- NotFound.jsx

Contoh implementasi Login.jsx:

```jsx
// src/pages/Login.jsx
import { useState } from 'react';
import { useNavigate, useLocation, Link } from 'react-router-dom';
import { useAuth } from '../hooks/useAuth';

const Login = () => {
  const [email, setEmail] = useState('');
  const [password, setPassword] = useState('');
  const [error, setError] = useState('');
  
  const { login } = useAuth();
  const navigate = useNavigate();
  const location = useLocation();
  
  const from = location.state?.from?.pathname || "/dashboard";
  
  const handleSubmit = (e) => {
    e.preventDefault();
    setError('');
    
    // Simulasi login (dalam aplikasi nyata gunakan API)
    if (email === 'user@example.com' && password === 'password') {
      login({
        id: 1,
        name: 'John Doe',
        email: 'user@example.com',
        avatar: '/avatar.png'
      });
      navigate(from, { replace: true });
    } else {
      setError('Email atau password salah!');
    }
  };
  
  return (
    <div className="login-page">
      <h1>Login</h1>
      
      {error && <div className="error">{error}</div>}
      
      <form onSubmit={handleSubmit}>
        <div className="form-group">
          <label htmlFor="email">Email</label>
          <input
            type="email"
            id="email"
            value={email}
            onChange={(e) => setEmail(e.target.value)}
            required
          />
        </div>
        
        <div className="form-group">
          <label htmlFor="password">Password</label>
          <input
            type="password"
            id="password"
            value={password}
            onChange={(e) => setPassword(e.target.value)}
            required
          />
        </div>
        
        <button type="submit">Login</button>
      </form>
      
      <p>
        Belum punya akun? <Link to="/register">Register</Link>
      </p>
    </div>
  );
};

export default Login;
```

Implementasikan komponen-komponen lainnya dengan pendekatan serupa, menyesuaikan dengan kebutuhan masing-masing halaman.

### Testing Project

Setelah mengimplementasikan semua komponen, jalankan aplikasi untuk menguji fungsionalitas:

```bash
npm start
```

Pastikan untuk menguji:
1. Navigasi antar halaman menggunakan menu
2. Mengakses halaman detail dengan parameter URL
3. Login dan logout
4. Akses ke halaman terproteksi (Dashboard)
5. Lazy loading komponen
6. Responsifitas aplikasi

## Referensi Tambahan

1. [Dokumentasi Resmi React Router](https://reactrouter.com/)
2. [Code Splitting di React](https://reactjs.org/docs/code-splitting.html)
3. [React.lazy dan Suspense](https://reactjs.org/docs/code-splitting.html#reactlazy)
4. [Patterns for Authentication dengan React Router](https://ui.dev/react-router-protected-routes-authentication)

---

Dengan menyelesaikan modul ini, kamu sekarang memiliki pemahaman komprehensif tentang routing di React dan bagaimana membangun aplikasi multi-halaman yang kompleks. Konsep-konsep seperti protected routes, nested routes, dan lazy loading sangat penting untuk mengembangkan aplikasi React yang skalabel dan performant di dunia nyata.

Selamat belajar Web Development! Modul ini merupakan fondasi penting untuk melanjutkan ke tahap React Development pada modul berikutnya.

END MODULE 4
# MODUL 5: STATE MANAGEMENT DI REACT

## Daftar Isi
- [Pendahuluan](#pendahuluan)
- [Minggu 9: Pengenalan State Management](#minggu-9-pengenalan-state-management)
  - [Context API dan useContext](#context-api-dan-usecontext)
- [Minggu 10: Redux dan Redux Toolkit](#minggu-10-redux-dan-redux-toolkit)
  - [React Redux](#react-redux)
  - [Redux Toolkit](#redux-toolkit)
  - [Immutability Patterns](#immutability-patterns)
- [Minggu 11: Middleware dan Side Effects](#minggu-11-middleware-dan-side-effects)
  - [Middleware dan Side Effects](#middleware-dan-side-effects-1)
  - [Redux Thunk vs Redux Saga](#redux-thunk-vs-redux-saga)
- [Project: E-Commerce App](#project-e-commerce-app)
- [Referensi dan Belajar Lebih Lanjut](#referensi-dan-belajar-lebih-lanjut)

## Pendahuluan

State management adalah salah satu aspek paling penting dalam pengembangan aplikasi React yang kompleks. Seiring dengan bertambahnya ukuran aplikasi, mengelola state (data) menjadi semakin menantang. Modul ini akan membantu Anda memahami dan menguasai berbagai teknik state management di React, mulai dari Context API yang built-in hingga library eksternal seperti Redux.

## Minggu 9: Pengenalan State Management

### Context API dan useContext

#### Apa itu State Management?

State management adalah cara untuk mengelola dan menyimpan data dalam aplikasi. Pada aplikasi kecil, kita mungkin cukup menggunakan `useState` dan props, tetapi pada aplikasi yang lebih besar, pendekatan ini bisa menjadi rumit karena:

1. **Prop Drilling**: Meneruskan props melalui banyak komponen yang tidak membutuhkannya
2. **Kompleksitas State**: State yang saling berhubungan dan berubah di banyak tempat
3. **Pemeliharaan Kode**: Lebih sulit melacak perubahan dan sumber bug

#### Context API

Context API adalah fitur built-in React yang memungkinkan kita berbagi state tanpa prop drilling.

**Kapan Menggunakan Context API:**
- Ketika data perlu diakses oleh banyak komponen pada level berbeda
- Untuk menyimpan state global atau semi-global (theme, bahasa, autentikasi)
- Ketika Anda ingin menghindari prop drilling

**Komponen Utama Context API:**
1. `React.createContext()`: Membuat context baru
2. `Context.Provider`: Komponen yang menyediakan nilai context
3. `Context.Consumer` atau `useContext`: Cara untuk mengkonsumsi nilai dari context

#### Implementasi Context API

**1. Membuat Context:**

```jsx
// ThemeContext.js
import { createContext } from 'react';

// Nilai default (opsional)
const ThemeContext = createContext('light');

export default ThemeContext;
```

**2. Menyediakan Context:**

```jsx
// App.js
import { useState } from 'react';
import ThemeContext from './ThemeContext';

function App() {
  const [theme, setTheme] = useState('light');
  
  return (
    <ThemeContext.Provider value={{ theme, setTheme }}>
      <MainComponent />
    </ThemeContext.Provider>
  );
}
```

**3. Menggunakan Context dengan useContext:**

```jsx
// ThemedButton.js
import { useContext } from 'react';
import ThemeContext from './ThemeContext';

function ThemedButton() {
  const { theme, setTheme } = useContext(ThemeContext);
  
  return (
    <button 
      style={{ background: theme === 'dark' ? '#333' : '#fff', color: theme === 'dark' ? '#fff' : '#333' }}
      onClick={() => setTheme(theme === 'light' ? 'dark' : 'light')}
    >
      Toggle Theme (Current: {theme})
    </button>
  );
}
```

#### Pola Umum Context API

**Context + Reducer Pattern:**

```jsx
// UserContext.js
import { createContext, useReducer } from 'react';

const initialState = { user: null, isLoading: false, error: null };

function userReducer(state, action) {
  switch (action.type) {
    case 'LOGIN_START':
      return { ...state, isLoading: true, error: null };
    case 'LOGIN_SUCCESS':
      return { ...state, user: action.payload, isLoading: false };
    case 'LOGIN_FAILURE':
      return { ...state, error: action.payload, isLoading: false };
    case 'LOGOUT':
      return { ...state, user: null };
    default:
      return state;
  }
}

const UserContext = createContext();

export function UserProvider({ children }) {
  const [state, dispatch] = useReducer(userReducer, initialState);
  
  return (
    <UserContext.Provider value={{ state, dispatch }}>
      {children}
    </UserContext.Provider>
  );
}

export default UserContext;
```

#### Keuntungan Context API:
- Built-in di React, tidak perlu library eksternal
- Sederhana untuk kasus penggunaan yang tidak terlalu kompleks
- Tidak menambah ukuran bundle aplikasi

#### Keterbatasan Context API:
- Tidak dioptimalkan untuk perubahan yang sering
- Kurang terstruktur untuk aplikasi yang sangat besar
- Tidak memiliki fitur middleware, time-travel debugging

#### Latihan Context API

**Latihan 1:** Buat aplikasi Todo List menggunakan Context API dan useReducer.

**Latihan 2:** Implementasikan sistem autentikasi sederhana (login/logout) menggunakan Context.

## Minggu 10: Redux dan Redux Toolkit

### React Redux

Redux adalah library state management yang populer untuk aplikasi JavaScript. Meskipun tidak terikat dengan React, keduanya sering digunakan bersama melalui library React Redux.

#### Konsep Utama Redux

1. **Single Source of Truth**: Seluruh state aplikasi disimpan dalam satu objek tree dalam satu store.
2. **State is Read-Only**: Cara mengubah state adalah dengan mengirimkan (dispatch) action.
3. **Changes Made with Pure Functions**: Reducer adalah fungsi murni yang menerima state dan action, lalu mengembalikan state baru.

#### Komponen Redux

1. **Store**: Objek yang menyimpan state aplikasi
2. **Actions**: Objek yang menjelaskan apa yang terjadi
3. **Reducers**: Fungsi yang menentukan bagaimana state berubah
4. **Selectors**: Fungsi untuk mengambil bagian tertentu dari state

#### Implementasi Redux Dasar

**1. Membuat Action Types dan Action Creators:**

```jsx
// actions/counterActions.js
export const INCREMENT = 'INCREMENT';
export const DECREMENT = 'DECREMENT';
export const RESET = 'RESET';

export const increment = () => ({ type: INCREMENT });
export const decrement = () => ({ type: DECREMENT });
export const reset = () => ({ type: RESET });
```

**2. Membuat Reducer:**

```jsx
// reducers/counterReducer.js
import { INCREMENT, DECREMENT, RESET } from '../actions/counterActions';

const initialState = { count: 0 };

function counterReducer(state = initialState, action) {
  switch (action.type) {
    case INCREMENT:
      return { ...state, count: state.count + 1 };
    case DECREMENT:
      return { ...state, count: state.count - 1 };
    case RESET:
      return { ...state, count: 0 };
    default:
      return state;
  }
}

export default counterReducer;
```

**3. Membuat Root Reducer (untuk aplikasi dengan banyak reducer):**

```jsx
// reducers/index.js
import { combineReducers } from 'redux';
import counterReducer from './counterReducer';
import todosReducer from './todosReducer';

const rootReducer = combineReducers({
  counter: counterReducer,
  todos: todosReducer
});

export default rootReducer;
```

**4. Membuat Store:**

```jsx
// store.js
import { createStore } from 'redux';
import rootReducer from './reducers';

const store = createStore(
  rootReducer,
  window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__()
);

export default store;
```

**5. Menghubungkan Redux dengan React:**

```jsx
// index.js
import React from 'react';
import ReactDOM from 'react-dom';
import { Provider } from 'react-redux';
import store from './store';
import App from './App';

ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById('root')
);
```

**6. Menggunakan Redux dalam Komponen:**

```jsx
// Counter.js
import { useSelector, useDispatch } from 'react-redux';
import { increment, decrement, reset } from './actions/counterActions';

function Counter() {
  // Mengakses state dari store
  const count = useSelector(state => state.counter.count);
  // Mendapatkan fungsi dispatch
  const dispatch = useDispatch();
  
  return (
    <div>
      <h2>Counter: {count}</h2>
      <button onClick={() => dispatch(increment())}>Increment</button>
      <button onClick={() => dispatch(decrement())}>Decrement</button>
      <button onClick={() => dispatch(reset())}>Reset</button>
    </div>
  );
}
```

### Redux Toolkit

Redux Toolkit adalah opini resmi dan cara yang disarankan untuk menulis logika Redux. Itu dikembangkan untuk mengatasi tiga masalah utama yang sering dikeluhkan pengguna Redux:

1. "Konfigurasi Redux terlalu rumit"
2. "Saya harus menambahkan banyak paket untuk membuat Redux bermanfaat"
3. "Redux membutuhkan terlalu banyak boilerplate code"

#### Fitur Utama Redux Toolkit

1. **`configureStore()`**: Membungkus `createStore` dengan cara opini yang lebih baik untuk mengatur store
2. **`createReducer()`**: Memungkinkan Anda menulis reducers dengan logika mutasi karena menggunakan Immer di belakang layar
3. **`createAction()`**: Menghasilkan action creator dengan tipe yang diberikan
4. **`createSlice()`**: Menghasilkan slice reducers, action types, dan action creators
5. **`createAsyncThunk`**: Membuat thunk untuk async operations

#### Implementasi dengan Redux Toolkit

**1. Membuat Store:**

```jsx
// store.js
import { configureStore } from '@reduxjs/toolkit';
import counterReducer from './features/counter/counterSlice';

export const store = configureStore({
  reducer: {
    counter: counterReducer,
  },
});
```

**2. Membuat Slice (menggabungkan actions dan reducer):**

```jsx
// features/counter/counterSlice.js
import { createSlice } from '@reduxjs/toolkit';

const initialState = {
  value: 0,
};

export const counterSlice = createSlice({
  name: 'counter',
  initialState,
  reducers: {
    increment: (state) => {
      // Redux Toolkit mengizinkan kita untuk "mutasi" state karena menggunakan Immer di belakang layar
      state.value += 1;
    },
    decrement: (state) => {
      state.value -= 1;
    },
    incrementByAmount: (state, action) => {
      state.value += action.payload;
    },
  },
});

// Export actions
export const { increment, decrement, incrementByAmount } = counterSlice.actions;

// Export reducer
export default counterSlice.reducer;
```

**3. Menggunakan dalam Komponen:**

```jsx
// Counter.js
import { useSelector, useDispatch } from 'react-redux';
import { increment, decrement, incrementByAmount } from './counterSlice';

export function Counter() {
  const count = useSelector((state) => state.counter.value);
  const dispatch = useDispatch();

  return (
    <div>
      <div>
        <button onClick={() => dispatch(increment())}>Increment</button>
        <span>{count}</span>
        <button onClick={() => dispatch(decrement())}>Decrement</button>
        <button onClick={() => dispatch(incrementByAmount(5))}>+5</button>
      </div>
    </div>
  );
}
```

### Immutability Patterns

Redux mengharuskan kita untuk memperbarui state secara immutable (tidak langsung memodifikasi objek state yang ada). Memahami pola immutability penting untuk menggunakan Redux dengan benar.

#### Mengapa Immutability Penting?

1. **Prediktabilitas**: Memudahkan untuk melacak perubahan state
2. **Performa**: Memungkinkan optimasi rendering dengan cepat menentukan apakah state berubah
3. **Debugging**: Memudahkan untuk time-travel debugging

#### Pola Immutability Dasar

**1. Untuk Objek:**

```jsx
// Menambah properti baru
const newState = { ...oldState, name: 'John' };

// Memperbarui properti yang ada
const newState = { ...oldState, age: 30 };

// Objek bersarang
const newState = {
  ...oldState,
  user: {
    ...oldState.user,
    name: 'John'
  }
};
```

**2. Untuk Array:**

```jsx
// Menambah item
const newArray = [...oldArray, newItem];

// Menghapus item
const newArray = oldArray.filter(item => item.id !== idToRemove);

// Memperbarui item
const newArray = oldArray.map(item => 
  item.id === idToUpdate ? { ...item, name: 'New Name' } : item
);
```

#### Library Helper

Beberapa library yang membantu dengan immutability:

1. **Immer**: Memungkinkan kita untuk menulis kode yang terlihat seperti "mutasi" tetapi tetap menghasilkan state baru (digunakan oleh Redux Toolkit di balik layar)
2. **Immutable.js**: Library untuk objek immutable dengan banyak fungsi helper

#### Contoh dengan Immer

```jsx
import produce from 'immer';

const baseState = {
  users: [
    { id: 1, name: 'John' },
    { id: 2, name: 'Mary' }
  ]
};

// Tanpa Immer
const newState = {
  ...baseState,
  users: baseState.users.map(user => 
    user.id === 1 ? { ...user, name: 'John Smith' } : user
  )
};

// Dengan Immer
const newStateWithImmer = produce(baseState, draft => {
  // Kita dapat "mutasi" draft secara langsung
  const user = draft.users.find(u => u.id === 1);
  if (user) user.name = 'John Smith';
});
```

#### Latihan Immutability

**Latihan 1:** Implementasikan fungsi untuk menambah, menghapus, dan memperbarui item dalam array todos secara immutable.

**Latihan 2:** Gunakan Immer untuk menyederhanakan operasi immutable pada struktur objek bersarang.

## Minggu 11: Middleware dan Side Effects

### Middleware dan Side Effects

Redux dirancang untuk menangani perubahan state yang sinkron dan murni. Namun, aplikasi dunia nyata sering membutuhkan operasi asinkron seperti permintaan API. Di sinilah middleware berperan.

#### Apa itu Middleware?

Middleware adalah lapisan antara tindakan dipancarkan (action dispatched) dan reducer. Middleware memberikan titik ekstensi untuk menjalankan logika ketika action dikirim, seperti logging, crash reporting, melakukan operasi asinkron, dll.

#### Side Effects di Redux

Side effect adalah operasi yang mengubah state di luar alur Redux murni, seperti:
1. API calls (fetch)
2. Mengakses localStorage
3. Menggunakan timers
4. Logging

#### Implementasi Middleware Sederhana

**Logger Middleware:**

```jsx
// Tanpa Redux Toolkit
const logger = store => next => action => {
  console.log('dispatching', action);
  let result = next(action);
  console.log('next state', store.getState());
  return result;
};

// Penggunaan
import { createStore, applyMiddleware } from 'redux';
import rootReducer from './reducers';
import logger from './middleware/logger';

const store = createStore(
  rootReducer,
  applyMiddleware(logger)
);
```

**Dengan Redux Toolkit:**

```jsx
import { configureStore } from '@reduxjs/toolkit';
import rootReducer from './reducers';

// Logger middleware
const logger = store => next => action => {
  console.log('dispatching', action);
  let result = next(action);
  console.log('next state', store.getState());
  return result;
};

const store = configureStore({
  reducer: rootReducer,
  middleware: (getDefaultMiddleware) => 
    getDefaultMiddleware().concat(logger)
});
```

### Redux Thunk vs Redux Saga

Untuk menangani side effects (terutama operasi asinkron), dua middleware yang paling populer adalah Redux Thunk dan Redux Saga.

#### Redux Thunk

Redux Thunk adalah middleware yang memungkinkan action creators mengembalikan fungsi (thunk) alih-alih objek action. Thunk ini menerima `dispatch` dan `getState` sebagai argumen.

**Keuntungan Thunk:**
- Sederhana dan mudah dipelajari
- Ukuran kecil
- Cocok untuk kasus penggunaan sederhana hingga menengah

**Kelemahan Thunk:**
- Logika asinkron bisa menjadi sulit untuk diuji
- Menangani alur kompleks bisa jadi rumit
- Kurang terstruktur untuk kasus yang sangat kompleks

**Contoh Redux Thunk:**

```jsx
// actions/userActions.js
export const fetchUserRequest = () => ({ type: 'FETCH_USER_REQUEST' });
export const fetchUserSuccess = (user) => ({ type: 'FETCH_USER_SUCCESS', payload: user });
export const fetchUserFailure = (error) => ({ type: 'FETCH_USER_FAILURE', payload: error });

// Thunk action creator
export const fetchUser = (userId) => {
  return async (dispatch, getState) => {
    dispatch(fetchUserRequest());
    try {
      const response = await fetch(`https://api.example.com/users/${userId}`);
      const data = await response.json();
      dispatch(fetchUserSuccess(data));
    } catch (error) {
      dispatch(fetchUserFailure(error.message));
    }
  };
};

// Penggunaan dalam komponen
const UserProfile = ({ userId }) => {
  const dispatch = useDispatch();
  const { user, loading, error } = useSelector(state => state.user);
  
  useEffect(() => {
    dispatch(fetchUser(userId));
  }, [userId, dispatch]);
  
  if (loading) return <div>Loading...</div>;
  if (error) return <div>Error: {error}</div>;
  if (!user) return null;
  
  return <div>{user.name}</div>;
};
```

**Dengan Redux Toolkit:**

Redux Toolkit memiliki `createAsyncThunk` yang menyederhanakan pola ini:

```jsx
// features/users/usersSlice.js
import { createSlice, createAsyncThunk } from '@reduxjs/toolkit';

export const fetchUser = createAsyncThunk(
  'users/fetchUser',
  async (userId, { rejectWithValue }) => {
    try {
      const response = await fetch(`https://api.example.com/users/${userId}`);
      if (!response.ok) throw new Error('Server error');
      const data = await response.json();
      return data;
    } catch (error) {
      return rejectWithValue(error.message);
    }
  }
);

const usersSlice = createSlice({
  name: 'users',
  initialState: {
    user: null,
    loading: false,
    error: null
  },
  reducers: {},
  extraReducers: (builder) => {
    builder
      .addCase(fetchUser.pending, (state) => {
        state.loading = true;
        state.error = null;
      })
      .addCase(fetchUser.fulfilled, (state, action) => {
        state.loading = false;
        state.user = action.payload;
      })
      .addCase(fetchUser.rejected, (state, action) => {
        state.loading = false;
        state.error = action.payload;
      });
  }
});

export default usersSlice.reducer;
```

#### Redux Saga

Redux Saga adalah middleware yang menggunakan generator JavaScript untuk membuat alur asinkron yang lebih terstruktur dan deklaratif.

**Keuntungan Saga:**
- Alur asinkron yang lebih terstruktur
- Lebih mudah diuji
- Fitur bawaan untuk konkurensi, racing conditions, dan pembatalan
- Cocok untuk aplikasi dengan alur asinkron kompleks

**Kelemahan Saga:**
- Kurva belajar yang lebih tinggi (perlu memahami generator)
- Lebih banyak kode boilerplate
- Mungkin berlebihan untuk kasus yang sederhana

**Contoh Redux Saga:**

```jsx
// sagas/userSaga.js
import { call, put, takeLatest } from 'redux-saga/effects';
import { 
  FETCH_USER_REQUEST, 
  fetchUserSuccess, 
  fetchUserFailure 
} from '../actions/userActions';

// Worker saga: akan melakukan tugas asinkron
function* fetchUser(action) {
  try {
    const { userId } = action.payload;
    const response = yield call(fetch, `https://api.example.com/users/${userId}`);
    const user = yield response.json();
    yield put(fetchUserSuccess(user));
  } catch (error) {
    yield put(fetchUserFailure(error.message));
  }
}

// Watcher saga: memantau tindakan yang dikirim
export function* userSaga() {
  yield takeLatest(FETCH_USER_REQUEST, fetchUser);
}
```

**Saga Root dan Setup:**

```jsx
// sagas/index.js
import { all } from 'redux-saga/effects';
import { userSaga } from './userSaga';
import { cartSaga } from './cartSaga';

export default function* rootSaga() {
  yield all([
    userSaga(),
    cartSaga(),
  ]);
}

// store.js
import { createStore, applyMiddleware } from 'redux';
import createSagaMiddleware from 'redux-saga';
import rootReducer from './reducers';
import rootSaga from './sagas';

const sagaMiddleware = createSagaMiddleware();

const store = createStore(
  rootReducer,
  applyMiddleware(sagaMiddleware)
);

sagaMiddleware.run(rootSaga);

export default store;
```

#### Perbandingan Thunk vs Saga

| Fitur | Redux Thunk | Redux Saga |
|-------|-------------|------------|
| Kurva Belajar | Rendah | Sedang-Tinggi |
| Ukuran Bundle | Kecil | Lebih Besar |
| Testing | Cukup Rumit | Lebih Mudah |
| Pembatalan | Manual | Built-in |
| Konkurensi | Manual | Built-in |
| Kompleksitas | Sederhana | Lebih Kompleks |
| Kasus Ideal | Aplikasi Kecil-Menengah | Aplikasi Kompleks |

#### Latihan Middleware

**Latihan 1:** Implementasikan Redux Thunk untuk mengambil data dari API dan tampilkan dalam komponen.

**Latihan 2:** Konversi aplikasi Thunk ke Saga dan bandingkan pendekatan keduanya.

## Project: E-Commerce App

Sekarang saatnya menerapkan semua yang telah dipelajari dengan membangun aplikasi E-Commerce. Proyek ini akan mencakup:

1. Manajemen state kompleks dengan Redux Toolkit
2. Penanganan operasi asinkron untuk mengambil data produk
3. Manajemen keranjang belanja
4. Proses checkout
5. Autentikasi pengguna

### Struktur Proyek

```
e-commerce-app/
│
├── public/
├── src/
│   ├── app/
│   │   ├── store.js             # Redux store configuration
│   │   └── rootReducer.js       # Root reducer
│   │
│   ├── components/              # Shared components
│   │   ├── Header/
│   │   ├── Footer/
│   │   ├── ProductCard/
│   │   └── ...
│   │
│   ├── features/                # Feature modules with slice
│   │   ├── auth/
│   │   │   ├── authSlice.js
│   │   │   ├── Login.js
│   │   │   └── Register.js
│   │   │
│   │   ├── products/
│   │   │   ├── productsSlice.js
│   │   │   ├── ProductList.js
│   │   │   └── ProductDetail.js
│   │   │
│   │   ├── cart/
│   │   │   ├── cartSlice.js
│   │   │   └── Cart.js
│   │   │
│   │   └── checkout/
│   │       ├── checkoutSlice.js
│   │       └── Checkout.js
│   │
│   ├── services/                # API services
│   │   ├── api.js
│   │   └── ...
│   │
│   ├── utils/                   # Utility functions
│   ├── App.js
│   └── index.js
│
└── package.json
```

### Implementasi Fitur Utama

#### 1. Slice untuk Produk

```jsx
// features/products/productsSlice.js
import { createSlice, createAsyncThunk } from '@reduxjs/toolkit';
import { fetchProducts } from '../../services/api';

export const getProducts = createAsyncThunk(
  'products/getProducts',
  async (_, { rejectWithValue }) => {
    try {
      const response = await fetchProducts();
      return response.data;
    } catch (error) {
      return rejectWithValue(error.response.data);
    }
  }
);

const productsSlice = createSlice({
  name: 'products',
  initialState: {
    items: [],
    status: 'idle', // 'idle' | 'loading' | 'succeeded' | 'failed'
    error: null
  },
  reducers: {},
  extraReducers: (builder) => {
    builder
      .addCase(getProducts.pending, (state) => {
        state.status = 'loading';
      })
      .addCase(getProducts.fulfilled, (state, action) => {
        state.status = 'succeeded';
        state.items = action.payload;
      })
      .addCase(getProducts.rejected, (state, action) => {
        state.status = 'failed';
        state.error = action.payload;
      });
  }
});

export default productsSlice.reducer;
```

#### 2. Slice untuk Keranjang

```jsx
// features/cart/cartSlice.js
import { createSlice } from '@reduxjs/toolkit';

const cartSlice = createSlice({
  name: 'cart',
  initialState: {
    items: [],
    totalQuantity: 0,
    totalAmount: 0
  },
  reducers: {
    addItemToCart(state, action) {
      const newItem = action.payload;
      const existingItem = state.items.find(item => item.id === newItem.id);
      
      if (!existingItem) {
        state.items.push({
          id: newItem.id,
          price: newItem.price,
          quantity: 1,
          totalPrice: newItem.price,
          name: newItem.title,
          image: newItem.image
        });
      } else {
        existingItem.quantity++;
        existingItem.totalPrice += newItem.price;
      }
      
      state.totalQuantity++;
      state.totalAmount += newItem.price;
    },
    
    removeItemFromCart(state, action) {
      const id = action.payload;
      const existingItem = state.items.find(item => item.id === id);
      
      if (existingItem.quantity === 1) {
        state.items = state.items.filter(item => item.id !== id);
      } else {
        existingItem.quantity--;
        existingItem.totalPrice -= existingItem.price;
      }
      
      state.totalQuantity--;
      state.totalAmount -= existingItem.price;
    },
    
    clearCart(state) {
      state.items = [];
      state.totalQuantity = 0;
      state.totalAmount = 0;
    }
  }
});

export const { addItemToCart, removeItemFromCart, clearCart } = cartSlice.actions;
export default cartSlice.reducer;
```

#### 3. Komponen Produk dan Keranjang

```jsx
// features/products/ProductList.js
import React, { useEffect } from 'react';
import { useDispatch, useSelector } from 'react-redux';
import { getProducts } from './productsSlice';
import { addItemToCart } from '../cart/cartSlice';
import ProductCard from '../../components/ProductCard';

const ProductList = () => {
  const dispatch = useDispatch();
  const { items, status, error } = useSelector(state => state.products);
  
  useEffect(() => {
    if (status === 'idle') {
      dispatch(getProducts());
    }
  }, [status, dispatch]);
  
  if (status === 'loading') {
    return <div>Loading...</div>;
  }
  
  if (status === 'failed') {
    return <div>Error: {error}</div>;
  }
  
  return (
    <div className="product-grid">
      {items.map(product => (
        <ProductCard 
          key={product.id}
          product={product}
          onAddToCart={() => dispatch(addItemToCart(product))}
        />
      ))}
    </div>
  );
};

export default ProductList;

// features/cart/Cart.js
import React from 'react';
import { useSelector, useDispatch } from 'react-redux';
import { addItemToCart, removeItemFromCart, clearCart } from './cartSlice';

const Cart = () => {
  const dispatch = useDispatch();
  const { items, totalQuantity, totalAmount } = useSelector(state => state.cart);
  
  if (items.length === 0) {
    return <div>Your cart is empty.</div>;
  }
  
  return (
    <div className="cart">
      <h2>Your Cart</h2>
      <div className="cart-items">
        {items.map(item => (
          <div key={item.id} className="cart-item">
            <img src={item.image} alt={item.name} width="50" />
            <div>
              <h3>{item.name}</h3>
              <p>${item.price.toFixed(2)} x {item.quantity}</p>
              <div className="item-actions">
                <button onClick={() => dispatch(removeItemFromCart(item.id))}>-</button>
                <span>{item.quantity}</span>
                <button onClick={() => dispatch(addItemToCart({ id: item.id, price: item.price, title: item.name, image: item.image }))}>+</button>
              </div>
            </div>
            <div className="item-total">${item.totalPrice.toFixed(2)}</div>
          </div>
        ))}
      </div>
      <div className="cart-summary">
        <div>Total Items: {totalQuantity}</div>
        <div>Total Amount: ${totalAmount.toFixed(2)}</div>
        <button className="checkout-btn">Proceed to Checkout</button>
        <button className="clear-cart-btn" onClick={() => dispatch(clearCart())}>Clear Cart</button>
      </div>
    </div>
  );
};

export default Cart;

#### 4. Store Configuration

```jsx
// app/store.js
import { configureStore } from '@reduxjs/toolkit';
import productsReducer from '../features/products/productsSlice';
import cartReducer from '../features/cart/cartSlice';
import authReducer from '../features/auth/authSlice';
import checkoutReducer from '../features/checkout/checkoutSlice';

export const store = configureStore({
  reducer: {
    products: productsReducer,
    cart: cartReducer,
    auth: authReducer,
    checkout: checkoutReducer
  },
});
```

#### 5. API Service

```jsx
// services/api.js
import axios from 'axios';

const API_URL = 'https://fakestoreapi.com';

export const fetchProducts = () => {
  return axios.get(`${API_URL}/products`);
};

export const fetchProductById = (id) => {
  return axios.get(`${API_URL}/products/${id}`);
};

export const loginUser = (credentials) => {
  return axios.post(`${API_URL}/auth/login`, credentials);
};

// ... other API functions
```

### Pengembangan Proyek

Berikut adalah beberapa langkah untuk mengembangkan proyek ini:

1. **Setup Project Base**:
   - Inisialisasi proyek React dengan create-react-app
   - Instal dependensi: redux, react-redux, @reduxjs/toolkit, axios, react-router-dom

2. **Implementasi Routing**:
   - Konfigurasikan routes untuk halaman utama, detail produk, keranjang, dan checkout

3. **Implementasi State Management**:
   - Buat slices untuk produk, keranjang, autentikasi, dan checkout
   - Konfigurasikan Redux store

4. **Implementasi UI**:
   - Buat komponen untuk setiap fitur
   - Hubungkan komponen dengan Redux store

5. **Handling API dan Side Effects**:
   - Implementasikan API calls menggunakan createAsyncThunk
   - Tangani loading states dan errors

6. **Testing**:
   - Tulis unit tests untuk reducers dan thunks
   - Tulis integration tests untuk komponen

### Tantangan Tambahan

Setelah implementasi dasar selesai, coba tambahkan fitur-fitur ini untuk tantangan:

1. **Wishlist/Favorit**:
   - Implementasikan slice baru untuk menyimpan item favorit
   - Tambahkan tombol untuk menambah/menghapus dari favorit

2. **Filter dan Pencarian**:
   - Implementasikan filter untuk kategori produk
   - Tambahkan fitur pencarian

3. **Paginasi**:
   - Implementasikan paginasi untuk daftar produk

4. **Persistensi State**:
   - Gunakan redux-persist untuk menyimpan keranjang di localStorage

5. **Multiple Middleware**:
   - Tambahkan middleware untuk logging
   - Implementasikan timer untuk checkout (countdown)

## Referensi dan Belajar Lebih Lanjut

### Dokumentasi Resmi
- [React Context API](https://reactjs.org/docs/context.html)
- [Redux Documentation](https://redux.js.org/)
- [Redux Toolkit](https://redux-toolkit.js.org/)
- [Redux Thunk](https://github.com/reduxjs/redux-thunk)
- [Redux Saga](https://redux-saga.js.org/)

### Sumber Belajar
- [Egghead.io Redux Courses](https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867)
- [Redux Essentials Tutorial](https://redux.js.org/tutorials/essentials/part-1-overview-concepts)
- [React Redux Tutorials (Dave Ceddia)](https://daveceddia.com/redux-tutorial/)

### Tools
- [Redux DevTools Extension](https://github.com/zalmoxisus/redux-devtools-extension)
- [Immer](https://immerjs.github.io/immer/)
- [Reselect](https://github.com/reduxjs/reselect)

### Pola dan Praktik Terbaik
- [Redux Style Guide](https://redux.js.org/style-guide/style-guide)
- [Immutable Update Patterns](https://redux.js.org/usage/structuring-reducers/immutable-update-patterns)
- [Normalizing State Shape](https://redux.js.org/usage/structuring-reducers/normalizing-state-shape)

### YouTube Channels
- [Redux by Dan Abramov](https://www.youtube.com/watch?v=xsSnOQynTHs)
- [Net Ninja Redux Series](https://www.youtube.com/watch?v=Jf9EfJBz2Fc&list=PL4cUxeGkcC9ij8CfkAY2RAGb-tmkNwQHG)
- [Stephen Grider's Redux Courses](https://www.udemy.com/course/react-redux/)

END MODULE 5
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
