# Modul Pembelajaran Golang: Pemula hingga Expert

## Fase 1: Dasar-Dasar Golang (Hari 1-15)

### Modul 1: Pengenalan dan Setup (Hari 1-3)

#### Materi 1.1: Pengenalan Golang
- **Definisi**: Golang adalah bahasa pemrograman open source yang dibuat oleh Google, dirancang untuk efisiensi, kesederhanaan, dan keamanan.
- **Kelebihan Golang**:
  - Kompilasi cepat
  - Concurrent programming bawaan (goroutines)
  - Garbage collection otomatis
  - Static typing dengan sintaks simpel
  - Standar library yang kaya
  - Cross-platform

#### Materi 1.2: Instalasi dan Setup Workspace
- **Instalasi**:
  ```bash
  # Download dari golang.org
  # Verifikasi instalasi
  go version
  ```
- **Go Modules**:
  ```bash
  # Buat proyek baru
  mkdir myproject
  cd myproject
  go mod init github.com/username/myproject
  ```
- **Tools Development**:
  - Visual Studio Code + Go extension
  - GoLand
  - Atom dengan go-plus

#### Materi 1.3: Program Go Pertama
- **Struktur dasar**:
  ```go
  package main
  
  import "fmt"
  
  func main() {
      fmt.Println("Hello, Golang!")
  }
  ```
- **Kompilasi dan Eksekusi**:
  ```bash
  # Mode langsung
  go run hello.go
  
  # Mode kompilasi
  go build hello.go
  ./hello
  ```

### Modul 2: Dasar Pemrograman Go (Hari 4-6)

#### Materi 2.1: Variabel dan Tipe Data
- **Deklarasi Variabel**:
  ```go
  // Eksplisit
  var nama string = "Budi"
  
  // Implisit
  var umur = 25
  
  // Short declaration
  kota := "Jakarta"
  ```
- **Tipe Data Dasar**:
  - Boolean: `bool`
  - String: `string`
  - Numerik: `int`, `float64`, dll.
  - Byte: `byte` (alias dari uint8)
  - Rune: `rune` (alias dari int32)

#### Materi 2.2: Operator dan Control Flow
- **Operator**:
  - Aritmatika: `+`, `-`, `*`, `/`, `%`
  - Perbandingan: `==`, `!=`, `<`, `>`, `<=`, `>=`
  - Logika: `&&`, `||`, `!`
- **Struktur Kendali**:
  ```go
  // If-else
  if nilai >= 60 {
      fmt.Println("Lulus")
  } else {
      fmt.Println("Tidak Lulus")
  }
  
  // Switch
  switch hari {
  case "Senin":
      fmt.Println("Awal minggu")
  case "Jumat":
      fmt.Println("Akhir minggu kerja")
  default:
      fmt.Println("Hari biasa")
  }
  
  // For loop (satu-satunya jenis loop di Go)
  for i := 0; i < 5; i++ {
      fmt.Println(i)
  }
  ```

#### Materi 2.3: Array dan Slice
- **Array** (ukuran tetap):
  ```go
  var numbers [5]int
  primes := [5]int{2, 3, 5, 7, 11}
  ```
- **Slice** (ukuran dinamis):
  ```go
  fruits := []string{"apple", "banana", "orange"}
  numbers := make([]int, 5, 10) // len 5, cap 10
  
  // Operasi slice
  slice = append(slice, 10)
  newSlice := slice[1:3]
  ```

### Modul 3: Konsep Dasar Lanjutan (Hari 7-9)

#### Materi 3.1: Maps dan Structs
- **Maps** (key-value pairs):
  ```go
  scores := map[string]int{
      "Alice": 90,
      "Bob":   85,
  }
  
  // Operasi map
  scores["Carol"] = 95
  delete(scores, "Bob")
  score, exists := scores["Alice"]
  ```
- **Structs** (custom types):
  ```go
  type Person struct {
      Name     string
      Age      int
      Address  string
  }
  
  // Instantiate
  p := Person{Name: "Andi", Age: 30, Address: "Jakarta"}
  fmt.Println(p.Name) // Access field
  ```

#### Materi 3.2: Pointers
- **Pointer Basics**:
  ```go
  x := 10
  var p *int = &x  // p menyimpan alamat memori x
  fmt.Println(*p)  // Dereferencing: mengakses nilai dari alamat
  *p = 20          // Mengubah nilai x melalui pointer
  ```
- **Pointer dengan Struct**:
  ```go
  func updatePerson(p *Person) {
      p.Age = p.Age + 1  // Shorthand untuk (*p).Age
  }
  ```

#### Materi 3.3: Functions dan Methods
- **Function Basics**:
  ```go
  func add(a, b int) int {
      return a + b
  }
  
  // Multiple return values
  func divide(a, b float64) (float64, error) {
      if b == 0 {
          return 0, errors.New("pembagian dengan nol")
      }
      return a / b, nil
  }
  ```
- **Methods** (functions dengan receiver):
  ```go
  type Rectangle struct {
      Width, Height float64
  }
  
  // Method dengan receiver by value
  func (r Rectangle) Area() float64 {
      return r.Width * r.Height
  }
  
  // Method dengan receiver by pointer
  func (r *Rectangle) Scale(factor float64) {
      r.Width *= factor
      r.Height *= factor
  }
  ```

### Modul 4: Error Handling dan Testing (Hari 10-12)

#### Materi 4.1: Error Handling
- **Error Basics**:
  ```go
  // Return error
  if err != nil {
      return nil, err
  }
  
  // Creating errors
  errors.New("error message")
  fmt.Errorf("error: %v", value)
  ```
- **Custom Errors**:
  ```go
  type ValidationError struct {
      Field   string
      Message string
  }
  
  func (e *ValidationError) Error() string {
      return fmt.Sprintf("%s: %s", e.Field, e.Message)
  }
  ```

#### Materi 4.2: Panic dan Recover
- **Panic** (untuk error fatal):
  ```go
  if critical {
      panic("aplikasi tidak dapat dilanjutkan")
  }
  ```
- **Recover** (menangkap panic):
  ```go
  defer func() {
      if r := recover(); r != nil {
          fmt.Println("Recovered:", r)
      }
  }()
  ```

#### Materi 4.3: Testing
- **Unit Testing**:
  ```go
  // math.go
  func Add(a, b int) int {
      return a + b
  }
  
  // math_test.go
  func TestAdd(t *testing.T) {
      result := Add(2, 3)
      if result != 5 {
          t.Errorf("Add(2, 3) = %d; want 5", result)
      }
  }
  ```
- **Running Tests**:
  ```bash
  go test
  go test -v  # Verbose
  go test -cover  # Test coverage
  ```

### Modul 5: Concurrency Dasar (Hari 13-15)

#### Materi 5.1: Goroutines
- **Goroutine Basics**:
  ```go
  // Start a goroutine
  go func() {
      fmt.Println("Hello from goroutine!")
  }()
  
  // Allow time for goroutine to execute
  time.Sleep(time.Second)
  ```

#### Materi 5.2: Channels
- **Channel Basics**:
  ```go
  // Membuat channel
  ch := make(chan int)
  
  // Send value (dalam goroutine)
  go func() {
      ch <- 42  // Send value to channel
  }()
  
  // Receive value
  value := <-ch
  fmt.Println(value)
  
  // Buffered channel
  bufCh := make(chan int, 3)
  ```

#### Materi 5.3: Synchronization
- **WaitGroups**:
  ```go
  var wg sync.WaitGroup
  
  for i := 0; i < 5; i++ {
      wg.Add(1)  // Increment counter
      go func(id int) {
          defer wg.Done()  // Decrement counter
          fmt.Printf("Worker %d done\n", id)
      }(i)
  }
  
  wg.Wait()  // Wait for all goroutines
  ```
- **Select Statement**:
  ```go
  select {
  case msg := <-ch1:
      fmt.Println("Received from ch1:", msg)
  case msg := <-ch2:
      fmt.Println("Received from ch2:", msg)
  case <-time.After(time.Second):
      fmt.Println("Timeout")
  }
  ```

## Fase 2: Web Development dengan Go (Hari 16-30)

### Modul 6: Dasar Web Development (Hari 16-18)

#### Materi 6.1: HTTP Server Dasar
- **Server Sederhana**:
  ```go
  package main
  
  import (
      "fmt"
      "net/http"
  )
  
  func handler(w http.ResponseWriter, r *http.Request) {
      fmt.Fprintf(w, "Hello, %s!", r.URL.Path[1:])
  }
  
  func main() {
      http.HandleFunc("/", handler)
      http.ListenAndServe(":8080", nil)
  }
  ```
- **HTTP Methods**:
  ```go
  func handler(w http.ResponseWriter, r *http.Request) {
      if r.Method == "GET" {
          // Handle GET
      } else if r.Method == "POST" {
          // Handle POST
      }
  }
  ```

#### Materi 6.2: Routing
- **Basic Routing**:
  ```go
  http.HandleFunc("/", homeHandler)
  http.HandleFunc("/about", aboutHandler)
  http.HandleFunc("/contact", contactHandler)
  ```
- **URL Parameters**:
  ```go
  http.HandleFunc("/users/", func(w http.ResponseWriter, r *http.Request) {
      id := strings.TrimPrefix(r.URL.Path, "/users/")
      fmt.Fprintf(w, "User ID: %s", id)
  })
  ```

#### Materi 6.3: Serving Static Files
- **Static File Server**:
  ```go
  // Serve files from ./static directory
  fs := http.FileServer(http.Dir("./static"))
  http.Handle("/static/", http.StripPrefix("/static/", fs))
  ```

### Modul 7: REST API Development (Hari 19-21)

#### Materi 7.1: JSON Handling
- **JSON Marshalling/Unmarshalling**:
  ```go
  // Struct to JSON
  type Person struct {
      Name  string `json:"name"`
      Age   int    `json:"age"`
      Email string `json:"email,omitempty"`
  }
  
  p := Person{Name: "John", Age: 30}
  jsonData, err := json.Marshal(p)
  
  // JSON to Struct
  var newPerson Person
  err = json.Unmarshal(jsonData, &newPerson)
  ```
- **JSON Response**:
  ```go
  func userHandler(w http.ResponseWriter, r *http.Request) {
      user := Person{Name: "John", Age: 30}
      
      w.Header().Set("Content-Type", "application/json")
      json.NewEncoder(w).Encode(user)
  }
  ```

#### Materi 7.2: Building REST API
- **API Endpoints**:
  ```go
  // GET /users
  http.HandleFunc("/users", func(w http.ResponseWriter, r *http.Request) {
      if r.Method != "GET" {
          http.Error(w, "Method not allowed", http.StatusMethodNotAllowed)
          return
      }
      
      // Return user list
      users := []Person{
          {Name: "John", Age: 30},
          {Name: "Jane", Age: 25},
      }
      
      w.Header().Set("Content-Type", "application/json")
      json.NewEncoder(w).Encode(users)
  })
  ```
- **Request Parsing**:
  ```go
  // POST /users
  http.HandleFunc("/users", func(w http.ResponseWriter, r *http.Request) {
      if r.Method != "POST" {
          http.Error(w, "Method not allowed", http.StatusMethodNotAllowed)
          return
      }
      
      var newUser Person
      err := json.NewDecoder(r.Body).Decode(&newUser)
      if err != nil {
          http.Error(w, err.Error(), http.StatusBadRequest)
          return
      }
      
      // Process newUser...
      w.WriteHeader(http.StatusCreated)
  })
  ```

#### Materi 7.3: HTTP Middleware
- **Middleware Pattern**:
  ```go
  func loggingMiddleware(next http.Handler) http.Handler {
      return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
          // Log before request
          fmt.Printf("Request: %s %s\n", r.Method, r.URL.Path)
          
          // Call the next handler
          next.ServeHTTP(w, r)
          
          // Log after request
          fmt.Println("Request completed")
      })
  }
  
  // Usage
  handler := http.HandlerFunc(myHandler)
  http.Handle("/", loggingMiddleware(handler))
  ```

### Modul 8: Database Interaction (Hari 22-24)

#### Materi 8.1: SQL Database Connection
- **Connecting to Database**:
  ```go
  import (
      "database/sql"
      _ "github.com/go-sql-driver/mysql"
  )
  
  func main() {
      db, err := sql.Open("mysql", "user:password@tcp(127.0.0.1:3306)/dbname")
      if err != nil {
          log.Fatal(err)
      }
      defer db.Close()
      
      // Test connection
      err = db.Ping()
      if err != nil {
          log.Fatal(err)
      }
  }
  ```

#### Materi 8.2: CRUD Operations
- **Query dan Execute**:
  ```go
  // SELECT
  rows, err := db.Query("SELECT id, name FROM users WHERE age > ?", 18)
  if err != nil {
      log.Fatal(err)
  }
  defer rows.Close()
  
  for rows.Next() {
      var id int
      var name string
      err = rows.Scan(&id, &name)
      // Process data...
  }
  
  // INSERT
  result, err := db.Exec("INSERT INTO users (name, age) VALUES (?, ?)", "John", 30)
  if err != nil {
      log.Fatal(err)
  }
  
  id, err := result.LastInsertId()
  ```
- **Prepared Statements**:
  ```go
  stmt, err := db.Prepare("INSERT INTO users(name, age) VALUES(?, ?)")
  if err != nil {
      log.Fatal(err)
  }
  defer stmt.Close()
  
  for _, user := range users {
      _, err := stmt.Exec(user.Name, user.Age)
      // Handle error...
  }
  ```

#### Materi 8.3: Database Migrations
- **Migration Tool**: golang-migrate
  ```bash
  # Create migration
  migrate create -ext sql -dir migrations -seq create_users_table
  
  # Run migrations
  migrate -database "mysql://user:password@tcp(localhost:3306)/dbname" -path migrations up
  ```
- **Sample Migration**:
  ```sql
  -- migrations/000001_create_users_table.up.sql
  CREATE TABLE users (
      id INT AUTO_INCREMENT PRIMARY KEY,
      name VARCHAR(255) NOT NULL,
      age INT,
      created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
  );
  
  -- migrations/000001_create_users_table.down.sql
  DROP TABLE users;
  ```

### Modul 9: Validasi dan Autentikasi (Hari 25-27)

#### Materi 9.1: Input Validation
- **Validasi Dasar**:
  ```go
  func validateUser(user User) error {
      if user.Name == "" {
          return errors.New("name cannot be empty")
      }
      if user.Age < 0 || user.Age > 150 {
          return errors.New("invalid age")
      }
      return nil
  }
  ```
- **Validasi dengan Library**: validator
  ```go
  import "github.com/go-playground/validator/v10"
  
  type User struct {
      Name  string `validate:"required,min=3,max=50"`
      Email string `validate:"required,email"`
      Age   int    `validate:"gte=0,lte=130"`
  }
  
  func validateUser(user User) error {
      validate := validator.New()
      return validate.Struct(user)
  }
  ```

#### Materi 9.2: Password Hashing
- **Bcrypt**:
  ```go
  import "golang.org/x/crypto/bcrypt"
  
  // Hash password
  hashedPassword, err := bcrypt.GenerateFromPassword([]byte(password), bcrypt.DefaultCost)
  if err != nil {
      return err
  }
  
  // Verify password
  err = bcrypt.CompareHashAndPassword(hashedPassword, []byte(inputPassword))
  if err == nil {
      // Password correct
  } else {
      // Password incorrect
  }
  ```

#### Materi 9.3: JWT Authentication
- **JWT Token Generation**:
  ```go
  import "github.com/golang-jwt/jwt/v4"
  
  // Create token
  claims := jwt.MapClaims{
      "user_id": 123,
      "exp":     time.Now().Add(time.Hour * 24).Unix(),
  }
  token := jwt.NewWithClaims(jwt.SigningMethodHS256, claims)
  tokenString, err := token.SignedString([]byte("your-secret-key"))
  
  // Verify token
  token, err := jwt.Parse(tokenString, func(token *jwt.Token) (interface{}, error) {
      return []byte("your-secret-key"), nil
  })
  
  if claims, ok := token.Claims.(jwt.MapClaims); ok && token.Valid {
      userId := claims["user_id"].(float64)
      // Use userId...
  }
  ```
- **JWT Middleware**:
  ```go
  func jwtMiddleware(next http.Handler) http.Handler {
      return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
          tokenString := r.Header.Get("Authorization")
          // Verify token...
          
          if !tokenValid {
              http.Error(w, "Unauthorized", http.StatusUnauthorized)
              return
          }
          
          next.ServeHTTP(w, r)
      })
  }
  ```

### Modul 10: Frameworks dan Toolkits (Hari 28-30)

#### Materi 10.1: Gin Framework
- **Setup Dasar**:
  ```go
  import "github.com/gin-gonic/gin"
  
  func main() {
      r := gin.Default() // Includes logger and recovery middleware
      
      r.GET("/ping", func(c *gin.Context) {
          c.JSON(200, gin.H{
              "message": "pong",
          })
      })
      
      r.Run(":8080")
  }
  ```
- **Route Parameters**:
  ```go
  r.GET("/users/:id", func(c *gin.Context) {
      id := c.Param("id")
      c.JSON(200, gin.H{"id": id})
  })
  ```
- **Query Parameters**:
  ```go
  r.GET("/users", func(c *gin.Context) {
      name := c.DefaultQuery("name", "Guest")
      c.String(200, "Hello %s", name)
  })
  ```

#### Materi 10.2: Echo Framework
- **Setup Dasar**:
  ```go
  import "github.com/labstack/echo/v4"
  
  func main() {
      e := echo.New()
      
      e.GET("/", func(c echo.Context) error {
          return c.String(http.StatusOK, "Hello, World!")
      })
      
      e.Logger.Fatal(e.Start(":8080"))
  }
  ```
- **Request Binding**:
  ```go
  type User struct {
      Name  string `json:"name" form:"name"`
      Email string `json:"email" form:"email"`
  }
  
  e.POST("/users", func(c echo.Context) error {
      u := new(User)
      if err := c.Bind(u); err != nil {
          return err
      }
      return c.JSON(http.StatusCreated, u)
  })
  ```

#### Materi 10.3: Fiber Framework
- **Setup Dasar**:
  ```go
  import "github.com/gofiber/fiber/v2"
  
  func main() {
      app := fiber.New()
      
      app.Get("/", func(c *fiber.Ctx) error {
          return c.SendString("Hello, World!")
      })
      
      app.Listen(":8080")
  }
  ```
- **Static Files**:
  ```go
  app.Static("/", "./public")
  ```
- **Grouping Routes**:
  ```go
  api := app.Group("/api")
  
  api.Get("/users", getUsers)
  api.Post("/users", createUser)
  ```

## Fase 3: Backend Development Lanjutan (Hari 31-45)

### Modul 11: Authentication Lanjutan (Hari 31-33)

#### Materi 11.1: OAuth 2.0
- **Implementasi OAuth Client**:
  ```go
  import "golang.org/x/oauth2"
  
  // Setup OAuth config
  conf := &oauth2.Config{
      ClientID:     "YOUR_CLIENT_ID",
      ClientSecret: "YOUR_CLIENT_SECRET",
      RedirectURL:  "http://localhost:8080/callback",
      Scopes:       []string{"profile", "email"},
      Endpoint: oauth2.Endpoint{
          AuthURL:  "https://provider.com/o/oauth2/auth",
          TokenURL: "https://provider.com/o/oauth2/token",
      },
  }
  
  // Generate auth URL
  url := conf.AuthCodeURL("state", oauth2.AccessTypeOffline)
  
  // Exchange code for token
  token, err := conf.Exchange(ctx, code)
  ```

#### Materi 11.2: Multi-Factor Authentication (MFA)
- **TOTP Implementation** (Time-based One-Time Password):
  ```go
  import "github.com/pquerna/otp/totp"
  
  // Generate new TOTP key
  key, err := totp.Generate(totp.GenerateOpts{
      Issuer:      "YourApp",
      AccountName: "user@example.com",
  })
  
  // Get provisioning URI for QR code
  uri := key.URL()
  
  // Validate TOTP
  valid := totp.Validate(userInputCode, key.Secret())
  if valid {
      // Code is valid
  }
  ```

#### Materi 11.3: Role-Based Access Control (RBAC)
- **RBAC Model**:
  ```go
  type Role string
  
  const (
      RoleAdmin  Role = "admin"
      RoleEditor Role = "editor"
      RoleViewer Role = "viewer"
  )
  
  type User struct {
      ID    int
      Name  string
      Roles []Role
  }
  
  func hasRole(user User, role Role) bool {
      for _, r := range user.Roles {
          if r == role {
              return true
          }
      }
      return false
  }
  ```
- **RBAC Middleware**:
  ```go
  func roleMiddleware(role Role) gin.HandlerFunc {
      return func(c *gin.Context) {
          // Get user from context after authentication
          user := getUserFromContext(c)
          
          if !hasRole(user, role) {
              c.AbortWithStatusJSON(http.StatusForbidden, gin.H{
                  "error": "insufficient permissions",
              })
              return
          }
          
          c.Next()
      }
  }
  
  // Usage
  r.GET("/admin", authMiddleware(), roleMiddleware(RoleAdmin), adminHandler)
  ```

### Modul 12: Security Best Practices (Hari 34-36)

#### Materi 12.1: Input Sanitization
- **HTML Escaping**:
  ```go
  import "html/template"
  
  // Automatic escaping with html/template
  t, err := template.New("webpage").Parse(`<div>{{.UserInput}}</div>`)
  
  // Manual escaping
  safeInput := template.HTMLEscapeString(userInput)
  ```
- **SQL Injection Prevention**:
  ```go
  // JANGAN:
  db.Exec("SELECT * FROM users WHERE username = '" + username + "'")
  
  // BENAR:
  db.Exec("SELECT * FROM users WHERE username = ?", username)
  ```

#### Materi 12.2: CSRF Protection
- **CSRF Token Generation**:
  ```go
  import "github.com/gorilla/csrf"
  
  // Setup CSRF protection middleware
  csrfMiddleware := csrf.Protect(
      []byte("32-byte-long-auth-key"),
      csrf.Secure(true),
      csrf.SameSite(csrf.SameSiteLaxMode),
  )
  
  // In handler
  token := csrf.Token(r)
  // Include token in form or send with AJAX
  ```
- **Verifying CSRF Token**:
  ```html
  <form method="POST" action="/api/users">
      <input type="hidden" name="gorilla.csrf.Token" value="{{.CSRFToken}}">
      <!-- Form fields -->
  </form>
  ```

#### Materi 12.3: Security Headers
- **Secure Headers Middleware**:
  ```go
  func securityHeadersMiddleware(next http.Handler) http.Handler {
      return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
          // Add security headers
          w.Header().Set("X-XSS-Protection", "1; mode=block")
          w.Header().Set("X-Content-Type-Options", "nosniff")
          w.Header().Set("X-Frame-Options", "DENY")
          w.Header().Set("Content-Security-Policy", "default-src 'self'")
          w.Header().Set("Referrer-Policy", "strict-origin-when-cross-origin")
          w.Header().Set("Strict-Transport-Security", "max-age=31536000; includeSubDomains")
          
          next.ServeHTTP(w, r)
      })
  }
  ```

### Modul 13: Caching dan Performance (Hari 37-39)

#### Materi 13.1: Redis Integration
- **Setup Redis Client**:
  ```go
  import "github.com/go-redis/redis/v8"
  
  rdb := redis.NewClient(&redis.Options{
      Addr:     "localhost:6379",
      Password: "", // no password set
      DB:       0,  // use default DB
  })
  
  // Test connection
  ctx := context.Background()
  _, err := rdb.Ping(ctx).Result()
  ```
- **Basic Operations**:
  ```go
  // Set key with expiration
  err := rdb.Set(ctx, "key", "value", 1*time.Hour).Err()
  
  // Get key
  val, err := rdb.Get(ctx, "key").Result()
  if err == redis.Nil {
      // Key does not exist
  } else if err != nil {
      // Error
  }
  
  // Delete key
  err := rdb.Del(ctx, "key").Err()
  ```

#### Materi 13.2: Caching Strategies
- **Cache-Aside Pattern**:
  ```go
  func getUser(id string) (User, error) {
      // Try to get from cache first
      cacheKey := "user:" + id
      userData, err := rdb.Get(ctx, cacheKey).Result()
      
      if err == nil {
          // Cache hit
          var user User
          err = json.Unmarshal([]byte(userData), &user)
          return user, err
      }
      
      // Cache miss, get from database
      user, err := getUserFromDB(id)
      if err != nil {
          return User{}, err
      }
      
      // Update cache
      userJSON, _ := json.Marshal(user)
      rdb.Set(ctx, cacheKey, userJSON, 10*time.Minute)
      
      return user, nil
  }
  ```
- **Cache Invalidation**:
  ```go
  func updateUser(id string, userData User) error {
      // Update in database
      err := updateUserInDB(id, userData)
      if err != nil {
          return err
      }
      
      // Invalidate cache
      cacheKey := "user:" + id
      rdb.Del(ctx, cacheKey)
      
      return nil
  }
  ```

#### Materi 13.3: Performance Optimization
- **Profiling**:
  ```go
  import _ "net/http/pprof"
  
  // Enable profiling endpoints
  go func() {
      log.Println(http.ListenAndServe("localhost:6060", nil))
  }()
  ```
- **Connection Pooling**:
  ```go
  // Database connection pool
  db, err := sql.Open("mysql", "user:password@tcp(127.0.0.1:3306)/dbname")
  if err != nil {
      log.Fatal(err)
  }
  
  // Set connection pool parameters
  db.SetMaxOpenConns(25)
  db.SetMaxIdleConns(25)
  db.SetConnMaxLifetime(5 * time.Minute)
  ```
- **Gzip Compression**:
  ```go
  import "github.com/gin-contrib/gzip"
  
  // In Gin
  r := gin.Default()
  r.Use(gzip.Gzip(gzip.DefaultCompression))
  ```

### Modul 14: Logging dan Monitoring (Hari 40-42)

#### Materi 14.1: Structured Logging
- **Zap Logger**:
  ```go
  import "go.uber.org/zap"
  
  // Create logger
  logger, err := zap.NewProduction()
  if err != nil {
      // Handle error
  }
  defer logger.Sync()
  
  // Use logger
  logger.Info("Request processed",
      zap.String("method", "GET"),
      zap.String("path", "/users"),
      zap.Int("statusCode", 200),
      zap.Duration("latency", time.Millisecond*53),
  )
  ```
- **Zerolog**:
  ```go
  import "github.com/rs/zerolog"
  import "github.com/rs/zerolog/log"
  
  // Configure global logger
  zerolog.TimeFieldFormat = zerolog.TimeFormatUnix
  log.Logger = log.With().Caller().Logger()
  
  // Logging
  log.Info().
      Str("method", "GET").
      Str("path", "/users").
      Int("statusCode", 200).
      Dur("latency", time.Millisecond*53).
      Msg("Request processed")
  ```

#### Materi 14.2: Log Management
- **Log Rotation dengan lumberjack**:
  ```go
  import "gopkg.in/natefinch/lumberjack.v2"
  
  // Configure log rotation
  logWriter := &lumberjack.Logger{
      Filename:   "/var/log/myapp/app.log",
      MaxSize:    100, // megabytes
      MaxBackups: 3,
      MaxAge:     28,   // days
      Compress:   true, // compress rotated files
  }
  
  // Use with zap
  logger := zap.New(
      zapcore.NewCore(
          zapcore.NewJSONEncoder(zap.NewProductionEncoderConfig()),
          zapcore.AddSync(logWriter),
          zap.InfoLevel,
      ),
  )
  ```
- **Centralized Logging**:
  ```go
  // Fluentd logging example
  import "github.com/fluent/fluent-logger-golang/fluent"
  
  logger, err := fluent.New(fluent.Config{
      FluentHost: "localhost",
      FluentPort: 24224,
      TagPrefix:  "myapp",
  })
  if err != nil {
      // Handle error
  }
  
  // Log message
  logger.Post("access", map[string]interface{}{
      "method":     "GET",
      "path":       "/users",
      "statusCode": 200,
      "latency":    53, // milliseconds
  })
  ```

#### Materi 14.3: Monitoring dengan Prometheus
- **Setup Prometheus Metrics**:
  ```go
  import (
      "github.com/prometheus/client_golang/prometheus"
      "github.com/prometheus/client_golang/prometheus/promhttp"
  )
  
  var (
      httpRequestsTotal = prometheus.NewCounterVec(
          prometheus.CounterOpts{
              Name: "http_requests_total",
              Help: "Total number of HTTP requests",
          },
          []string{"method", "endpoint", "status"},
      )
      
      httpRequestDuration = prometheus.NewHistogramVec(
          prometheus.HistogramOpts{
              Name:    "http_request_duration_seconds",
              Help:    "HTTP request duration in seconds",
              Buckets: prometheus.DefBuckets,
          },
          []string{"method", "endpoint"},
      )
  )
  
  func init() {
      // Register metrics
      prometheus.MustRegister(httpRequestsTotal)
      prometheus.MustRegister(httpRequestDuration)
  }
  
  func main() {
      // Expose metrics endpoint
      http.Handle("/metrics", promhttp.Handler())
      
      // Start server
      http.ListenAndServe(":8080", nil)
  }
  ```
- **Middleware for Metrics**:
  ```go
  func metricsMiddleware(next http.Handler) http.Handler {
      return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
          start := time.Now()
          
          // Wrap ResponseWriter to capture status code
          ww := NewResponseWriter(w)
          
          // Call next handler
          next.ServeHTTP(ww, r)
          
          // Record metrics after request is processed
          duration := time.Since(start).Seconds()
          httpRequestDuration.With(prometheus.Labels{
              "method":   r.Method,
              "endpoint": r.URL.Path,
          }).Observe(duration)
          
          httpRequestsTotal.With(prometheus.Labels{
              "method":   r.Method,
              "endpoint": r.URL.Path,
              "status":   fmt.Sprintf("%d", ww.Status()),
          }).Inc()
      })
  }
  ```

### Modul 15: Testing Lanjutan (Hari 43-45)

#### Materi 15.1: Integration Testing
- **HTTP Server Testing**:
  ```go
  func TestUserAPI(t *testing.T) {
      // Setup test server
      router := setupRouter()
      ts := httptest.NewServer(router)
      defer ts.Close()
      
      // Create HTTP client
      client := &http.Client{}
      
      // Test GET request
      resp, err := client.Get(ts.URL + "/api/users")
      if err != nil {
          t.Fatal(err)
      }
      defer resp.Body.Close()
      
      // Check status code
      if resp.StatusCode != http.StatusOK {
          t.Errorf("Expected status OK; got %v", resp.Status)
      }
      
      // Check response body
      var users []User
      if err := json.NewDecoder(resp.Body).Decode(&users); err != nil {
          t.Fatal(err)
      }
      
      if len(users) == 0 {
          t.Error("Expected users, got empty array")
      }
  }
  ```
- **Database Testing**:
  ```go
  func TestUserRepository(t *testing.T) {
      // Setup test database
      db, err := setupTestDB()
      if err != nil {
          t.Fatal(err)
      }
      
      // Create repository
      repo := NewUserRepository(db)
      
      // Test user creation
      user := User{Name: "Test User", Email: "test@example.com"}
      id, err := repo.Create(user)
      if err != nil {
          t.Errorf("Failed to create user: %v", err)
      }
      
      // Test user retrieval
      retrieved, err := repo.GetByID(id)
      if err != nil {
          t.Errorf("Failed to get user: %v", err)
      }
      
      if retrieved.Name != user.Name {
          t.Errorf("Expected name %s, got %s", user.Name, retrieved.Name)
      }
  }
  ```

#### Materi 15.2: Mocking
- **Mocking dengan Testify**:
  ```go
  import "github.com/stretchr/testify/mock"
  
  // Interface to mock
  type UserService interface {
      GetUser(id string) (User, error)
      CreateUser(user User) error
  }
  
  // Mock implementation
  type MockUserService struct {
      mock.Mock
  }
  
  func (m *MockUserService) GetUser(id string) (User, error) {
      args := m.Called(id)
      return args.Get(0).(User), args.Error(1)
  }
  
  func (m *MockUserService) CreateUser(user User) error {
      args := m.Called(user)
      return args.Error(0)
  }
  
  // Test with mock
  func TestUserHandler(t *testing.T) {
      mockService := new(MockUserService)
      
      // Setup expectations
      mockUser := User{ID: "123", Name: "Test User"}
      mockService.On("GetUser", "123").Return(mockUser, nil)
      
      // Create handler with mock
      handler := NewUserHandler(mockService)
      
      // Create test request
      req, _ := http.NewRequest("GET", "/users/123", nil)
      rr := httptest.NewRecorder()
      
      // Call handler
      handler.ServeHTTP(rr, req)
      
      // Assert status code
      if rr.Code != http.StatusOK {
          t.Errorf("Expected status %d; got %d", http.StatusOK, rr.Code)
      }
      
      // Verify mock was called as expected
      mockService.AssertExpectations(t)
  }
  ```
- **Mocking HTTP Responses** dengan httptest:
  ```go
  func TestFetchExternalAPI(t *testing.T) {
      // Create mock server
      server := httptest.NewServer(http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
          // Check request
          if r.URL.Path != "/api/data" {
              t.Errorf("Expected request to '/api/data', got '%s'", r.URL.Path)
          }
          
          // Return mock response
          w.Header().Set("Content-Type", "application/json")
          w.WriteHeader(http.StatusOK)
          json.NewEncoder(w).Encode(map[string]string{"status": "success"})
      }))
      defer server.Close()
      
      // Use mock server URL in your client
      client := NewAPIClient(server.URL)
      
      // Test your client
      response, err := client.FetchData()
      if err != nil {
          t.Fatalf("Expected no error, got %v", err)
      }
      
      if response.Status != "success" {
          t.Errorf("Expected status 'success', got '%s'", response.Status)
      }
  }
  ```

#### Materi 15.3: Benchmark Testing
- **Basic Benchmarking**:
  ```go
  func BenchmarkStringsJoin(b *testing.B) {
      strs := []string{"apple", "banana", "cherry", "date", "elderberry"}
      b.ResetTimer()
      
      for i := 0; i < b.N; i++ {
          strings.Join(strs, ", ")
      }
  }
  
  func BenchmarkStringsConcatenation(b *testing.B) {
      strs := []string{"apple", "banana", "cherry", "date", "elderberry"}
      b.ResetTimer()
      
      for i := 0; i < b.N; i++ {
          var result string
          for j, s := range strs {
              if j > 0 {
                  result += ", "
              }
              result += s
          }
      }
  }
  ```
- **Running Benchmarks**:
  ```bash
  go test -bench=. -benchmem
  ```
- **Sub-Benchmarks**:
  ```go
  func BenchmarkJSON(b *testing.B) {
      data := getTestData()
      
      b.Run("Marshal", func(b *testing.B) {
          for i := 0; i < b.N; i++ {
              json.Marshal(data)
          }
      })
      
      bytes, _ := json.Marshal(data)
      b.Run("Unmarshal", func(b *testing.B) {
          for i := 0; i < b.N; i++ {
              var result interface{}
              json.Unmarshal(bytes, &result)
          }
      })
  }
  ```

## Fase 4: Microservices dan Deployment (Hari 46-60)

### Modul 16: Microservices Architecture (Hari 46-48)

#### Materi 16.1: Microservices Basics
- **Monolith vs Microservices**:
  - Monolith: Aplikasi tunggal, tightly coupled
  - Microservices: Layanan kecil, loosely coupled, masing-masing memiliki tanggung jawab tunggal

- **Desain Microservice**:
  ```
  ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
  │   User API  │     │  Order API  │     │ Payment API │
  │  Service    │────>│  Service    │────>│  Service    │
  └─────────────┘     └─────────────┘     └─────────────┘
         │                   │                   │
         ▼                   ▼                   ▼
  ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
  │  User DB    │     │  Order DB   │     │ Payment DB  │
  └─────────────┘     └─────────────┘     └─────────────┘
  ```

#### Materi 16.2: Service Communication
- **REST Communication**:
  ```go
  type OrderService struct {
      paymentAPIURL string
      httpClient    *http.Client
  }
  
  func (s *OrderService) ProcessOrder(order Order) error {
      // Create payment request
      payment := PaymentRequest{
          OrderID: order.ID,
          Amount:  order.Total,
      }
      
      paymentJSON, _ := json.Marshal(payment)
      
      // Call Payment API
      resp, err := s.httpClient.Post(
          s.paymentAPIURL+"/api/payments",
          "application/json",
          bytes.NewBuffer(paymentJSON),
      )
      
      if err != nil {
          return err
      }
      defer resp.Body.Close()
      
      // Check response
      if resp.StatusCode != http.StatusCreated {
          return fmt.Errorf("payment failed with status %d", resp.StatusCode)
      }
      
      return nil
  }
  ```
- **gRPC Communication**:
  ```proto
  // payment.proto
  syntax = "proto3";
  
  package payment;
  
  service PaymentService {
      rpc ProcessPayment(PaymentRequest) returns (PaymentResponse);
  }
  
  message PaymentRequest {
      string order_id = 1;
      double amount = 2;
  }
  
  message PaymentResponse {
      string payment_id = 1;
      string status = 2;
  }
  ```
  
  ```go
  // Client implementation
  import "google.golang.org/grpc"
  
  func processPayment(orderID string, amount float64) (*payment.PaymentResponse, error) {
      // Setup connection
      conn, err := grpc.Dial("payment-service:50051", grpc.WithInsecure())
      if err != nil {
          return nil, err
      }
      defer conn.Close()
      
      // Create client
      client := payment.NewPaymentServiceClient(conn)
      
      // Make request
      return client.ProcessPayment(context.Background(), &payment.PaymentRequest{
          OrderId: orderID,
          Amount:  amount,
      })
  }
  ```

#### Materi 16.3: API Gateway
- **Basic API Gateway**:
  ```go
  import (
      "github.com/gin-gonic/gin"
      "net/http/httputil"
      "net/url"
  )
  
  func main() {
      router := gin.Default()
      
      // User service proxy
      userServiceURL, _ := url.Parse("http://user-service:8080")
      userProxy := httputil.NewSingleHostReverseProxy(userServiceURL)
      
      // Order service proxy
      orderServiceURL, _ := url.Parse("http://order-service:8080")
      orderProxy := httputil.NewSingleHostReverseProxy(orderServiceURL)
      
      // Payment service proxy
      paymentServiceURL, _ := url.Parse("http://payment-service:8080")
      paymentProxy := httputil.NewSingleHostReverseProxy(paymentServiceURL)
      
      // Routes
      router.Any("/api/users/*path", gin.WrapH(userProxy))
      router.Any("/api/orders/*path", gin.WrapH(orderProxy))
      router.Any("/api/payments/*path", gin.WrapH(paymentProxy))
      
      router.Run(":80")
  }
  ```
- **Adding Authentication to Gateway**:
  ```go
  func authMiddleware() gin.HandlerFunc {
      return func(c *gin.Context) {
          token := c.GetHeader("Authorization")
          
          // Validate token
          if !isValidToken(token) {
              c.AbortWithStatusJSON(http.StatusUnauthorized, gin.H{
                  "error": "invalid or missing token",
              })
              return
          }
          
          // Add user info to headers for downstream services
          userID := extractUserID(token)
          c.Request.Header.Set("X-User-ID", userID)
          
          c.Next()
      }
  }
  
  // Apply middleware to routes
  router.Any("/api/orders/*path", authMiddleware(), gin.WrapH(orderProxy))
  ```

### Modul 17: Message Queues dan Event-Driven Architecture (Hari 49-51)

#### Materi 17.1: RabbitMQ Integration
- **RabbitMQ Producer**:
  ```go
  import "github.com/streadway/amqp"
  
  func publishOrderCreated(order Order) error {
      // Connect to RabbitMQ
      conn, err := amqp.Dial("amqp://guest:guest@rabbitmq:5672/")
      if err != nil {
          return err
      }
      defer conn.Close()
      
      // Create channel
      ch, err := conn.Channel()
      if err != nil {
          return err
      }
      defer ch.Close()
      
      // Declare queue
      q, err := ch.QueueDeclare(
          "orders", // name
          true,     // durable
          false,    // delete when unused
          false,    // exclusive
          false,    // no-wait
          nil,      // arguments
      )
      if err != nil {
          return err
      }
      
      // Marshal order to JSON
      body, err := json.Marshal(order)
      if err != nil {
          return err
      }
      
      // Publish message
      return ch.Publish(
          "",     // exchange
          q.Name, // routing key
          false,  // mandatory
          false,  // immediate
          amqp.Publishing{
              ContentType: "application/json",
              Body:        body,
          },
      )
  }
  ```
- **RabbitMQ Consumer**:
  ```go
  func startOrderConsumer() {
      // Connect to RabbitMQ
      conn, err := amqp.Dial("amqp://guest:guest@rabbitmq:5672/")
      failOnError(err, "Failed to connect to RabbitMQ")
      defer conn.Close()
      
      // Create channel
      ch, err := conn.Channel()
      failOnError(err, "Failed to open a channel")
      defer ch.Close()
      
      // Declare queue
      q, err := ch.QueueDeclare(
          "orders", // name
          true,     // durable
          false,    // delete when unused
          false,    // exclusive
          false,    // no-wait
          nil,      // arguments
      )
      failOnError(err, "Failed to declare a queue")
      
      // Set QoS (prefetch count)
      err = ch.Qos(
          1,     // prefetch count
          0,     // prefetch size
          false, // global
      )
      failOnError(err, "Failed to set QoS")
      
      // Consume messages
      msgs, err := ch.Consume(
          q.Name, // queue
          "",     // consumer
          false,  // auto-ack
          false,  // exclusive
          false,  // no-local
          false,  // no-wait
          nil,    // args
      )
      failOnError(err, "Failed to register a consumer")
      
      // Process messages
      forever := make(chan bool)
      go func() {
          for d := range msgs {
              var order Order
              err := json.Unmarshal(d.Body, &order)
              
              if err != nil {
                  log.Printf("Error parsing order: %v", err)
                  d.Nack(false, true) // Negative acknowledgment, requeue
                  continue
              }
              
              // Process order
              err = processOrder(order)
              
              if err != nil {
                  log.Printf("Error processing order: %v", err)
                  d.Nack(false, true) // Negative acknowledgment, requeue
              } else {
                  d.Ack(false) // Acknowledgment
              }
          }
      }()
      
      log.Printf("Order consumer started")
      <-forever
  }
  ```

#### Materi 17.2: Kafka Integration
- **Kafka Producer**:
  ```go
  import "github.com/segmentio/kafka-go"
  
  func publishEvent(topic string, key string, value []byte) error {
      // Create writer
      w := kafka.NewWriter(kafka.WriterConfig{
          Brokers:  []string{"kafka-1:9092", "kafka-2:9092"},
          Topic:    topic,
          Balancer: &kafka.LeastBytes{},
      })
      defer w.Close()
      
      // Write message
      err := w.WriteMessages(context.Background(),
          kafka.Message{
              Key:   []byte(key),
              Value: value,
          },
      )
      
      return err
  }
  
  func publishOrderCreated(order Order) error {
      orderJSON, err := json.Marshal(order)
      if err != nil {
          return err
      }
      
      return publishEvent("orders", order.ID, orderJSON)
  }
  ```
- **Kafka Consumer**:
  ```go
  func startOrderConsumer() {
      // Create reader
      r := kafka.NewReader(kafka.ReaderConfig{
          Brokers:   []string{"kafka-1:9092", "kafka-2:9092"},
          Topic:     "orders",
          GroupID:   "order-processing-service",
          MinBytes:  10e3, // 10KB
          MaxBytes:  10e6, // 10MB
          Partition: 0,
      })
      defer r.Close()
      
      // Process messages
      for {
          m, err := r.ReadMessage(context.Background())
          if err != nil {
              log.Printf("Error reading message: %v", err)
              continue
          }
          
          var order Order
          err = json.Unmarshal(m.Value, &order)
          if err != nil {
              log.Printf("Error parsing order: %v", err)
              continue
          }
          
          // Process order
          err = processOrder(order)
          if err != nil {
              log.Printf("Error processing order: %v", err)
          }
      }
  }
  ```

#### Materi 17.3: Event-Driven Design Patterns
- **CQRS (Command Query Responsibility Segregation)**:
  ```go
  // Command (Write) Model
  type OrderCommand struct {
      ID        string
      UserID    string
      Products  []OrderProduct
      CreatedAt time.Time
  }
  
  // Query (Read) Model
  type OrderSummary struct {
      ID           string
      UserID       string
      TotalAmount  float64
      ProductCount int
      Status       string
      CreatedAt    time.Time
  }
  
  // Command Handler
  func CreateOrderHandler(cmd OrderCommand) error {
      // Validate command
      if err := validateOrder(cmd); err != nil {
          return err
      }
      
      // Store in write database
      if err := storeOrder(cmd); err != nil {
          return err
      }
      
      // Publish event
      event := OrderCreatedEvent{
          ID:        cmd.ID,
          UserID:    cmd.UserID,
          Products:  cmd.Products,
          CreatedAt: cmd.CreatedAt,
      }
      
      return publishEvent("order-created", cmd.ID, event)
  }
  
  // Event Handler (updates read model)
  func OrderCreatedEventHandler(event OrderCreatedEvent) error {
      // Calculate summary data
      totalAmount := 0.0
      for _, p := range event.Products {
          totalAmount += p.Price * float64(p.Quantity)
      }
      
      // Create read model
      summary := OrderSummary{
          ID:           event.ID,
          UserID:       event.UserID,
          TotalAmount:  totalAmount,
          ProductCount: len(event.Products),
          Status:       "created",
          CreatedAt:    event.CreatedAt,
      }
      
      // Store in read database
      return storeOrderSummary(summary)
  }
  ```
- **Event Sourcing**:
  ```go
  // Event store
  type EventStore interface {
      SaveEvents(streamID string, events []Event, expectedVersion int) error
      GetEvents(streamID string) ([]Event, error)
  }
  
  // Event
  type Event interface {
      GetType() string
      GetData() []byte
      GetStreamID() string
      GetVersion() int
  }
  
  // Order aggregate
  type Order struct {
      ID       string
      UserID   string
      Products []OrderProduct
      Status   string
      Version  int
  }
  
  // Reconstruct aggregate from events
  func LoadOrder(eventStore EventStore, orderID string) (Order, error) {
      var order Order
      order.ID = orderID
      
      events, err := eventStore.GetEvents(orderID)
      if err != nil {
          return order, err
      }
      
      for _, event := range events {
          order.ApplyEvent(event)
          order.Version = event.GetVersion()
      }
      
      return order, nil
  }
  
  // Apply changes and generate events
  func (o *Order) AddProduct(product OrderProduct) OrderProductAddedEvent {
      // Create event
      event := OrderProductAddedEvent{
          OrderID:    o.ID,
          Product:    product,
          Version:    o.Version + 1,
      }
      
      // Apply event to order
      o.Products = append(o.Products, product)
      o.Version++
      
      return event
  }
  ```

### Modul 18: Docker dan Containerization (Hari 52-54)

#### Materi 18.1: Dockerfile untuk Go Applications
- **Basic Dockerfile**:
  ```dockerfile
  FROM golang:1.17-alpine AS builder
  
  WORKDIR /app
  
  # Copy go.mod and go.sum
  COPY go.mod go.sum ./
  
  # Download dependencies
  RUN go mod download
  
  # Copy source code
  COPY . .
  
  # Build the application
  RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o main .
  
  # Use a small alpine image
  FROM alpine:latest
  
  WORKDIR /root/
  
  # Copy the binary from builder
  COPY --from=builder /app/main .
  
  # Expose port
  EXPOSE 8080
  
  # Run the binary
  CMD ["./main"]
  ```
- **Multi-Stage Build for Smaller Images**:
  ```dockerfile
  # Build stage
  FROM golang:1.17-alpine AS builder
  
  WORKDIR /app
  
  COPY go.mod go.sum ./
  RUN go mod download
  
  COPY . .
  
  # Build with optimization
  RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -ldflags="-w -s" -o /go/bin/app
  
  # Final stage
  FROM scratch
  
  # Copy certificates for HTTPS connections
  COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
  
  # Copy binary
  COPY --from=builder /go/bin/app /app
  
  # Expose port
  EXPOSE 8080
  
  # Run
  ENTRYPOINT ["/app"]
  ```

#### Materi 18.2: Docker Compose
- **Docker Compose untuk Development**:
  ```yaml
  # docker-compose.yml
  version: '3'
  
  services:
    api:
      build:
        context: .
        dockerfile: Dockerfile
      ports:
        - "8080:8080"
      environment:
        - DB_HOST=db
        - DB_USER=postgres
        - DB_PASSWORD=password
        - DB_NAME=appdb
        - REDIS_HOST=redis:6379
      depends_on:
        - db
        - redis
      volumes:
        - ./:/app
      restart: on-failure
  
    db:
      image: postgres:13
      ports:
        - "5432:5432"
      environment:
        - POSTGRES_USER=postgres
        - POSTGRES_PASSWORD=password
        - POSTGRES_DB=appdb
      volumes:
        - postgres_data:/var/lib/postgresql/data
  
    redis:
      image: redis:6-alpine
      ports:
        - "6379:6379"
      volumes:
        - redis_data:/data
  
  volumes:
    postgres_data:
    redis_data:
  ```
- **Database Migration dengan Docker Compose**:
  ```yaml
  services:
    # Add to existing docker-compose.yml
    migration:
      build:
        context: .
        dockerfile: Dockerfile.migration
      environment:
        - DB_HOST=db
        - DB_USER=postgres
        - DB_PASSWORD=password
        - DB_NAME=appdb
      depends_on:
        - db
      command: ["./wait-for-it.sh", "db:5432", "--", "./migrate"]
  ```
  
  ```dockerfile
  # Dockerfile.migration
  FROM golang:1.17-alpine
  
  WORKDIR /app
  
  COPY go.mod go.sum ./
  RUN go mod download
  
  COPY . .
  
  RUN go build -o migrate ./cmd/migrate
  
  # Add wait-for-it script
COPY scripts/wait-for-it.sh /app/wait-for-it.sh
RUN chmod +x /app/wait-for-it.sh

CMD ["./migrate"]
  ```

#### Materi 18.3: Docker Network dan Best Practices
- **Docker Network**:
  ```yaml
  # docker-compose.yml dengan custom network
  version: '3'
  
  services:
    api:
      # ... (konfigurasi seperti sebelumnya)
      networks:
        - backend
        - frontend
  
    db:
      # ... (konfigurasi seperti sebelumnya)
      networks:
        - backend
  
    redis:
      # ... (konfigurasi seperti sebelumnya)
      networks:
        - backend
  
  networks:
    backend:
      driver: bridge
    frontend:
      driver: bridge
  ```
- **Docker Security Best Practices**:
  - Gunakan image minimal (alpine atau scratch)
  - Jangan jalankan container sebagai root
  - Scan image untuk vulnerabilities dengan tools seperti Trivy
  - Gunakan multi-stage build untuk mengurangi attack surface
  - Buat non-root user di Dockerfile:
  
  ```dockerfile
  # Buat user dengan id non-privileged
  RUN adduser -D -u 10001 appuser
  
  # Switch ke user non-root
  USER appuser
  
  # Jalankan aplikasi
  CMD ["./app"]
  ```

- **Environment Variables dan Secrets**:
  - Gunakan .env file untuk development
  - Gunakan Docker Secrets untuk production
  - Jangan hardcode credentials di image

### Modul 19: Kubernetes dan Deployment (Hari 55-57)

#### Materi 19.1: Kubernetes Basics
- **Pod Definition**:
  ```yaml
  # pod.yaml
  apiVersion: v1
  kind: Pod
  metadata:
    name: api-pod
    labels:
      app: api
  spec:
    containers:
    - name: api
      image: myapp/api:latest
      ports:
      - containerPort: 8080
      env:
      - name: DB_HOST
        value: "postgres-service"
      - name: REDIS_HOST
        value: "redis-service:6379"
  ```
- **Deployment**:
  ```yaml
  # deployment.yaml
  apiVersion: apps/v1
  kind: Deployment
  metadata:
    name: api-deployment
  spec:
    replicas: 3
    selector:
      matchLabels:
        app: api
    template:
      metadata:
        labels:
          app: api
      spec:
        containers:
        - name: api
          image: myapp/api:latest
          ports:
          - containerPort: 8080
          env:
          - name: DB_HOST
            value: "postgres-service"
          - name: REDIS_HOST
            value: "redis-service:6379"
          livenessProbe:
            httpGet:
              path: /health
              port: 8080
            initialDelaySeconds: 3
            periodSeconds: 3
  ```
- **Service**:
  ```yaml
  # service.yaml
  apiVersion: v1
  kind: Service
  metadata:
    name: api-service
  spec:
    selector:
      app: api
    ports:
    - port: 80
      targetPort: 8080
    type: ClusterIP
  ```

#### Materi 19.2: ConfigMap dan Secrets
- **ConfigMap**:
  ```yaml
  # configmap.yaml
  apiVersion: v1
  kind: ConfigMap
  metadata:
    name: api-config
  data:
    APP_ENV: "production"
    LOG_LEVEL: "info"
    METRICS_ENABLED: "true"
  ```
- **Secret**:
  ```yaml
  # secret.yaml
  apiVersion: v1
  kind: Secret
  metadata:
    name: api-secrets
  type: Opaque
  data:
    # Values must be base64 encoded
    DB_PASSWORD: cGFzc3dvcmQ=  # "password" in base64
    API_KEY: c2VjcmV0LWtleQ==  # "secret-key" in base64
  ```
- **Menggunakan ConfigMap dan Secret**:
  ```yaml
  # deployment dengan config
  spec:
    containers:
    - name: api
      image: myapp/api:latest
      ports:
      - containerPort: 8080
      env:
      # Dari ConfigMap
      - name: APP_ENV
        valueFrom:
          configMapKeyRef:
            name: api-config
            key: APP_ENV
      # Dari Secret
      - name: DB_PASSWORD
        valueFrom:
          secretKeyRef:
            name: api-secrets
            key: DB_PASSWORD
      # Semua nilai dari ConfigMap
      envFrom:
      - configMapRef:
          name: api-config
  ```

#### Materi 19.3: Kubernetes Deployment Strategies
- **Rolling Update**:
  ```yaml
  # deployment dengan rolling update
  spec:
    replicas: 3
    strategy:
      type: RollingUpdate
      rollingUpdate:
        maxSurge: 1        # Max pods yang bisa dibuat melebihi replicas
        maxUnavailable: 0  # Max pods yang boleh unavailable selama update
  ```
- **Blue-Green Deployment**:
  ```yaml
  # blue deployment
  metadata:
    name: api-blue
    labels:
      app: api
      version: blue
  
  # green deployment
  metadata:
    name: api-green
    labels:
      app: api
      version: green
  
  # service (awalnya mengarah ke blue)
  spec:
    selector:
      app: api
      version: blue  # Untuk switch, ubah selector ke green
  ```
- **Canary Deployment**:
  ```yaml
  # Main deployment (90% traffic)
  spec:
    replicas: 9
    template:
      metadata:
        labels:
          app: api
          version: stable
  
  # Canary deployment (10% traffic)
  spec:
    replicas: 1
    template:
      metadata:
        labels:
          app: api
          version: canary
  
  # Service (mengarah ke keduanya)
  spec:
    selector:
      app: api  # Tanpa version, akan memilih semua pod dengan label app: api
  ```

### Modul 20: Proyek Capstone dan Portfolio (Hari 58-60)

#### Materi 20.1: Desain Sistem End-to-End
- **Arsitektur Microservices**:
  ```
  ┌────────────┐      ┌────────────┐
  │   API      │      │   Web UI   │
  │  Gateway   │◄────►│            │
  └────────────┘      └────────────┘
         │
         ├────────────┬─────────────┬─────────────┐
         ▼            ▼             ▼             ▼
  ┌────────────┐ ┌─────────────┐ ┌─────────┐ ┌────────────┐
  │    User    │ │    Order    │ │ Payment │ │ Inventory  │
  │  Service   │ │   Service   │ │ Service │ │  Service   │
  └────────────┘ └─────────────┘ └─────────┘ └────────────┘
         │             │             │             │
         ▼             ▼             ▼             ▼
  ┌────────────┐ ┌─────────────┐ ┌─────────┐ ┌────────────┐
  │  User DB   │ │  Order DB   │ │Payment DB│ │Inventory DB│
  └────────────┘ └─────────────┘ └─────────┘ └────────────┘
                        │
                        ▼
                  ┌─────────────┐
                  │  Message    │
                  │   Queue     │
                  └─────────────┘
                        │
                        ▼
                  ┌─────────────┐
                  │ Notification│
                  │   Service   │
                  └─────────────┘
  ```

- **Komponen Proyek**:
  1. **API Gateway**: Menggunakan Gin, menangani routing, autentikasi, dan rate limiting
  2. **User Service**: Mengelola user, autentikasi, dan otorisasi
  3. **Order Service**: Mengelola pemesanan dan status
  4. **Payment Service**: Mengelola transaksi pembayaran
  5. **Inventory Service**: Mengelola stok produk
  6. **Notification Service**: Mengirim email/SMS notifikasi
  7. **Message Queue**: RabbitMQ atau Kafka untuk komunikasi asinkron

#### Materi 20.2: Implementasi Proyek
- **User Service**:
  - Registrasi dan login
  - JWT authentication
  - Profile management
  - RBAC (Role-Based Access Control)

- **Order Service**:
  - CRUD operasi untuk order
  - Order status management
  - Integration dengan Payment dan Inventory
  - Event publishing untuk order events

- **Komunikasi antar Service**:
  - REST API untuk synchronous communication
  - Message Queue untuk asynchronous communication
  - gRPC untuk high-performance communication

- **Deployment**:
  - Docker Compose untuk development
  - Kubernetes manifests untuk production
  - CI/CD pipeline

#### Materi 20.3: Dokumentasi dan Portfolio
- **API Documentation**:
  - Swagger/OpenAPI specification
  - Contoh kode dan penggunaan
  - Penjelasan error codes

- **Project Documentation**:
  - Architecture diagrams
  - Setup dan deployment instructions
  - Development workflow

- **README yang Komprehensif**:
  ```markdown
  # E-Commerce Microservices

  Sistem e-commerce berbasis microservices yang diimplementasikan dengan Go.

  ## Architecture

  [Diagram Arsitektur]

  ## Services

  * **API Gateway**: Entry point untuk semua requests
  * **User Service**: Mengelola user dan authentication
  * **Order Service**: Mengelola pemesanan
  * **Payment Service**: Menangani pembayaran
  * **Inventory Service**: Mengelola stok produk
  * **Notification Service**: Mengirim notifikasi

  ## Technologies

  * Go 1.17
  * PostgreSQL
  * Redis
  * RabbitMQ
  * Docker & Kubernetes
  * JWT Authentication
  * Prometheus & Grafana monitoring

  ## Setup & Deployment

  ### Local Development

  ```bash
  # Clone repository
  git clone https://github.com/username/ecommerce-microservices.git

  # Start with Docker Compose
  docker-compose up
  ```

  ### Production Deployment

  ```bash
  # Deploy to Kubernetes
  kubectl apply -f kubernetes/
  ```

  ## API Documentation

  API documentation tersedia di `/swagger` endpoint setelah menjalankan service,
  atau lihat [docs/api.md](docs/api.md).

  ## Performance

  Benchmark results dan capacity planning tersedia di [docs/performance.md](docs/performance.md).
  ```

- **Portfolio GitHub**:
  1. Struktur repository yang rapi
  2. Dokumentasi yang jelas
  3. Code examples dan demo
  4. Test coverage yang baik
  5. Setup instructions yang lengkap

## Rangkuman

Selamat! Anda telah mempelajari materi Golang dari dasar hingga expert. Kurikulum ini telah mencakup:

1. **Dasar-Dasar Golang**: Sintaks, tipe data, struktur kontrol, fungsi, dll.
2. **Web Development**: REST API, database interaction, autentikasi, middleware
3. **Backend Development Lanjutan**: Security, caching, logging, monitoring
4. **Microservices & Deployment**: Docker, Kubernetes, message queues, event-driven architecture

Dengan menguasai materi-materi ini, Anda telah siap untuk bekerja sebagai Golang developer di industri. Teruslah belajar dan mengembangkan diri dengan mengikuti perkembangan terbaru di ekosistem Go!
