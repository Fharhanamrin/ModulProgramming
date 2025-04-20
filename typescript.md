# TypeScript Curriculum: Basic to Expert

## Timeline Pembelajaran

| Fase | Durasi | Level | Topik Utama |
|------|--------|-------|-------------|
| Fase 1 | 2 minggu | Basic | Pengenalan TypeScript, tipe dasar, dan sintaks dasar |
| Fase 2 | 2 minggu | Intermediate | Tipe lanjutan, generic, dan pengelolaan error |
| Fase 3 | 3 minggu | Advanced | OOP, design patterns dan aplikasi kompleks |
| Fase 4 | 3 minggu | Expert | TypeScript dengan framework, optimasi, dan arsitektur aplikasi |

---

## Fase 1: TypeScript Basic (2 minggu)

### Minggu 1: Pengenalan TypeScript

#### 1. Pengenalan TypeScript
- Apa itu TypeScript dan mengapa menggunakannya
- Perbedaan antara JavaScript dan TypeScript
- Manfaat dan kekurangan TypeScript
- Sejarah singkat TypeScript

#### 2. Setup Lingkungan Development
- Instalasi Node.js dan npm
- Instalasi TypeScript secara global dan lokal
- Konfigurasi editor (VSCode, extensions yang direkomendasikan)
- Struktur proyek TypeScript dasar

#### 3. Dasar-dasar TypeScript
- Kompilasi file TypeScript ke JavaScript
- Konfigurasi tsconfig.json dasar
- Memahami transpilasi TypeScript

#### 4. Tipe Data Dasar
- Boolean, Number, String
- Array dan Tuple
- Enum
- Any, Unknown, dan Never
- Void
- Null dan Undefined
- Object

### Minggu 2: Type System dan Sintaks Dasar

#### 5. Type Annotations dan Type Inference
- Mendeklarasikan tipe secara eksplisit
- Type inference (ketika TypeScript menyimpulkan tipe)
- Best practices untuk annotations

#### 6. Interface
- Mendefinisikan interface
- Optional properties
- Readonly properties
- Interface extending
- Interface vs Type Alias

#### 7. Functions dalam TypeScript
- Function type annotations
- Optional dan default parameters
- Rest parameters
- Function overloading
- Arrow functions

#### 8. Tipe Union dan Intersection
- Union types (|)
- Intersection types (&)
- Type Guards
- Discriminated Unions

---

## Fase 2: TypeScript Intermediate (2 minggu)

### Minggu 3: Tipe Lanjutan

#### 9. Type Aliases dan Literal Types
- Membuat type aliases
- String literal types
- Numeric literal types
- Boolean literal types
- Template literal types

#### 10. Classes dalam TypeScript
- Pengenalan class
- Access modifiers (public, private, protected)
- Inheritance
- Abstract classes
- Implementing interfaces

#### 11. Generics
- Apa itu Generics dan mengapa diperlukan
- Generic functions
- Generic interfaces
- Generic classes
- Generic constraints

#### 12. Advanced Types
- Conditional types
- Mapped types
- Index types
- keyof operator
- Utility types (Partial, Required, Record, Pick, Omit, dll)

### Minggu 4: Module System dan Error Handling

#### 13. Module System
- Namespaces
- ES modules
- CommonJS modules
- Dynamic imports
- Module resolution strategies

#### 14. Error Handling
- Try-catch blocks
- Error types
- Custom error classes
- Error propagation
- Asynchronous error handling

#### 15. Asynchronous TypeScript
- Promises dengan type safety
- Async/await
- Handling promise rejections
- Promise combinators (all, race, allSettled)
- Parallel vs sequential execution

#### 16. Testing TypeScript Code
- Unit testing dengan Jest/Mocha
- TypeScript-specific testing challenges
- Mocking
- Integration tests
- Type testing dengan dtslint

---

## Fase 3: TypeScript Advanced (3 minggu)

### Minggu 5: Object-Oriented Programming

#### 17. Advanced OOP Concepts
- Polymorphism dalam TypeScript
- Mixins
- Decorators
- Method overriding
- Static members

#### 18. Design Patterns dalam TypeScript
- Singleton pattern
- Factory pattern
- Observer pattern
- Strategy pattern
- Adapter pattern
- Command pattern

#### 19. Dependency Injection
- Prinsip dependency injection
- Inversion of Control (IoC)
- Container untuk dependency injection
- Implementasi DI dengan TypeScript

#### 20. SOLID Principles
- Single Responsibility Principle
- Open/Closed Principle
- Liskov Substitution Principle
- Interface Segregation Principle
- Dependency Inversion Principle

### Minggu 6: TypeScript Project Structure dan Tooling

#### 21. Project Structure
- Organizing code
- Folder structure best practices
- Monorepo vs multiple repositories
- Configuration inheritance

#### 22. Build Tools dan Bundlers
- Webpack dengan TypeScript
- Rollup.js
- Parcel
- esbuild
- Optimasi build

#### 23. Linting dan Formatting
- ESLint untuk TypeScript
- Prettier
- Custom rules
- Automating code quality checks

#### 24. TypeScript Declaration Files
- Memahami .d.ts files
- Membuat declaration files
- Consuming external libraries
- DefinitelyTyped repository
- Publishing typings

### Minggu 7: Advanced TypeScript Patterns

#### 25. Functional Programming dengan TypeScript
- Pure functions
- Immutability
- Higher-order functions
- Function composition
- Option/Maybe pattern

#### 26. Metaprogramming
- Decorators lanjutan
- Reflection
- Symbol
- Proxy

#### 27. Advanced Generic Patterns
- Higher-order types
- Recursive types
- Variadic tuple types
- Template literal type inference

#### 28. Type-Level Programming
- Type challenges
- Type arithmetic
- Type state machines
- Type validation
- Type-level algorithms

---

## Fase 4: TypeScript Expert (3 minggu)

### Minggu 8: TypeScript dengan Framework dan Library

#### 29. TypeScript dengan React
- React dan TypeScript setup
- Component typing
- Props dan state typing
- Hooks dengan TypeScript
- Context API typing
- React performance dengan TypeScript

#### 30. TypeScript dengan Node.js
- Setup Node.js dengan TypeScript
- Express/Nest.js dengan TypeScript
- Database access dengan type safety
- API design dengan TypeScript
- Error handling di aplikasi server

#### 31. TypeScript dengan Angular
- Angular architecture
- Angular services, directives, pipes
- Angular forms
- NgRx dengan TypeScript
- Testing Angular apps

#### 32. TypeScript dengan Vue.js
- Vue.js 3 Composition API
- TypeScript di Vue components
- Pinia/Vuex dengan TypeScript
- Vue Router dengan TypeScript
- Custom directives

### Minggu 9: Advanced Application Architecture

#### 33. Domain-Driven Design (DDD)
- Bounded contexts
- Entities, value objects, aggregates
- Repositories
- Domain services
- Application services

#### 34. Architectural Patterns
- Clean Architecture
- Hexagonal Architecture
- Microservices
- CQRS
- Event Sourcing

#### 35. State Management
- Implementasi state management
- Redux dengan TypeScript
- MobX dengan TypeScript
- Zustand, Jotai, Recoil
- Custom state management solutions

#### 36. Advanced API Design
- RESTful APIs dengan TypeScript
- GraphQL dengan TypeScript
- gRPC dan Protocol Buffers
- WebSockets dengan TypeScript
- Type-safe API clients

### Minggu 10: Optimasi dan Performance

#### 37. Performance Optimization
- Memory management
- Optimizing TypeScript compilation
- Bundle size optimization
- Runtime performance
- Lazy loading

#### 38. Advanced Debugging
- Source maps
- Chrome DevTools dengan TypeScript
- Node.js debugging
- Performance profiling
- Memory leak identification

#### 39. Security Best Practices
- Type-safe validation
- CSRF/XSS prevention
- Authentication dan authorization
- Rate limiting
- Input sanitization

#### 40. Real-world TypeScript
- Migrasi dari JavaScript ke TypeScript
- Working with legacy code
- TypeScript in production
- Scaling TypeScript applications
- Case studies

---

## Proyek-proyek untuk Latihan

### Proyek Basic
1. Todo List App dengan tipe yang kuat
2. Calculator dengan type safety
3. Form validation dengan TypeScript

### Proyek Intermediate
1. REST API client dengan TypeScript
2. State management library simple
3. CLI tool dengan TypeScript

### Proyek Advanced
1. Full-stack application dengan TypeScript (Node.js + React/Angular/Vue)
2. Framework component library dengan TypeScript
3. Game sederhana dengan TypeScript dan Canvas/WebGL

### Proyek Expert
1. Implementasi arsitektur microservice dengan TypeScript
2. Compiler/parser sederhana
3. Framework kustom dengan TypeScript

---

## Sumber Daya Tambahan

### Dokumentasi
- [TypeScript Official Documentation](https://www.typescriptlang.org/docs/)
- [TypeScript GitHub Repository](https://github.com/microsoft/TypeScript)
- [TypeScript Deep Dive Book](https://basarat.gitbook.io/typescript/)

### Kursus Online
- TypeScript Fundamentals (Frontend Masters)
- Understanding TypeScript (Udemy)
- Advanced TypeScript (Pluralsight)

### Komunitas dan Forum
- [TypeScript GitHub Discussions](https://github.com/microsoft/TypeScript/discussions)
- [TypeScript Discord Server](https://discord.com/invite/typescript)
- [TypeScript Stack Overflow](https://stackoverflow.com/questions/tagged/typescript)

### Blogs dan Newsletter
- TypeScript Weekly Newsletter
- Mariusschulz.com
- Blog resmi TypeScript

### Alat dan Playground
- [TypeScript Playground](https://www.typescriptlang.org/play)
- [TS Config Options Explainer](https://www.typescriptlang.org/tsconfig)
- [Type Challenges](https://github.com/type-challenges/type-challenges)
