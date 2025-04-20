# Materi Pembelajaran Golang: Dasar hingga Expert

## Fase 1: Dasar-Dasar Golang (Hari 1-15)

### Hari 1: Pengenalan Go dan Setup

**1. Apa itu Go (Golang)?**
- Golang adalah bahasa pemrograman open-source yang dikembangkan oleh Google
- Dirancang untuk performa tinggi, konkurensi mudah, dan sintaks sederhana
- Cocok untuk pengembangan backend, microservices, dan aplikasi sistem

**2. Keunggulan Go:**
- Kompilasi cepat dan hasil binary yang efisien
- Garbage collection otomatis
- Konkurensi bawaan (goroutines & channels)
- Pustaka standar yang kaya
- Static typing dengan sintaks yang sederhana

**3. Instalasi Go:**
```bash
# Di Linux/macOS via homebrew
brew install go

# Di Windows via chocolatey
choco install golang

# Atau download dari golang.org
```

**4. Setup Workspace:**
```bash
# Buat direktori Go workspace
mkdir -p ~/go/{bin,src,pkg}

# Tambahkan ke path di .bashrc atau .zshrc
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```

**5. Program Hello World:**
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, Go!")
}
```

**Latihan Hari 1:**
1. Instal Go di komputer Anda
2. Setup workspace Go
3. Buat dan jalankan program Hello World
4. Eksperimen dengan beberapa pesan berbeda

### Hari 2: Variabel dan Tipe Data

**1. Deklarasi Variabel:**
```go
// Deklarasi dengan tipe eksplisit
var nama string = "Budi"

// Deklarasi singkat dengan inferensi tipe
umur := 25

// Multiple declaration
var x, y int = 10, 20
```

**2. Tipe Data Dasar:**
```go
// Integers
var a int = 10
var b int8 = 127  // -128 to 127
var c uint = 100  // unsigned integer

// Floating point
var f float32 = 3.14
var g float64 = 3.141592653589793

// Boolean
var benar bool = true
var salah bool = false

// String
var pesan string = "Halo Golang"
```

**3. Konstanta:**
```go
const Pi = 3.14159
const (
    StatusOK = 200
    StatusNotFound = 404
)
```

**4. Type Conversions:**
```go
var i int = 42
var f float64 = float64(i)
var s string = strconv.Itoa(i)  // Int to String
```

**Latihan Hari 2:**
1. Buat program yang mendeklarasikan dan menampilkan variabel berbagai tipe
2. Lakukan konversi antar tipe data
3. Gunakan konstanta dalam program

### Hari 3: Operator dan Struktur Kendali

**1. Operator:**
```go
// Aritmatika: +, -, *, /, %
sum := 5 + 3  // 8
div := 10 / 3  // 3 (integer division)

// Perbandingan: ==, !=, <, >, <=, >=
isEqual := (5 == 5)  // true

// Logika: &&, ||, !
result := (true && false)  // false
```

**2. If Statement:**
```go
if umur >= 17 {
    fmt.Println("Boleh membuat SIM")
} else if umur >= 13 {
    fmt.Println("Boleh main sosial media")
} else {
    fmt.Println("Masih anak-anak")
}

// If dengan statement awal
if nilai := getNilai(); nilai > 80 {
    fmt.Println("Nilai A")
}
```

**3. Switch Statement:**
```go
switch hari {
case "Senin":
    fmt.Println("Awal minggu")
case "Jumat":
    fmt.Println("Akhir minggu kerja")
default:
    fmt.Println("Hari biasa")
}

// Switch tanpa ekspresi
switch {
case nilai >= 80:
    fmt.Println("Nilai A")
case nilai >= 70:
    fmt.Println("Nilai B")
default:
    fmt.Println("Nilai C")
}
```

**4. Loops:**
```go
// For tradisional
for i := 0; i < 5; i++ {
    fmt.Println(i)
}

// For sebagai while
i := 0
for i < 5 {
    fmt.Println(i)
    i++
}

// For selamanya
for {
    fmt.Println("Infinite loop")
    break  // Keluar dari loop
}
```

**Latihan Hari 3:**
1. Buat program kalkulator sederhana dengan operator aritmatika
2. Buat program yang menggunakan if-else untuk menentukan kategori nilai
3. Buat program yang menggunakan switch untuk menu pilihan
4. Buat program yang mencetak pola menggunakan loop

### Hari 4: Array, Slice, dan Map

**1. Array:**
```go
// Deklarasi array
var angka [5]int  // Array dengan 5 elemen integer
angka[0] = 10
angka[1] = 20

// Inisialisasi langsung
nama := [3]string{"Andi", "Budi", "Cici"}

// Array dengan ukuran otomatis
kota := [...]string{"Jakarta", "Bandung", "Surabaya"}
```

**2. Slice:**
```go
// Membuat slice dari array
var s []int = angka[1:4]  // elemen 1, 2, 3

// Membuat slice langsung
buah := []string{"Apel", "Jeruk", "Mangga"}

// Fungsi make untuk slice
numbers := make([]int, 5)      // len=5, cap=5
numbers = append(numbers, 6)   // menambah elemen
```

**3. Maps:**
```go
// Deklarasi map
var userAge map[string]int
userAge = make(map[string]int)

// Inisialisasi langsung
scores := map[string]int{
    "Andi": 85,
    "Budi": 92,
    "Cici": 78,
}

// Operasi map
scores["Dedi"] = 88        // Menambah/mengubah
nilai, exists := scores["Andi"]  // Mengecek keberadaan key
delete(scores, "Cici")     // Menghapus key
```

**Latihan Hari 4:**
1. Buat program yang mengolah data array siswa
2. Buat program yang menggunakan slice untuk daftar dinamis
3. Buat kamus sederhana menggunakan map
4. Implementasikan fungsi pencarian di slice

### Hari 5: Structs dan Pointers

**1. Structs:**
```go
// Mendefinisikan struct
type Person struct {
    Name string
    Age  int
    Address string
}

// Membuat instance struct
var p1 Person
p1.Name = "Budi"
p1.Age = 25

// Inisialisasi langsung
p2 := Person{
    Name: "Ani",
    Age: 23,
}

// Struct anonim
employee := struct {
    ID   int
    Role string
}{
    ID:   1001,
    Role: "Developer",
}
```

**2. Pointers:**
```go
// Deklarasi pointer
var p *int
x := 10
p = &x  // p menyimpan alamat x

// Dereference pointer
fmt.Println(*p)  // Mengakses nilai yang ditunjuk p

// Pointer ke struct
var pPerson *Person
pPerson = &p1
pPerson.Name = "Budi Santoso"  // Mengubah nilai melalui pointer
```

**3. Struct Methods:**
```go
// Method pada struct
type Rectangle struct {
    Width, Height float64
}

// Method dengan receiver
func (r Rectangle) Area() float64 {
    return r.Width * r.Height
}

// Method dengan pointer receiver
func (r *Rectangle) Scale(factor float64) {
    r.Width *= factor
    r.Height *= factor
}
```

**Latihan Hari 5:**
1. Buat struct untuk merepresentasikan produk dengan beberapa atribut
2. Tambahkan method ke struct untuk menghitung diskon
3. Buat fungsi yang memanipulasi struct melalui pointer
4. Implementasikan sistem inventaris sederhana menggunakan struct dan slice

### Hari 6: Functions dan Packages

**1. Functions:**
```go
// Fungsi dasar
func sayHello(name string) {
    fmt.Println("Hello,", name)
}

// Fungsi dengan return value
func add(a, b int) int {
    return a + b
}

// Fungsi dengan multiple return values
func divide(a, b float64) (float64, error) {
    if b == 0 {
        return 0, errors.New("pembagian dengan nol")
    }
    return a / b, nil
}

// Variadic functions
func sum(nums ...int) int {
    total := 0
    for _, num := range nums {
        total += num
    }
    return total
}
```

**2. Packages:**
```go
// Membuat package baru (di file utils/math.go)
package utils

// Exported function (huruf kapital)
func Add(a, b int) int {
    return a + b
}

// Non-exported function (huruf kecil)
func multiply(a, b int) int {
    return a * b
}

// Menggunakan package (di main.go)
package main

import (
    "fmt"
    "myapp/utils"
)

func main() {
    result := utils.Add(5, 3)
    fmt.Println(result)
}
```

**3. Anonymous Functions & Closures:**
```go
// Anonymous function
func main() {
    func() {
        fmt.Println("Anonymous function")
    }()
    
    // Function variable
    add := func(a, b int) int {
        return a + b
    }
    fmt.Println(add(3, 5))
    
    // Closure
    counter := func() func() int {
        count := 0
        return func() int {
            count++
            return count
        }
    }()
    
    fmt.Println(counter())  // 1
    fmt.Println(counter())  // 2
}
```

**Latihan Hari 6:**
1. Buat package utilities dengan beberapa fungsi helper
2. Implementasikan fungsi-fungsi matematika dasar
3. Buat fungsi yang mengembalikan multiple values
4. Buat closure untuk counter atau generator

### Hari 7: Error Handling

**1. Error Basics:**
```go
// Mengembalikan error
func divide(a, b float64) (float64, error) {
    if b == 0 {
        return 0, errors.New("pembagian dengan nol")
    }
    return a / b, nil
}

// Penanganan error
result, err := divide(10, 0)
if err != nil {
    fmt.Println("Error:", err)
} else {
    fmt.Println("Result:", result)
}
```

**2. Custom Errors:**
```go
// Membuat custom error type
type ValidationError struct {
    Field string
    Message string
}

func (e *ValidationError) Error() string {
    return fmt.Sprintf("validasi gagal pada field %s: %s", e.Field, e.Message)
}

// Menggunakan custom error
func validateAge(age int) error {
    if age < 0 {
        return &ValidationError{
            Field: "age",
            Message: "tidak boleh negatif",
        }
    }
    return nil
}
```

**3. Panic dan Recover:**
```go
// Fungsi dengan panic
func processCriticalData() {
    data := getData()
    if data == nil {
        panic("data kritis tidak tersedia")
    }
    // proses data
}

// Recover dari panic
func safeProcess() {
    defer func() {
        if r := recover(); r != nil {
            fmt.Println("Recovered from panic:", r)
        }
    }()
    
    processCriticalData()
}
```

**Latihan Hari 7:**
1. Buat fungsi validasi dengan berbagai error cases
2. Implementasikan custom error untuk aplikasi
3. Buat program yang mendemonstrasikan panic dan recover
4. Implementasikan logging untuk error handling

### Hari 8: Testing

**1. Unit Testing Dasar:**
```go
// File: math.go
package math

func Add(a, b int) int {
    return a + b
}

// File: math_test.go
package math

import "testing"

func TestAdd(t *testing.T) {
    result := Add(3, 2)
    expected := 5
    
    if result != expected {
        t.Errorf("Add(3, 2) = %d; want %d", result, expected)
    }
}
```

**2. Test Cases:**
```go
func TestAdd(t *testing.T) {
    tests := []struct {
        name     string
        a, b     int
        expected int
    }{
        {"positive", 3, 2, 5},
        {"negative", -1, -2, -3},
        {"mixed", -5, 5, 0},
    }
    
    for _, tc := range tests {
        t.Run(tc.name, func(t *testing.T) {
            result := Add(tc.a, tc.b)
            if result != tc.expected {
                t.Errorf("Add(%d, %d) = %d; want %d", 
                         tc.a, tc.b, result, tc.expected)
            }
        })
    }
}
```

**3. Benchmarking:**
```go
func BenchmarkAdd(b *testing.B) {
    for i := 0; i < b.N; i++ {
        Add(3, 2)
    }
}
```

**4. Coverage Testing:**
```bash
go test -cover ./...
```

**Latihan Hari 8:**
1. Buat test cases untuk fungsi yang dibuat sebelumnya
2. Implementasikan table-driven tests
3. Jalankan benchmark untuk fungsi kritis
4. Gunakan test coverage untuk meningkatkan test quality

### Hari 9: Concurrency Dasar - Goroutines

**1. Goroutines Basics:**
```go
// Membuat goroutine
func main() {
    go sayHello("World")  // Berjalan secara asynchronous
    
    // Pastikan program tidak exit sebelum goroutine selesai
    time.Sleep(100 * time.Millisecond)
}

func sayHello(name string) {
    fmt.Println("Hello,", name)
}
```

**2. WaitGroups:**
```go
func main() {
    var wg sync.WaitGroup
    
    // Tambahkan counter
    wg.Add(1)
    
    go func() {
        defer wg.Done()  // Kurangi counter ketika selesai
        fmt.Println("Goroutine working...")
    }()
    
    // Tunggu sampai semua goroutines selesai
    wg.Wait()
    fmt.Println("All done!")
}
```

**3. Multiple Goroutines:**
```go
func main() {
    var wg sync.WaitGroup
    
    // Jalankan beberapa goroutines
    for i := 1; i <= 5; i++ {
        wg.Add(1)
        go worker(i, &wg)
    }
    
    wg.Wait()
}

func worker(id int, wg *sync.WaitGroup) {
    defer wg.Done()
    fmt.Printf("Worker %d starting\n", id)
    time.Sleep(time.Second)
    fmt.Printf("Worker %d done\n", id)
}
```

**Latihan Hari 9:**
1. Buat program yang menjalankan beberapa goroutines
2. Implementasikan waitgroup untuk sinkronisasi
3. Buat worker pool pattern
4. Implementasikan counter bersama dengan mutex

### Hari 10: Concurrency Lanjutan - Channels

**1. Channel Basics:**
```go
// Membuat channel
ch := make(chan int)

// Mengirim data ke channel
go func() {
    ch <- 42  // Mengirim nilai ke channel
}()

// Menerima data dari channel
value := <-ch  // Menerima nilai dari channel
fmt.Println(value)

// Buffered channel
bufCh := make(chan string, 2)
bufCh <- "hello"
bufCh <- "world"
```

**2. Channel Direction:**
```go
// Channel hanya untuk kirim
func send(ch chan<- int, value int) {
    ch <- value
}

// Channel hanya untuk terima
func receive(ch <-chan int) int {
    return <-ch
}
```

**3. Select Statement:**
```go
func main() {
    ch1 := make(chan string)
    ch2 := make(chan string)
    
    go func() {
        time.Sleep(1 * time.Second)
        ch1 <- "one"
    }()
    
    go func() {
        time.Sleep(2 * time.Second)
        ch2 <- "two"
    }()
    
    for i := 0; i < 2; i++ {
        select {
        case msg1 := <-ch1:
            fmt.Println("Received", msg1)
        case msg2 := <-ch2:
            fmt.Println("Received", msg2)
        case <-time.After(3 * time.Second):
            fmt.Println("Timeout")
        }
    }
}
```

**4. Closing Channels:**
```go
func main() {
    jobs := make(chan int, 5)
    done := make(chan bool)
    
    // Producer
    go func() {
        for i := 1; i <= 5; i++ {
            jobs <- i
        }
        close(jobs)  // Tutup channel setelah selesai
    }()
    
    // Consumer
    go func() {
        for {
            j, more := <-jobs
            if more {
                fmt.Println("received job", j)
            } else {
                fmt.Println("all jobs received")
                done <- true
                return
            }
        }
    }()
    
    <-done
}
```

**Latihan Hari 10:**
1. Buat program producer-consumer dengan channels
2. Implementasikan fan-out/fan-in pattern
3. Gunakan select untuk timeout handling
4. Implementasikan pipeline pattern

### Hari 11: Context dan Pattern Concurrency

**1. Context:**
```go
func main() {
    // Context dengan cancel
    ctx, cancel := context.WithCancel(context.Background())
    defer cancel()
    
    go doWork(ctx)
    
    time.Sleep(5 * time.Second)
    cancel()  // Batalkan semua operasi
    time.Sleep(1 * time.Second)
}

func doWork(ctx context.Context) {
    for {
        select {
        case <-ctx.Done():
            fmt.Println("Work cancelled")
            return
        default:
            fmt.Println("Working...")
        }
        time.Sleep(1 * time.Second)
    }
}
```

**2. Timeout dan Deadline:**
```go
// Context dengan timeout
ctx, cancel := context.WithTimeout(context.Background(), 5*time.Second)
defer cancel()

// Context dengan deadline
deadline := time.Now().Add(10 * time.Second)
ctx, cancel := context.WithDeadline(context.Background(), deadline)
defer cancel()
```

**3. Fan-out, Fan-in Pattern:**
```go
func generator(nums ...int) <-chan int {
    out := make(chan int)
    go func() {
        defer close(out)
        for _, n := range nums {
            out <- n
        }
    }()
    return out
}

func square(in <-chan int) <-chan int {
    out := make(chan int)
    go func() {
        defer close(out)
        for n := range in {
            out <- n * n
        }
    }()
    return out
}

func merge(cs ...<-chan int) <-chan int {
    var wg sync.WaitGroup
    out := make(chan int)
    
    output := func(c <-chan int) {
        defer wg.Done()
        for n := range c {
            out <- n
        }
    }
    
    wg.Add(len(cs))
    for _, c := range cs {
        go output(c)
    }
    
    go func() {
        wg.Wait()
        close(out)
    }()
    
    return out
}

func main() {
    in := generator(1, 2, 3, 4, 5)
    
    // Fan-out - distribusikan pekerjaan ke 3 worker
    c1 := square(in)
    c2 := square(in)
    c3 := square(in)
    
    // Fan-in - gabungkan hasil
    for n := range merge(c1, c2, c3) {
        fmt.Println(n)
    }
}
```

**Latihan Hari 11:**
1. Implementasikan request handling dengan context
2. Buat program dengan timeout handling
3. Implementasikan fan-out/fan-in pattern untuk komputasi paralel
4. Buat pipeline untuk pemrosesan data

### Hari 12: Interfaces

**1. Interface Basics:**
```go
// Mendefinisikan interface
type Shape interface {
    Area() float64
    Perimeter() float64
}

// Struct yang mengimplementasikan interface
type Rectangle struct {
    Width, Height float64
}

func (r Rectangle) Area() float64 {
    return r.Width * r.Height
}

func (r Rectangle) Perimeter() float64 {
    return 2 * (r.Width + r.Height)
}

// Struct lain yang mengimplementasikan interface
type Circle struct {
    Radius float64
}

func (c Circle) Area() float64 {
    return math.Pi * c.Radius * c.Radius
}

func (c Circle) Perimeter() float64 {
    return 2 * math.Pi * c.Radius
}

// Fungsi yang menerima interface
func printShapeInfo(s Shape) {
    fmt.Printf("Area: %.2f\n", s.Area())
    fmt.Printf("Perimeter: %.2f\n", s.Perimeter())
}

func main() {
    r := Rectangle{Width: 5, Height: 3}
    c := Circle{Radius: 2}
    
    printShapeInfo(r)
    printShapeInfo(c)
}
```

**2. Empty Interface:**
```go
// Empty interface dapat menampung nilai apapun
func printAny(v interface{}) {
    fmt.Printf("Tipe: %T, Nilai: %v\n", v, v)
}

func main() {
    printAny(42)
    printAny("hello")
    printAny(true)
}
```

**3. Type Assertions:**
```go
func main() {
    var i interface{} = "hello"
    
    // Type assertion
    s, ok := i.(string)
    if ok {
        fmt.Println(s)
    }
    
    // Type switch
    switch v := i.(type) {
    case string:
        fmt.Println("string:", v)
    case int:
        fmt.Println("int:", v)
    default:
        fmt.Printf("unknown type: %T\n", v)
    }
}
```

**Latihan Hari 12:**
1. Buat interface untuk sistem pembayaran
2. Implementasikan beberapa metode pembayaran
3. Buat generic handler menggunakan empty interface
4. Implementasikan type assertion untuk penanganan khusus

### Hari 13: File I/O dan JSON

**1. File Reading:**
```go
// Membaca seluruh file
data, err := ioutil.ReadFile("file.txt")
if err != nil {
    log.Fatal(err)
}
fmt.Println(string(data))

// Membaca file dengan bufio
file, err := os.Open("file.txt")
if err != nil {
    log.Fatal(err)
}
defer file.Close()

scanner := bufio.NewScanner(file)
for scanner.Scan() {
    fmt.Println(scanner.Text())
}
```

**2. File Writing:**
```go
// Menulis ke file
err := ioutil.WriteFile("output.txt", []byte("Hello Go"), 0644)
if err != nil {
    log.Fatal(err)
}

// Menulis dengan bufio
file, err := os.Create("output.txt")
if err != nil {
    log.Fatal(err)
}
defer file.Close()

writer := bufio.NewWriter(file)
_, err = writer.WriteString("Hello Go\n")
if err != nil {
    log.Fatal(err)
}
writer.Flush()
```

**3. JSON Marshalling:**
```go
type Person struct {
    Name  string `json:"name"`
    Age   int    `json:"age"`
    Email string `json:"email,omitempty"`
}

func main() {
    p := Person{Name: "John", Age: 30}
    
    // Struct ke JSON
    data, err := json.Marshal(p)
    if err != nil {
        log.Fatal(err)
    }
    fmt.Println(string(data))
    
    // Pretty print
    data, err = json.MarshalIndent(p, "", "  ")
    if err != nil {
        log.Fatal(err)
    }
    fmt.Println(string(data))
}
```

**4. JSON Unmarshalling:**
```go
jsonStr := `{"name":"John","age":30,"email":"john@example.com"}`

var p Person
err := json.Unmarshal([]byte(jsonStr), &p)
if err != nil {
    log.Fatal(err)
}
fmt.Printf("%+v\n", p)
```

**Latihan Hari 13:**
1. Buat aplikasi yang membaca dan menulis file konfigurasi
2. Implementasikan parser JSON untuk file konfigurasi
3. Buat struct yang sesuai dengan format JSON tertentu
4. Buat program untuk membaca dan menulis file log

### Hari 14: Database Access

**1. SQL Database Connection:**
```go
import (
    "database/sql"
    _ "github.com/go-sql-driver/mysql"
)

func main() {
    // Format: username:password@protocol(address)/dbname
    db, err := sql.Open("mysql", "user:password@tcp(127.0.0.1:3306)/testdb")
    if err != nil {
        log.Fatal(err)
    }
    defer db.Close()
    
    // Cek koneksi
    err = db.Ping()
    if err != nil {
        log.Fatal(err)
    }
    
    fmt.Println("Connected to database!")
}
```

**2. Query dan Scan:**
```go
// Query single row
var name string
var id int
err = db.QueryRow("SELECT id, name FROM users WHERE id = ?", 1).Scan(&id, &name)
if err != nil {
    log.Fatal(err)
}
fmt.Printf("ID: %d, Name: %s\n", id, name)

// Query multiple rows
rows, err := db.Query("SELECT id, name FROM users")
if err != nil {
    log.Fatal(err)
}
defer rows.Close()

for rows.Next() {
    var id int
    var name string
    err = rows.Scan(&id, &name)
    if err != nil {
        log.Fatal(err)
    }
    fmt.Printf("ID: %d, Name: %s\n", id, name)
}
```

**3. Prepared Statements:**
```go
// Prepared statement untuk insert
stmt, err := db.Prepare("INSERT INTO users(name, email) VALUES(?, ?)")
if err != nil {
    log.Fatal(err)
}
defer stmt.Close()

// Execute prepared statement
res, err := stmt.Exec("John Doe", "john@example.com")
if err != nil {
    log.Fatal(err)
}

lastID, err := res.LastInsertId()
if err != nil {
    log.Fatal(err)
}
fmt.Printf("Inserted user with ID: %d\n", lastID)
```

**4. Transactions:**
```go
// Begin transaction
tx, err := db.Begin()
if err != nil {
    log.Fatal(err)
}

// Execute statements within transaction
_, err = tx.Exec("UPDATE accounts SET balance = balance - ? WHERE id = ?", 100, 1)
if err != nil {
    tx.Rollback()
    log.Fatal(err)
}

_, err = tx.Exec("UPDATE accounts SET balance = balance + ? WHERE id = ?", 100, 2)
if err != nil {
    tx.Rollback()
    log.Fatal(err)
}

// Commit transaction
err = tx.Commit()
if err != nil {
    log.Fatal(err)
}
```

**Latihan Hari 14:**
1. Buat koneksi ke database MySQL atau PostgreSQL
2. Implementasikan CRUD operations
3. Buat program transfer dana dengan transactions
4. Buat repository pattern untuk akses database

### Hari 15: RESTful API Dasar

**1. Simple HTTP Server:**
```go
package main

import (
    "fmt"
    "log"
    "net/http"
)

func helloHandler(w http.ResponseWriter, r *http.Request) {
    fmt.Fprintf(w, "Hello, World!")
}

func main() {
    http.HandleFunc("/hello", helloHandler)
    
    fmt.Println("Server started at :8080")
    log.Fatal(http.ListenAndServe(":8080", nil))
}
```

**2. Request Handling:**
```go
func userHandler(w http.ResponseWriter, r *http.Request) {
    switch r.Method {
    case "GET":
        // Handle GET
        fmt.Fprintf(w, "Get User")
    case "POST":
        // Handle POST
        decoder := json.NewDecoder(r.Body)
        var user User
        err := decoder.Decode(&user)
        if err != nil {
            http.Error(w, err.Error(), http.StatusBadRequest)
            return
        }
        fmt.Fprintf(w, "Created user: %s", user.Name)
    default:
        http.Error(w, "Method not allowed", http.StatusMethodNotAllowed)
    }
}
```

**3. JSON Response:**
```go
type User struct {
    ID   int    `json:"id"`
    Name string `json:"name"`
}

func getUserHandler(w http.ResponseWriter, r *http.Request) {
    user := User{ID: 1, Name: "John Doe"}
    
    w.Header().Set("Content-Type", "application/json")
    json.NewEncoder(w).Encode(user)
}
```

**4. URL Parameters:**
```go
func main() {
    http.HandleFunc("/users/", func(w http.ResponseWriter, r *http.Request) {
        // Extract ID from URL like /users/123
        id := strings.TrimPrefix(r.URL.Path, "/users/")
        fmt.Fprintf(w, "User ID: %s", id)
    })
    
    log.Fatal(http.ListenAndServe(":8080", nil))
}
```

**Latihan Hari 15:**
1. Buat REST API sederhana dengan endpoint GET dan POST
2. Implementasikan handler untuk resource users dan products
3. Buat response dalam format JSON
4. Implementasikan routing dengan parameter

## Fase 2: Web Development dengan Go (Hari 16-30)

### Hari 16: Web Framework - Gin

**1. Setup Gin:**
```go
package main

import (
    "github.com/gin-gonic/gin"
    "net/http"
)

func main() {
    r := gin.Default()
    
    r.GET("/ping", func(c *gin.Context) {
        c.JSON(http.StatusOK, gin.H{
            "message": "pong",
        })
    })
    
    r.Run(":8080") // listen and serve on 0.0.0.0:8080
}
```

**2. Route Parameters:**
```go
r.GET("/users/:id", func(c *gin.Context) {
    id := c.Param("id")
    c.JSON(http.StatusOK, gin.H{
        "user_id": id,
    })
})

// Query parameters /search?name=john
r.GET("/search", func(c *gin.Context) {
    name := c.DefaultQuery("name", "Guest")
    c.JSON(http.StatusOK, gin.H{
        "name": name,
    })
})
```

**3. Request Binding:**
```go
type LoginForm struct {
    Username string `json:"username" binding:"required"`
    Password string `json:"password" binding:"required"`
}

r.POST("/login", func(c *gin.Context) {
    var form LoginForm
    if err := c.ShouldBindJSON(&form); err != nil {
        c.JSON(http.StatusBadRequest, gin.H{"error": err.Error()})
        return
    }
    
    // Validasi berhasil
    c.JSON(http.StatusOK, gin.H{
        "status": "logged in",
        "username": form.Username,
    })
})
```

**4. Middleware:**
```go
// Custom middleware
func Logger() gin.HandlerFunc {
    return func(c *gin.Context) {
        t := time.Now()
        
        // Set example variable
        c.Set("example", "12345")
        
        // before request
        c.Next()
        
        // after request
        latency := time.Since(t)
        log.Print(latency)
        
        // access status we are sending
        status := c.Writer.Status()
        log.Println(status)
    }
}

func main() {
    r := gin.New()
    r.Use(Logger())
    
    r.GET("/test", func(c *gin.Context) {
        example := c.MustGet("example").(string)
        
        c.JSON(http.StatusOK, gin.H{
            "example": example,
        })
    })
    
    r.Run(":8080")
}
```

**Latihan Hari 16:**
1. Buat REST API dengan Gin framework
2. Implementasikan routing dengan parameter
3. Buat validasi input dengan binding
4. Implementasikan custom middleware untuk logging

### Hari 17: Authentication dan Authorization

**1. Password Hashing:**
```go
import "golang.org/x/crypto/bcrypt"

// Hash password
func HashPassword(password string) (string, error) {
    bytes, err := bcrypt.GenerateFromPassword([]byte(password), bcrypt.DefaultCost)
    return string(bytes), err
}

// Check password
func CheckPasswordHash(password, hash string) bool {
    err := bcrypt.CompareHashAndPassword([]byte(hash), []byte(password))
    return err == nil
}
```

**2. JWT Authentication:**
```go
import "github.com/golang-jwt/jwt/v4"

var jwtKey = []byte("secret_key")

type Claims struct {
    UserID uint
    jwt.StandardClaims
}

// Generate token
func GenerateToken(userID uint) (string, error) {
    expirationTime := time.Now().Add(24 * time.Hour)
    claims := &Claims{
        UserID: userID,
        StandardClaims: jwt.StandardClaims{
            ExpiresAt: expirationTime.Unix(),
        },
    }
    
    token := jwt.NewWithClaims(jwt.SigningMethodHS256, claims)
    tokenString, err := token.SignedString(jwtKey)
    
    return tokenString, err
}

// Validate token
func ValidateToken(tokenString string) (*Claims, error) {
    claims := &Claims{}
    
    token, err := jwt.ParseWithClaims(tokenString, claims, func(token *jwt.Token) (interface{}, error) {
        return jwtKey, nil
    })
    
    if err != nil {
        return nil, err
    }
    
    if !token.Valid {
        return nil, errors.New("invalid token")
    }
    
    return claims, nil
}
```

**3. Middleware Auth dengan Gin:**
```go
func AuthMiddleware() gin.HandlerFunc {
    return func(c *gin.Context) {
        authHeader := c.GetHeader("Authorization")
        if authHeader == "" {
            c.AbortWithStatusJSON(http.StatusUnauthorized, gin.H{"error": "authorization header required"})
            return
        }
        
        // Ambil token dari header "Bearer <token>"
        tokenString := strings.Replace(authHeader, "Bearer ", "", 1)
        
        claims, err := ValidateToken(tokenString)
        if err != nil {
            c.AbortWithStatusJSON(http.StatusUnauthorized, gin.H{"error": "invalid token"})
            return
        }
        
        // Set user ID to context
        c.Set("userID", claims.UserID)
        c.Next()
    }
}

// Menggunakan middleware
func main() {
    r := gin.Default()
    
    public := r.Group("/api")
    {
        public.POST("/login", LoginHandler)
        public.POST("/register", RegisterHandler)
    }
    
    // Protected routes
    protected := r.Group("/api/protected")
    protected.Use(AuthMiddleware())
    {
        protected.GET("/profile", ProfileHandler)
    }
    
    r.Run(":8080")
}
```

**4. RBAC (Role-Based Access Control):**
```go
type User struct {
    ID    uint
    Email string
    Role  string // "admin", "user", etc.
}

func RoleMiddleware(roles ...string) gin.HandlerFunc {
    return func(c *gin.Context) {
        userID, exists := c.Get("userID")
        if !exists {
            c.AbortWithStatusJSON(http.StatusUnauthorized, gin.H{"error": "unauthorized"})
            return
        }
        
        // Get user from database
        var user User
        if err := db.First(&user, userID).Error; err != nil {
            c.AbortWithStatusJSON(http.StatusUnauthorized, gin.H{"error": "user not found"})
            return
        }
        
        // Check if user has required role
        hasRole := false
        for _, role := range roles {
            if user.Role == role {
                hasRole = true
                break
            }
        }
        
        if !hasRole {
            c.AbortWithStatusJSON(http.StatusForbidden, gin.H{"error": "permission denied"})
            return
        }
        
        c.Next()
    }
}

// Penggunaan
protected.GET("/admin", RoleMiddleware("admin"), AdminHandler)
```

**Latihan Hari 17:**
1. Implementasikan sistem autentikasi dengan JWT
2. Buat middleware untuk validasi token
3. Implementasikan sistem RBAC sederhana
4. Buat endpoint login dan register

### Hari 18: Validasi Input

**1. Validasi dengan Struct Tags:**
```go
import "github.com/go-playground/validator/v10"

type RegisterRequest struct {
    Username string `json:"username" binding:"required,min=3,max=20"`
    Email    string `json:"email" binding:"required,email"`
    Password string `json:"password" binding:"required,min=8"`
    Age      int    `json:"age" binding:"required,gte=18"`
}

func RegisterHandler(c *gin.Context) {
    var req RegisterRequest
    if err := c.ShouldBindJSON(&req); err != nil {
        c.JSON(http.StatusBadRequest, gin.H{"error": err.Error()})
        return
    }
    
    // Validasi berhasil
    c.JSON(http.StatusOK, gin.H{"message": "registration success"})
}
```

**2. Custom Validation:**
```go
type User struct {
    FirstName string `json:"first_name" binding:"required"`
    LastName  string `json:"last_name" binding:"required"`
    Email     string `json:"email" binding:"required,email"`
    Password  string `json:"password" binding:"required,min=8,validatePassword"`
}

// Custom validator
func validatePassword(fl validator.FieldLevel) bool {
    password := fl.Field().String()
    
    // Check for at least one uppercase letter
    hasUpper := false
    for _, c := range password {
        if unicode.IsUpper(c) {
            hasUpper = true
            break
        }
    }
    
    // Check for at least one number
    hasNumber := false
    for _, c := range password {
        if unicode.IsDigit(c) {
            hasNumber = true
            break
        }
    }
    
    return hasUpper && hasNumber
}

func main() {
    r := gin.Default()
    
    validate := validator.New()
    validate.RegisterValidation("validatePassword", validatePassword)
    
    // ...
}
```

**3. Error Handling untuk Validasi:**
```go
func CustomErrorHandler() gin.HandlerFunc {
    return func(c *gin.Context) {
        c.Next()
        
        // Only handle validation errors
        if len(c.Errors) > 0 {
            for _, e := range c.Errors {
                if errs, ok := e.Err.(validator.ValidationErrors); ok {
                    var errorMessages []string
                    for _, err := range errs {
                        errorMessages = append(errorMessages, formatValidationError(err))
                    }
                    c.JSON(http.StatusBadRequest, gin.H{"errors": errorMessages})
                    return
                }
            }
        }
    }
}

func formatValidationError(err validator.FieldError) string {
    field := err.Field()
    tag := err.Tag()
    
    switch tag {
    case "required":
        return fmt.Sprintf("%s is required", field)
    case "email":
        return fmt.Sprintf("%s must be a valid email", field)
    case "min":
        return fmt.Sprintf("%s must be at least %s characters", field, err.Param())
    // more cases...
    default:
        return fmt.Sprintf("%s is invalid", field)
    }
}
```

**4. Sanitasi Input:**
```go
import "github.com/microcosm-cc/bluemonday"

func SanitizeHandler(c *gin.Context) {
    var req struct {
        Content string `json:"content"`
    }
    
    if err := c.ShouldBindJSON(&req); err != nil {
        c.JSON(http.StatusBadRequest, gin.H{"error": err.Error()})
        return
    }
    
    // Sanitize HTML content
    p := bluemonday.UGCPolicy()
    sanitized := p.Sanitize(req.Content)
    
    c.JSON(http.StatusOK, gin.H{"sanitized": sanitized})
}
```

**Latihan Hari 18:**
1. Implementasikan validasi untuk form register dan login
2. Buat custom validator untuk format nomor telepon
3. Implementasikan error handling untuk validasi
4. Buat sanitasi untuk input user-generated content

### Hari 19: ORM dengan GORM

**1. Setup GORM:**
```go
import (
    "gorm.io/driver/mysql"
    "gorm.io/gorm"
)

func main() {
    dsn := "user:password@tcp(127.0.0.1:3306)/dbname?charset=utf8mb4&parseTime=True&loc=Local"
    db, err := gorm.Open(mysql.Open(dsn), &gorm.Config{})
    if err != nil {
        panic("failed to connect database")
    }
    
    // Auto migrate models
    db.AutoMigrate(&User{}, &Product{})
}
```

**2. Define Models:**
```go
type User struct {
    gorm.Model
    Name     string
    Email    string `gorm:"uniqueIndex"`
    Age      int
    Password string `gorm:"-"` // Tidak disimpan ke database
    Products []Product
}

type Product struct {
    gorm.Model
    Name        string
    Price       float64
    Description string
    UserID      uint
}
```

**3. CRUD Operations:**
```go
// Create
user := User{Name: "John", Email: "john@example.com", Age: 30}
result := db.Create(&user)
if result.Error != nil {
    // Handle error
}
fmt.Println(user.ID) // ID setelah diinsert

// Read
var user User
db.First(&user, 1) // find user with id 1
db.First(&user, "email = ?", "john@example.com") // find user with email

// Update
db.Model(&user).Updates(User{Name: "New Name", Age: 31})
// OR update specific fields
db.Model(&user).Updates(map[string]interface{}{"Name": "New Name", "Age": 31})

// Delete
db.Delete(&user, 1) // Soft delete user with id 1
```

**4. Associations dan Query:**
```go
// Preloading
var users []User
db.Preload("Products").Find(&users)

// Joins
db.Joins("JOIN products ON products.user_id = users.id").Find(&users)

// Where conditions
db.Where("age > ?", 20).Find(&users)
db.Where("name LIKE ?", "%jin%").Find(&users)

// Order & Limit
db.Order("age desc").Limit(10).Find(&users)

// Group & Having
type Result struct {
    Age   int
    Count int
}
var results []Result
db.Model(&User{}).Select("age, count(*) as count").Group("age").Having("count > ?", 1).Find(&results)
```

**Latihan Hari 19:**
1. Setup database dengan GORM
2. Implementasikan model dengan associations
3. Buat CRUD operations untuk models
4. Implementasikan query lanjutan dengan joins dan aggregations

### Hari 20: File Upload dan Serving

**1. File Upload dengan Gin:**
```go
func uploadHandler(c *gin.Context) {
    // Single file
    file, err := c.FormFile("file")
    if err != nil {
        c.JSON(http.StatusBadRequest, gin.H{"error": err.Error()})
        return
    }
    
    // Set destination path
    dst := fmt.Sprintf("uploads/%s", file.Filename)
    
    // Save file
    if err := c.SaveUploadedFile(file, dst); err != nil {
        c.JSON(http.StatusInternalServerError, gin.H{"error": err.Error()})
        return
    }
    
    c.JSON(http.StatusOK, gin.H{"filepath": dst})
}
```

**2. Multiple Files Upload:**
```go
func multiUploadHandler(c *gin.Context) {
    form, err := c.MultipartForm()
    if err != nil {
        c.JSON(http.StatusBadRequest, gin.H{"error": err.Error()})
        return
    }
    
    files := form.File["files"]
    
    var paths []string
    for _, file := range files {
        dst := fmt.Sprintf("uploads/%s", file.Filename)
        if err := c.SaveUploadedFile(file, dst); err != nil {
            c.JSON(http.StatusInternalServerError, gin.H{"error": err.Error()})
            return
        }
        paths = append(paths, dst)
    }
    
    c.JSON(http.StatusOK, gin.H{"filepaths": paths})
}
```

**3. Serving Static Files:**
```go
func main() {
    r := gin.Default()
    
    // Serve files from ./uploads directory
    r.Static("/files", "./uploads")
    
    // OR serve a single file
    r.StaticFile("/favicon.ico", "./resources/favicon.ico")
    
    r.Run(":8080")
}
```

**4. File Validation:**
```go
func uploadHandler(c *gin.Context) {
    file, err := c.FormFile("file")
    if err != nil {
        c.JSON(http.StatusBadRequest, gin.H{"error": err.Error()})
        return
    }
    
    // Validate file size
    if file.Size > 10*1024*1024 { // 10MB
        c.JSON(http.StatusBadRequest, gin.H{"error": "file too large"})
        return
    }
    
    // Validate file type
    ext := filepath.Ext(file.Filename)
    allowedExts := map[string]bool{".jpg": true, ".jpeg": true, ".png": true}
    if !allowedExts[strings.ToLower(ext)] {
        c.JSON(http.StatusBadRequest, gin.H{"error": "invalid file type"})
        return
    }
    
    // Generate unique filename
    filename := fmt.Sprintf("%d%s", time.Now().UnixNano(), ext)
    dst := filepath.Join("uploads", filename)
    
    if err := c.SaveUploadedFile(file, dst); err != nil {
        c.JSON(http.StatusInternalServerError, gin.H{"error": err.Error()})
        return
    }
    
    c.JSON(http.StatusOK, gin.H{"filepath": dst})
}
```

**Latihan Hari 20:**
1. Implementasikan endpoint untuk file upload
2. Buat validasi untuk ukuran dan tipe file
3. Implementasikan multiple files upload
4. Buat sistem untuk serving static files

### Hari 21: API Documentation dengan Swagger

**1. Setup Swagger:**
```go
// main.go
package main

import (
    "github.com/gin-gonic/gin"
    swaggerFiles "github.com/swaggo/files"
    ginSwagger "github.com/swaggo/gin-swagger"
    _ "myapp/docs" // Import docs
)

// @title API Documentation
// @version 1.0
// @description This is a sample API server.
// @host localhost:8080
// @BasePath /api
func main() {
    r := gin.Default()
    
    // Swagger documentation
    r.GET("/swagger/*any", ginSwagger.WrapHandler(swaggerFiles.Handler))
    
    // API routes
    api := r.Group("/api")
    {
        api.GET("/users", getUsers)
    }
    
    r.Run(":8080")
}
```

**2. Document API Endpoints:**
```go
// @Summary Get all users
// @Description Get a list of all users
// @Tags users
// @Accept json
// @Produce json
// @Success 200 {array} User
// @Failure 500 {object} ErrorResponse
// @Router /users [get]
func getUsers(c *gin.Context) {
    var users []User
    if err := db.Find(&users).Error; err != nil {
        c.JSON(http.StatusInternalServerError, gin.H{"error": err.Error()})
        return
    }
    
    c.JSON(http.StatusOK, users)
}
```

**3. Document Models:**
```go
// @Description User information
type User struct {
    ID        uint      `json:"id" gorm:"primaryKey"`
    Name      string    `json:"name" binding:"required"`
    Email     string    `json:"email" binding:"required,email"`
    CreatedAt time.Time `json:"created_at"`
}

// @Description Error response
type ErrorResponse struct {
    Error string `json:"error"`
}
```

**4. Document Authentication:**
```go
// @Summary Login user
// @Description Authenticate a user and get token
// @Tags auth
// @Accept json
// @Produce json
// @Param loginInput body LoginRequest true "Login Information"
// @Success 200 {object} TokenResponse
// @Failure 400 {object} ErrorResponse
// @Failure 401 {object} ErrorResponse
// @Router /login [post]
func login(c *gin.Context) {
    // ...
}

// @Description Login request
type LoginRequest struct {
    Email    string `json:"email" binding:"required,email"`
    Password string `json:"password" binding:"required"`
}

// @Description Token response
type TokenResponse struct {
    Token string `json:"token"`
}
```

**Latihan Hari 21:**
1. Setup Swagger untuk API documentation
2. Document semua endpoints yang sudah dibuat
3. Document models dan responses
4. Jalankan dan test Swagger UI

### Hari 22: Rate Limiting dan Caching

**1. Rate Limiting dengan Redis:**
```go
import (
    "github.com/gin-gonic/gin"
    "github.com/go-redis/redis/v8"
    "github.com/go-redis/redis_rate/v9"
    "golang.org/x/net/context"
)

func RateLimiterMiddleware(rdb *redis.Client) gin.HandlerFunc {
    limiter := redis_rate.NewLimiter(rdb)
    
    return func(c *gin.Context) {
        // Get client IP
        key := c.ClientIP()
        
        // Create context
        ctx := context.Background()
        
        // Allow 10 requests per minute
        res, err := limiter.Allow(ctx, key, redis_rate.PerMinute(10))
        if err != nil {
            c.AbortWithStatusJSON(http.StatusInternalServerError, gin.H{
                "error": "rate limitter error",
            })
            return
        }
        
        // Set RateLimit headers
        c.Header("X-RateLimit-Limit", "10")
        c.Header("X-RateLimit-Remaining", strconv.Itoa(res.Remaining))
        
        if res.Allowed == 0 {
            c.AbortWithStatusJSON(http.StatusTooManyRequests, gin.H{
                "error": "too many requests",
            })
            return
        }
        
        c.Next()
    }
}
```

**2. In-Memory Caching dengan go-cache:**
```go
import (
    "github.com/gin-gonic/gin"
    "github.com/patrickmn/go-cache"
    "time"
)

var memoryCache *cache.Cache

func init() {
    // Create a cache with 5 minute default expiration and 10 minute cleanup interval
    memoryCache = cache.New(5*time.Minute, 10*time.Minute)
}

func CacheMiddleware() gin.HandlerFunc {
    return func(c *gin.Context) {
        // Skip cache for non-GET methods
        if c.Request.Method != "GET" {
            c.Next()
            return
        }
        
        // Generate cache key from full request URL
        key := c.Request.URL.String()
        
        // Try to get cached response
        if response, found := memoryCache.Get(key); found {
            c.JSON(http.StatusOK, response)
            c.Abort()
            return
        }
        
        // Store the response data
        c.Writer = &cacheWriter{ResponseWriter: c.Writer, body: &bytes.Buffer{}}
        
        c.Next()
        
        // Cache the response
        if c.Writer.Status