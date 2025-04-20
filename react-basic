ing untuk daftar panjang
- Bundle optimization dengan webpack
- Optimasi API calls dan caching
- Image optimization
- Tree-shaking dan dead code elimination

### MODUL 9: TESTING & DEBUGGING

#### Topik 9.1: Unit Testing dengan Jest
**Durasi**: 1 hari  
**Materi**:
- Jest basics
- Test structure
- Matchers
- Mocking functions
- Snapshot testing
- Code coverage
- Test-driven development

**Hands-on Practice**:
```jsx
// Component to test
function sum(a, b) {
  return a + b;
}

// Basic test
test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});

// Testing a utility function
import { formatCurrency, capitalizeString } from '../utils';

describe('Utility functions', () => {
  test('formatCurrency formats numbers correctly', () => {
    expect(formatCurrency(1000)).toBe('$1,000.00');
    expect(formatCurrency(10.5)).toBe('$10.50');
    expect(formatCurrency(0)).toBe('$0.00');
  });
  
  test('capitalizeString capitalizes first letter', () => {
    expect(capitalizeString('hello')).toBe('Hello');
    expect(capitalizeString('WORLD')).toBe('World');
    expect(capitalizeString('')).toBe('');
  });
});

// Mock functions
test('calls callback when button is clicked', () => {
  const mockCallback = jest.fn();
  
  const button = document.createElement('button');
  button.onclick = mockCallback;
  button.click();
  
  expect(mockCallback).toHaveBeenCalled();
  expect(mockCallback).toHaveBeenCalledTimes(1);
});

// Snapshot testing
import renderer from 'react-test-renderer';
import Button from '../Button';

test('Button renders correctly', () => {
  const component = renderer.create(
    <Button label="Click me" primary={true} />
  );
  
  let tree = component.toJSON();
  expect(tree).toMatchSnapshot();
});
```

#### Topik 9.2: Component Testing dengan React Testing Library
**Durasi**: 2 hari  
**Materi**:
- React Testing Library philosophy
- Querying elements
- User events
- Form testing
- Async testing
- Custom render functions
- Test best practices

**Hands-on Practice**:
```jsx
// Counter.js
function Counter() {
  const [count, setCount] = useState(0);
  
  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(count - 1)}>Decrement</button>
    </div>
  );
}

// Counter.test.js
import { render, screen, fireEvent } from '@testing-library/react';
import Counter from './Counter';

test('renders counter with initial count of 0', () => {
  render(<Counter />);
  
  // Using screen query methods
  const headingElement = screen.getByText(/count: 0/i);
  expect(headingElement).toBeInTheDocument();
});

test('increments counter when increment button is clicked', () => {
  render(<Counter />);
  
  // Click the increment button
  const incrementButton = screen.getByText(/increment/i);
  fireEvent.click(incrementButton);
  
  // Check if count was updated
  const headingElement = screen.getByText(/count: 1/i);
  expect(headingElement).toBeInTheDocument();
});

test('decrements counter when decrement button is clicked', () => {
  render(<Counter />);
  
  // Click the decrement button
  const decrementButton = screen.getByText(/decrement/i);
  fireEvent.click(decrementButton);
  
  // Check if count was updated
  const headingElement = screen.getByText(/count: -1/i);
  expect(headingElement).toBeInTheDocument();
});

// LoginForm.js
function LoginForm({ onSubmit }) {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');
  const [error, setError] = useState('');
  
  const handleSubmit = (e) => {
    e.preventDefault();
    
    if (!username || !password) {
      setError('Please fill in all fields');
      return;
    }
    
    setError('');
    onSubmit({ username, password });
  };
  
  return (
    <form onSubmit={handleSubmit}>
      {error && <div role="alert">{error}</div>}
      
      <div>
        <label htmlFor="username">Username</label>
        <input
          id="username"
          value={username}
          onChange={(e) => setUsername(e.target.value)}
          data-testid="username"
        />
      </div>
      
      <div>
        <label htmlFor="password">Password</label>
        <input
          id="password"
          type="password"
          value={password}
          onChange={(e) => setPassword(e.target.value)}
          data-testid="password"
        />
      </div>
      
      <button type="submit">Login</button>
    </form>
  );
}

// LoginForm.test.js
import { render, screen, fireEvent, waitFor } from '@testing-library/react';
import userEvent from '@testing-library/user-event';
import LoginForm from './LoginForm';

test('calls onSubmit with username and password when form is submitted', async () => {
  const handleSubmit = jest.fn();
  render(<LoginForm onSubmit={handleSubmit} />);
  
  // Fill out the form
  userEvent.type(screen.getByTestId('username'), 'testuser');
  userEvent.type(screen.getByTestId('password'), 'password123');
  
  // Submit the form
  fireEvent.click(screen.getByText(/login/i));
  
  // Check if onSubmit was called with correct data
  expect(handleSubmit).toHaveBeenCalledWith({
    username: 'testuser',
    password: 'password123'
  });
});

test('shows error message when form is submitted with empty fields', () => {
  const handleSubmit = jest.fn();
  render(<LoginForm onSubmit={handleSubmit} />);
  
  // Submit form without filling fields
  fireEvent.click(screen.getByText(/login/i));
  
  // Check if error message is displayed
  const errorMessage = screen.getByRole('alert');
  expect(errorMessage).toHaveTextContent(/please fill in all fields/i);
  
  // Check that onSubmit was not called
  expect(handleSubmit).not.toHaveBeenCalled();
});

// Async component testing
function UserProfile({ userId }) {
  const [user, setUser] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);
  
  useEffect(() => {
    async function fetchUser() {
      try {
        setLoading(true);
        const response = await fetch(`/api/users/${userId}`);
        const data = await response.json();
        setUser(data);
      } catch (err) {
        setError('Failed to fetch user');
      } finally {
        setLoading(false);
      }
    }
    
    fetchUser();
  }, [userId]);
  
  if (loading) return <p>Loading...</p>;
  if (error) return <p>{error}</p>;
  if (!user) return null;
  
  return (
    <div>
      <h1>{user.name}</h1>
      <p>Email: {user.email}</p>
    </div>
  );
}

// UserProfile.test.js
import { render, screen, waitFor } from '@testing-library/react';
import { rest } from 'msw';
import { setupServer } from 'msw/node';
import UserProfile from './UserProfile';

const server = setupServer(
  rest.get('/api/users/1', (req, res, ctx) => {
    return res(
      ctx.json({
        id: 1,
        name: 'John Doe',
        email: 'john@example.com'
      })
    );
  })
);

// Enable API mocking before tests
beforeAll(() => server.listen());

// Reset any runtime request handlers we may add during the tests
afterEach(() => server.resetHandlers());

// Disable API mocking after the tests are done
afterAll(() => server.close());

test('fetches and displays user data', async () => {
  render(<UserProfile userId={1} />);
  
  // Check loading state
  expect(screen.getByText(/loading/i)).toBeInTheDocument();
  
  // Wait for user data to be displayed
  await waitFor(() => {
    expect(screen.getByText(/john doe/i)).toBeInTheDocument();
  });
  
  expect(screen.getByText(/email: john@example.com/i)).toBeInTheDocument();
});

test('handles API error', async () => {
  // Override the default MSW response for this test
  server.use(
    rest.get('/api/users/1', (req, res, ctx) => {
      return res(ctx.status(500));
    })
  );
  
  render(<UserProfile userId={1} />);
  
  // Wait for error message
  await waitFor(() => {
    expect(screen.getByText(/failed to fetch user/i)).toBeInTheDocument();
  });
});
```

#### Topik 9.3: Integration Testing
**Durasi**: 1 hari  
**Materi**:
- Integration vs unit testing
- Testing component integration
- Testing routes
- Testing state management
- Testing forms
- Testing API integration
- Test fixtures

**Hands-on Practice**:
```jsx
// Integration test for a TodoApp
import { render, screen, fireEvent, waitFor } from '@testing-library/react';
import userEvent from '@testing-library/user-event';
import { rest } from 'msw';
import { setupServer } from 'msw/node';
import TodoApp from './TodoApp';

// Mock API
const server = setupServer(
  // GET todos
  rest.get('/api/todos', (req, res, ctx) => {
    return res(
      ctx.json([
        { id: 1, text: 'Learn React', completed: false },
        { id: 2, text: 'Learn Testing', completed: true }
      ])
    );
  }),
  
  // POST new todo
  rest.post('/api/todos', (req, res, ctx) => {
    const { text } = req.body;
    return res(
      ctx.json({
        id: 3,
        text,
        completed: false
      })
    );
  }),
  
  // PUT todo (toggle completion)
  rest.put('/api/todos/:id', (req, res, ctx) => {
    const { id } = req.params;
    const { completed } = req.body;
    
    return res(
      ctx.json({
        id: Number(id),
        text: id === '1' ? 'Learn React' : 'Learn Testing',
        completed
      })
    );
  }),
  
  // DELETE todo
  rest.delete('/api/todos/:id', (req, res, ctx) => {
    return res(ctx.status(204));
  })
);

beforeAll(() => server.listen());
afterEach(() => server.resetHandlers());
afterAll(() => server.close());

test('loads and displays todos', async () => {
  render(<TodoApp />);
  
  // Check loading state
  expect(screen.getByText(/loading/i)).toBeInTheDocument();
  
  // Wait for todos to load
  await waitFor(() => {
    expect(screen.getByText(/learn react/i)).toBeInTheDocument();
  });
  
  expect(screen.getByText(/learn testing/i)).toBeInTheDocument();
});

test('adds a new todo', async () => {
  render(<TodoApp />);
  
  // Wait for initial todos to load
  await waitFor(() => {
    expect(screen.getByText(/learn react/i)).toBeInTheDocument();
  });
  
  // Add new todo
  const input = screen.getByPlaceholderText(/add todo/i);
  const addButton = screen.getByText(/add/i);
  
  userEvent.type(input, 'Learn Redux');
  fireEvent.click(addButton);
  
  // Check if new todo is added
  await waitFor(() => {
    expect(screen.getByText(/learn redux/i)).toBeInTheDocument();
  });
});

test('toggles todo completion', async () => {
  render(<TodoApp />);
  
  // Wait for initial todos to load
  await waitFor(() => {
    expect(screen.getByText(/learn react/i)).toBeInTheDocument();
  });
  
  // Get the "Learn React" todo item and toggle it
  const todoItem = screen.getByText(/learn react/i).closest('li');
  const checkbox = todoItem.querySelector('input[type="checkbox"]');
  
  // Initial state: not completed
  expect(checkbox).not.toBeChecked();
  
  // Toggle completion
  fireEvent.click(checkbox);
  
  // Wait for update and check if it's completed
  await waitFor(() => {
    expect(checkbox).toBeChecked();
  });
});

test('deletes a todo', async () => {
  render(<TodoApp />);
  
  // Wait for initial todos to load
  await waitFor(() => {
    expect(screen.getByText(/learn react/i)).toBeInTheDocument();
  });
  
  // Get the "Learn React" todo item and delete it
  const todoItem = screen.getByText(/learn react/i).closest('li');
  const deleteButton = todoItem.querySelector('.delete-btn');
  
  fireEvent.click(deleteButton);
  
  // Check if the todo is removed
  await waitFor(() => {
    expect(screen.queryByText(/learn react/i)).not.toBeInTheDocument();
  });
  
  // "Learn Testing" should still be there
  expect(screen.getByText(/learn testing/i)).toBeInTheDocument();
});
```

#### Topik 9.4: Advanced Debugging
**Durasi**: 1 hari  
**Materi**:
- React DevTools
- Chrome DevTools for React
- Component stack traces
- Error boundaries
- Debugging performance issues
- Debugging memory leaks
- Debugging strategies

**Hands-on Practice**:
```jsx
// Error Boundary implementation
class ErrorBoundary extends React.Component {
  constructor(props) {
    super(props);
    this.state = { hasError: false, error: null, errorInfo: null };
  }

  static getDerivedStateFromError(error) {
    // Update state so the next render will show the fallback UI
    return { hasError: true };
  }

  componentDidCatch(error, errorInfo) {
    // Log the error to an error reporting service
    console.error('Error caught by boundary:', error, errorInfo);
    this.setState({ error, errorInfo });
    
    // You can also log to an error reporting service here
    // logErrorToService(error, errorInfo);
  }

  render() {
    if (this.state.hasError) {
      // Fallback UI when an error occurs
      return (
        <div className="error-boundary">
          <h2>Something went wrong</h2>
          {this.props.fallback || <p>Please try again later</p>}
          
          {process.env.NODE_ENV !== 'production' && (
            <details>
              <summary>Error details</summary>
              <p>{this.state.error && this.state.error.toString()}</p>
              <pre>
                {this.state.errorInfo && this.state.errorInfo.componentStack}
              </pre>
            </details>
          )}
        </div>
      );
    }

    return this.props.children;
  }
}

// Usage
function App() {
  return (
    <div>
      <h1>My App</h1>
      
      <ErrorBoundary fallback={<p>Error in counter component</p>}>
        <Counter />
      </ErrorBoundary>
      
      <ErrorBoundary fallback={<p>Error in user profile component</p>}>
        <UserProfile userId={1} />
      </ErrorBoundary>
    </div>
  );
}

// Component with memory leak
function LeakyComponent() {
  useEffect(() => {
    // Set up an interval
    const intervalId = setInterval(() => {
      console.log('This will keep running...');
    }, 1000);
    
    // Missing cleanup function!
    // Should return () => clearInterval(intervalId);
  }, []);
  
  return <div>I might leak memory!</div>;
}

// Fixed component
function FixedComponent() {
  useEffect(() => {
    // Set up an interval
    const intervalId = setInterval(() => {
      console.log('This will clean up properly');
    }, 1000);
    
    // Proper cleanup function
    return () => {
      console.log('Cleaning up interval');
      clearInterval(intervalId);
    };
  }, []);
  
  return <div>I clean up properly!</div>;
}

// Using React DevTools programmatically
function DebugComponent() {
  // Add debug name to hooks for DevTools
  const [count, setCount] = useDebugValue('count', count => `Count: ${count}`);
  
  // Debug reference values
  const buttonRef = useRef();
  useEffect(() => {
    // Access and log DOM element properties
    if (buttonRef.current) {
      console.log('Button element:', buttonRef.current);
    }
  }, []);
  
  return (
    <div>
      <p>Count: {count}</p>
      <button 
        ref={buttonRef}
        onClick={() => setCount(count + 1)}
      >
        Increment
      </button>
    </div>
  );
}
```

**Project Modul 9**:  
Membuat Test suite untuk aplikasi React:
- Unit tests untuk utils dan hooks
- Component tests dengan React Testing Library
- Integration tests untuk workflows
- Performance test implementation
- End-to-end testing dengan Cypress
- CI/CD implementation untuk testing
- Test coverage reporting

### MODUL 10: SERVER-SIDE RENDERING & STATIC SITE GENERATION

#### Topik 10.1: Next.js Fundamentals
**Durasi**: 1 hari  
**Materi**:
- Next.js vs Create React App
- Pages dan routing di Next.js
- API routes
- Environment variables
- _app.js dan _document.js
- CSS Modules dan styling
- Public directory

**Hands-on Practice**:
```jsx
// pages/index.js - Home page
import Head from 'next/head';
import Link from 'next/link';
import styles from '../styles/Home.module.css';

export default function Home() {
  return (
    <div className={styles.container}>
      <Head>
        <title>My Next.js App</title>
        <meta name="description" content="Created with Next.js" />
        <link rel="icon" href="/favicon.ico" />
      </Head>

      <main className={styles.main}>
        <h1 className={styles.title}>
          Welcome to <a href="https://nextjs.org">Next.js!</a>
        </h1>

        <p className={styles.description}>
          Get started by editing{' '}
          <code className={styles.code}>pages/index.js</code>
        </p>

        <div className={styles.grid}>
          <Link href="/about">
            <a className={styles.card}>
              <h2>About &rarr;</h2>
              <p>Learn more about our company</p>
            </a>
          </Link>

          <Link href="/users">
            <a className={styles.card}>
              <h2>Users &rarr;</h2>
              <p>See a list of our users</p>
            </a>
          </Link>
        </div>
      </main>

      <footer className={styles.footer}>
        <p>My Next.js App</p>
      </footer>
    </div>
  );
}

// pages/about.js - About page
export default function About() {
  return (
    <div>
      <h1>About Us</h1>
      <p>This is the about page</p>
      <Link href="/">
        <a>Back to home</a>
      </Link>
    </div>
  );
}

// pages/users/index.js - Users list page
import Link from 'next/link';

export default function Users({ users }) {
  return (
    <div>
      <h1>Users</h1>
      <ul>
        {users.map(user => (
          <li key={user.id}>
            <Link href={`/users/${user.id}`}>
              <a>{user.name}</a>
            </Link>
          </li>
        ))}
      </ul>
      <Link href="/">
        <a>Back to home</a>
      </Link>
    </div>
  );
}

// getServerSideProps function to fetch data on each request
export async function getServerSideProps() {
  // Fetch data from an API
  const res = await fetch('https://jsonplaceholder.typicode.com/users');
  const users = await res.json();

  // Pass data to the page via props
  return { props: { users } };
}

// pages/users/[id].js - Dynamic user page
import { useRouter } from 'next/router';
import Link from 'next/link';

export default function User({ user }) {
  const router = useRouter();

  // If the page is still generating via fallback,
  // show a loading state
  if (router.isFallback) {
    return <div>Loading...</div>;
  }

  return (
    <div>
      <h1>{user.name}</h1>
      <p>Email: {user.email}</p>
      <p>Phone: {user.phone}</p>
      <Link href="/users">
        <a>Back to users</a>
      </Link>
    </div>
  );
}

// getStaticPaths defines which paths to pre-render
export async function getStaticPaths() {
  const res = await fetch('https://jsonplaceholder.typicode.com/users');
  const users = await res.json();

  // Generate paths for the first 5 users
  const paths = users.slice(0, 5).map(user => ({
    params: { id: user.id.toString() }
  }));

  return {
    paths,
    fallback: true // true, false, or 'blocking'
  };
}

// getStaticProps function to fetch data at build time
export async function getStaticProps({ params }) {
  try {
    const res = await fetch(`https://jsonplaceholder.typicode.com/users/${params.id}`);
    const user = await res.json();

    return {
      props: { user },
      // Re-generate page every 60 seconds if a request comes in
      revalidate: 60
    };
  } catch (error) {
    // If there's an error, return a 404 page
    return { notFound: true };
  }
}

// pages/api/hello.js - API route
export default function handler(req, res) {
  res.status(200).json({ name: 'John Doe' });
}

// pages/_app.js - Custom App component
import '../styles/globals.css';

function MyApp({ Component, pageProps }) {
  return (
    <div className="app-wrapper">
      <Component {...pageProps} />
    </div>
  );
}

export default MyApp;

// pages/_document.js - Custom Document component
import Document, { Html, Head, Main, NextScript } from 'next/document';

class MyDocument extends Document {
  render() {
    return (
      <Html lang="en">
        <Head>
          <link
            href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap"
            rel="stylesheet"
          />
        </Head>
        <body>
          <Main />
          <NextScript />
        </body>
      </Html>
    );
  }
}

export default MyDocument;
```

#### Topik 10.2: Server-Side Rendering
**Durasi**: 1 hari  
**Materi**:
- SSR concepts
- getServerSideProps
- Dynamic routing
- Authentication dengan SSR
- Handling cookies server-side
- Error handling
- Performance optimization

**Hands-on Practice**:
```jsx
// pages/dashboard.js - Protected dashboard page with SSR
import { useState } from 'react';
import { useRouter } from 'next/router';
import cookies from 'next-cookies';

export default function Dashboard({ user, data }) {
  const router = useRouter();
  const [loading, setLoading] = useState(false);
  
  const handleLogout = async () => {
    setLoading(true);
    try {
      await fetch('/api/logout', { method: 'POST' });
      router.push('/login');
    } catch (error) {
      console.error('Logout failed', error);
      setLoading(false);
    }
  };
  
  return (
    <div>
      <h1>Welcome, {user.name}</h1>
      <p>Email: {user.email}</p>
      
      <h2>Your Data</h2>
      <ul>
        {data.map(item => (
          <li key={item.id}>{item.title}</li>
        ))}
      </ul>
      
      <button onClick={handleLogout} disabled={loading}>
        {loading ? 'Logging out...' : 'Logout'}
      </button>
    </div>
  );
}

// Server-side authentication and data fetching
export async function getServerSideProps(context) {
  // Get token from cookies
  const { token } = cookies(context);
  
  if (!token) {
    // If no token, redirect to login
    return {
      redirect: {
        destination: '/login',
        permanent: false,
      },
    };
  }
  
  try {
    // Validate token and get user
    const userRes = await fetch('https://api.example.com/me', {
      headers: {
        Authorization: `Bearer ${token}`
      }
    });
    
    if (!userRes.ok) {
      throw new Error('Failed to fetch user');
    }
    
    const user = await userRes.json();
    
    // Fetch user's data
    const dataRes = await fetch(`https://api.example.com/users/${user.id}/data`, {
      headers: {
        Authorization: `Bearer ${token}`
      }
    });
    
    if (!dataRes.ok) {
      throw new Error('Failed to fetch data');
    }
    
    const data = await dataRes.json();
    
    // Return data as props
    return {
      props: {
        user,
        data
      }
    };
  } catch (error) {
    // If error, clear cookie and redirect to login
    context.res.setHeader(
      'Set-Cookie',
      'token=; Path=/; Max-Age=0; HttpOnly; Secure; SameSite=Strict'
    );
    
    return {
      redirect: {
        destination: '/login?error=session_expired',
        permanent: false,
      },
    };
  }
}

// API route for logout
// pages/api/logout.js
export default function handler(req, res) {
  if (req.method !== 'POST') {
    return res.status(405).json({ message: 'Method not allowed' });
  }
  
  // Clear the auth cookie
  res.setHeader(
    'Set-Cookie',
    'token=; Path=/; Max-Age=0; HttpOnly; Secure; SameSite=Strict'
  );
  
  res.status(200).json({ success: true });
}
```

#### Topik 10.3: Static Site Generation
**Durasi**: 1 hari  
**Materi**:
- Static Generation concepts
- getStaticProps
- getStaticPaths
- Incremental Static Regeneration
- Dynamic routing dengan SSG
- Data fetching strategies
- Image optimization

**Hands-on Practice**:
```jsx
// pages/blog/index.js - Blog posts list
import Link from 'next/link';
import Image from 'next/image';

export default function Blog({ posts }) {
  return (
    <div>
      <h1>Blog</h1>
      <div className="posts-grid">
        {posts.map(post => (
          <Link key={post.id} href={`/blog/${post.slug}`}>
            <a className="post-card">
              <div className="image-container">
                <Image
                  src={post.coverImage}
                  alt={post.title}
                  width={600}
                  height={400}
                  layout="responsive"
                  placeholder="blur"
                  blurDataURL={post.coverImageBlur}
                />
              </div>
              <h2>{post.title}</h2>
              <p>{post.excerpt}</p>
              <div className="post-meta">
                <span>{new Date(post.date).toLocaleDateString()}</span>
                <span>•</span>
                <span>{post.readingTime} min read</span>
              </div>
            </a>
          </Link>
        ))}
      </div>
    </div>
  );
}

// Fetch posts at build time
export async function getStaticProps() {
  const posts = await fetch('https://api.example.com/posts')
    .then(res => res.json());
  
  return {
    props: {
      posts
    },
    // Regenerate page every 10 minutes
    revalidate: 600
  };
}

// pages/blog/[slug].js - Individual blog post
import Image from 'next/image';
import Link from 'next/link';
import { MDXRemote } from 'next-mdx-remote';
import { serialize } from 'next-mdx-remote/serialize';

export default function BlogPost({ post, content }) {
  return (
    <article>
      <div className="post-header">
        <h1>{post.title}</h1>
        <div className="post-meta">
          <span>{new Date(post.date).toLocaleDateString()}</span>
          <span>•</span>
          <span>{post.readingTime} min read</span>
        </div>
      </div>
      
      <div className="post-cover">
        <Image
          src={post.coverImage}
          alt={post.title}
          width={1200}
          height={600}
          layout="responsive"
          priority
        />
      </div>
      
      <div className="post-content">
        <MDXRemote {...content} />
      </div>
      
      <div className="post-footer">
        <div className="author">
          <Image
            src={post.author.avatar}
            alt={post.author.name}
            width={50}
            height={50}
            className="avatar"
          />
          <div>
            <h3>{post.author.name}</h3>
            <p>{post.author.bio}</p>
          </div>
        </div>
        
        <div className="post# KURIKULUM DEVELOPER REACT EXPERT

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

## DETAIL MODUL

### MODUL 1: PENGENALAN WEB DEVELOPMENT

#### Topik 1.1: HTML5 dan Semantic Elements
**Durasi**: 1 hari  
**Materi**:
- Struktur dokumen HTML5
- Semantic elements: `<header>`, `<footer>`, `<section>`, `<article>`, `<nav>`, `<aside>`
- Atribut data- dan role
- Aksesibilitas dasar (ARIA)

**Hands-on Practice**:
- Membuat struktur halaman web yang semantik
- Mengimplementasikan form dengan validasi HTML5

#### Topik 1.2: CSS3, Flexbox dan Grid
**Durasi**: 1 hari  
**Materi**:
- CSS Selectors dan specificity
- Box model dan layout
- Flexbox untuk one-dimensional layout
- CSS Grid untuk two-dimensional layout
- Responsive design dengan media queries

**Hands-on Practice**:
- Membuat layout responsive dengan Flexbox
- Mengimplementasikan grid layout kompleks

#### Topik 1.3: JavaScript Fundamentals
**Durasi**: 2 hari  
**Materi**:
- Tipe data, variabel, dan scope
- Functions dan closures
- Objects dan arrays
- Prototype inheritance
- Error handling

**Hands-on Practice**:
- Mengimplementasikan algoritma dasar
- Membuat fungsi-fungsi utility

#### Topik 1.4: Modern JavaScript (ES6+)
**Durasi**: 2 hari  
**Materi**:
- Arrow functions
- Template literals
- Destructuring assignment
- Spread/rest operators
- Default parameters
- Classes
- Modules (import/export)
- Promises dan async/await

**Hands-on Practice**:
- Refactoring kode ES5 ke ES6+
- Implementasi asynchronous operations

**Project Modul 1**:  
Membuat landing page responsive dengan fitur:
- Navigasi sticky
- Hero section dengan animasi
- Gallery dengan grid layout
- Form validasi dengan JavaScript
- Dark/light mode toggle

### MODUL 2: PENGENALAN REACT

#### Topik 2.1: Pengenalan dan Setup
**Durasi**: 1 hari  
**Materi**:
- Apa itu React dan mengapa menggunakannya
- Virtual DOM dan diffing algorithm
- Single Page Application
- Setting up environment dengan Create React App
- React Developer Tools

**Hands-on Practice**:
- Membuat project pertama dengan Create React App
- Eksplorasi struktur project
- Menggunakan React Developer Tools

#### Topik 2.2: JSX dan Elements
**Durasi**: 1 hari  
**Materi**:
- Sintaks JSX
- Expressions di JSX
- Atribut di JSX
- Children elements
- Fragments
- Perbedaan JSX dengan HTML

**Hands-on Practice**:
- Menulis berbagai expressions di JSX
- Mengkonversi HTML ke JSX

#### Topik 2.3: Function dan Class Components
**Durasi**: 2 hari  
**Materi**:
- Function Components dasar
- Class Components dasar
- Perbedaan Function dan Class Components
- Props dan PropTypes
- Default Props
- Children prop

**Hands-on Practice**:
```jsx
// Function Component
function Greeting({ name = "Guest", role }) {
  return (
    <div className="greeting">
      <h2>Hello, {name}!</h2>
      {role && <p>Your role: {role}</p>}
    </div>
  );
}

#### Topik 7.2: Custom Hooks Development
**Durasi**: 1 hari  
**Materi**:
- Creating custom hooks
- Composing multiple hooks
- Rules of hooks
- Testing custom hooks
- Custom hooks best practices
- Reusable logic patterns

**Hands-on Practice**:
```jsx
// useLocalStorage hook
function useLocalStorage(key, initialValue) {
  // State to store our value
  const [storedValue, setStoredValue] = useState(() => {
    try {
      // Get from local storage by key
      const item = window.localStorage.getItem(key);
      // Parse stored json or if none return initialValue
      return item ? JSON.parse(item) : initialValue;
    } catch (error) {
      console.error(error);
      return initialValue;
    }
  });

  // Return a wrapped version of useState's setter function that
  // persists the new value to localStorage
  const setValue = (value) => {
    try {
      // Allow value to be a function
      const valueToStore =
        value instanceof Function ? value(storedValue) : value;
      // Save state
      setStoredValue(valueToStore);
      // Save to local storage
      window.localStorage.setItem(key, JSON.stringify(valueToStore));
    } catch (error) {
      console.error(error);
    }
  };

  return [storedValue, setValue];
}

// useMediaQuery hook
function useMediaQuery(query) {
  const [matches, setMatches] = useState(() => window.matchMedia(query).matches);

  useEffect(() => {
    const mediaQuery = window.matchMedia(query);
    const handler = (event) => setMatches(event.matches);
    
    // Set up event listener
    mediaQuery.addEventListener('change', handler);
    
    // Initial check
    setMatches(mediaQuery.matches);
    
    // Clean up
    return () => mediaQuery.removeEventListener('change', handler);
  }, [query]);

  return matches;
}

// useDebounce hook
function useDebounce(value, delay) {
  const [debouncedValue, setDebouncedValue] = useState(value);
  
  useEffect(() => {
    // Set debouncedValue to value after the specified delay
    const handler = setTimeout(() => {
      setDebouncedValue(value);
    }, delay);
    
    // Cancel the timeout if value changes or unmounts
    return () => {
      clearTimeout(handler);
    };
  }, [value, delay]);
  
  return debouncedValue;
}

// Using the custom hooks
function ThemeToggler() {
  // Use our custom localStorage hook
  const [theme, setTheme] = useLocalStorage('theme', 'light');
  
  // Use our custom media query hook
  const prefersDark = useMediaQuery('(prefers-color-scheme: dark)');
  
  useEffect(() => {
    // Set theme based on user's system preference on initial load
    if (prefersDark && theme === 'light') {
      setTheme('dark');
    }
  }, [prefersDark, setTheme, theme]);
  
  const toggleTheme = () => {
    setTheme(theme === 'light' ? 'dark' : 'light');
  };
  
  return (
    <button onClick={toggleTheme}>
      Current theme: {theme}
    </button>
  );
}

function SearchComponent() {
  const [searchTerm, setSearchTerm] = useState('');
  // Use our debounce hook to delay API calls
  const debouncedSearchTerm = useDebounce(searchTerm, 500);
  const [results, setResults] = useState([]);
  const [loading, setLoading] = useState(false);
  
  useEffect(() => {
    if (debouncedSearchTerm) {
      setLoading(true);
      // Make API call with debounced value
      fetchSearchResults(debouncedSearchTerm)
        .then(data => {
          setResults(data);
          setLoading(false);
        });
    } else {
      setResults([]);
    }
  }, [debouncedSearchTerm]);
  
  return (
    <div>
      <input
        value={searchTerm}
        onChange={(e) => setSearchTerm(e.target.value)}
        placeholder="Search..."
      />
      {loading && <p>Loading...</p>}
      <ul>
        {results.map(result => (
          <li key={result.id}>{result.name}</li>
        ))}
      </ul>
    </div>
  );
}
```

#### Topik 7.3: Advanced Component Patterns
**Durasi**: 2 hari  
**Materi**:
- Higher-Order Components (HOC)
- Render Props
- Compound Components
- Controlled vs Uncontrolled Components
- State Initializers
- Prop Collections and Getters

**Hands-on Practice**:
```jsx
// Higher-Order Component
function withLogger(Component) {
  const displayName = Component.displayName || Component.name || 'Component';
  
  function WithLogger(props) {
    useEffect(() => {
      console.log(`${displayName} mounted`);
      return () => {
        console.log(`${displayName} unmounted`);
      };
    }, []);
    
    console.log(`${displayName} rendered with props:`, props);
    
    return <Component {...props} />;
  }
  
  WithLogger.displayName = `withLogger(${displayName})`;
  
  return WithLogger;
}

// Usage of HOC
const EnhancedButton = withLogger(Button);

// Render Props pattern
function Toggle({ children }) {
  const [on, setOn] = useState(false);
  
  const toggle = () => setOn(!on);
  
  return children({
    on,
    toggle
  });
}

// Usage of Render Props
function App() {
  return (
    <Toggle>
      {({ on, toggle }) => (
        <div>
          <button onClick={toggle}>
            {on ? 'Turn off' : 'Turn on'}
          </button>
          <div>{on ? 'The switch is on' : 'The switch is off'}</div>
        </div>
      )}
    </Toggle>
  );
}

// Compound Components pattern
const TabContext = createContext();

function Tabs({ children, defaultIndex = 0 }) {
  const [activeIndex, setActiveIndex] = useState(defaultIndex);
  
  const value = {
    activeIndex,
    setActiveIndex
  };
  
  return (
    <TabContext.Provider value={value}>
      <div className="tabs">{children}</div>
    </TabContext.Provider>
  );
}

function TabList({ children }) {
  return <div className="tab-list">{children}</div>;
}

function Tab({ children, index }) {
  const { activeIndex, setActiveIndex } = useContext(TabContext);
  
  return (
    <button
      className={`tab ${activeIndex === index ? 'active' : ''}`}
      onClick={() => setActiveIndex(index)}
    >
      {children}
    </button>
  );
}

function TabPanels({ children }) {
  return <div className="tab-panels">{children}</div>;
}

function TabPanel({ children, index }) {
  const { activeIndex } = useContext(TabContext);
  
  return activeIndex === index ? (
    <div className="tab-panel">{children}</div>
  ) : null;
}

// Attach components as properties
Tabs.TabList = TabList;
Tabs.Tab = Tab;
Tabs.TabPanels = TabPanels;
Tabs.TabPanel = TabPanel;

// Usage of Compound Components
function App() {
  return (
    <Tabs defaultIndex={1}>
      <Tabs.TabList>
        <Tabs.Tab index={0}>Tab 1</Tabs.Tab>
        <Tabs.Tab index={1}>Tab 2</Tabs.Tab>
        <Tabs.Tab index={2}>Tab 3</Tabs.Tab>
      </Tabs.TabList>
      
      <Tabs.TabPanels>
        <Tabs.TabPanel index={0}>
          <h2>Panel 1</h2>
          <p>Content for Panel 1</p>
        </Tabs.TabPanel>
        <Tabs.TabPanel index={1}>
          <h2>Panel 2</h2>
          <p>Content for Panel 2</p>
        </Tabs.TabPanel>
        <Tabs.TabPanel index={2}>
          <h2>Panel 3</h2>
          <p>Content for Panel 3</p>
        </Tabs.TabPanel>
      </Tabs.TabPanels>
    </Tabs>
  );
}

// Prop Getters pattern
function useToggle() {
  const [on, setOn] = useState(false);
  
  const toggle = () => setOn(!on);
  
  // Function to get props for the toggle button
  const getTogglerProps = ({ onClick, ...props } = {}) => ({
    'aria-pressed': on,
    onClick: (event) => {
      // Call provided onClick if it exists
      onClick?.(event);
      // Call our toggle function
      toggle();
    },
    ...props
  });
  
  return {
    on,
    toggle,
    getTogglerProps
  };
}

// Usage of Prop Getters
function App() {
  const { on, getTogglerProps } = useToggle();
  
  return (
    <div>
      <button
        {...getTogglerProps({
          'aria-label': 'Toggle feature',
          onClick: () => console.log('Button clicked'),
          className: on ? 'active' : ''
        })}
      >
        {on ? 'ON' : 'OFF'}
      </button>
      <div>{on ? 'Feature enabled' : 'Feature disabled'}</div>
    </div>
  );
}
```

#### Topik 7.4: State Management Patterns
**Durasi**: 2 hari  
**Materi**:
- Context + useReducer pattern
- State machines
- Finite state management
- Custom store implementations
- Observer pattern
- Atomic state management

**Hands-on Practice**:
```jsx
// Context + useReducer pattern
const TodoContext = createContext();

const initialState = {
  todos: [],
  filter: 'all',
  loading: false,
  error: null
};

function todoReducer(state, action) {
  switch (action.type) {
    case 'FETCH_START':
      return { ...state, loading: true, error: null };
    case 'FETCH_SUCCESS':
      return { ...state, loading: false, todos: action.payload };
    case 'FETCH_ERROR':
      return { ...state, loading: false, error: action.payload };
    case 'ADD_TODO':
      return { ...state, todos: [...state.todos, action.payload] };
    case 'TOGGLE_TODO':
      return {
        ...state,
        todos: state.todos.map(todo =>
          todo.id === action.payload
            ? { ...todo, completed: !todo.completed }
            : todo
        )
      };
    case 'DELETE_TODO':
      return {
        ...state,
        todos: state.todos.filter(todo => todo.id !== action.payload)
      };
    case 'SET_FILTER':
      return { ...state, filter: action.payload };
    default:
      return state;
  }
}

function TodoProvider({ children }) {
  const [state, dispatch] = useReducer(todoReducer, initialState);
  
  // Memoize the context value to prevent unnecessary re-renders
  const value = useMemo(() => [state, dispatch], [state]);
  
  return (
    <TodoContext.Provider value={value}>
      {children}
    </TodoContext.Provider>
  );
}

// Custom hook to use the todo context
function useTodo() {
  const context = useContext(TodoContext);
  if (!context) {
    throw new Error('useTodo must be used within a TodoProvider');
  }
  return context;
}

// Simple state machine implementation
function createMachine(initialState, transitions) {
  return {
    value: initialState,
    transition(currentState, event) {
      const nextState = transitions[currentState]?.[event];
      return nextState !== undefined ? nextState : currentState;
    }
  };
}

function useMachine(machine) {
  const [state, setState] = useState(machine.value);
  
  const send = useCallback((event) => {
    setState(s => machine.transition(s, event));
  }, [machine]);
  
  return [state, send];
}

// Usage of state machine
const trafficLightMachine = createMachine('red', {
  red: { NEXT: 'green' },
  green: { NEXT: 'yellow' },
  yellow: { NEXT: 'red' }
});

function TrafficLight() {
  const [state, send] = useMachine(trafficLightMachine);
  
  return (
    <div className="traffic-light">
      <div className={`light red ${state === 'red' ? 'active' : ''}`} />
      <div className={`light yellow ${state === 'yellow' ? 'active' : ''}`} />
      <div className={`light green ${state === 'green' ? 'active' : ''}`} />
      
      <button onClick={() => send('NEXT')}>
        Change to next light
      </button>
    </div>
  );
}

// Custom observable store implementation
function createStore(initialState) {
  let state = initialState;
  const listeners = new Set();
  
  const getState = () => state;
  
  const setState = (newState) => {
    state = typeof newState === 'function' ? newState(state) : newState;
    listeners.forEach(listener => listener(state));
  };
  
  const subscribe = (listener) => {
    listeners.add(listener);
    return () => listeners.delete(listener);
  };
  
  return { getState, setState, subscribe };
}

// React hook to use the custom store
function useStore(store) {
  const [state, setState] = useState(store.getState());
  
  useEffect(() => {
    const unsubscribe = store.subscribe(setState);
    return unsubscribe;
  }, [store]);
  
  return [state, store.setState];
}

// Usage of custom store
const counterStore = createStore({ count: 0 });

function Counter() {
  const [state, setState] = useStore(counterStore);
  
  const increment = () => {
    setState(s => ({ count: s.count + 1 }));
  };
  
  const decrement = () => {
    setState(s => ({ count: s.count - 1 }));
  };
  
  return (
    <div>
      <p>Count: {state.count}</p>
      <button onClick={decrement}>-</button>
      <button onClick={increment}>+</button>
    </div>
  );
}
```

**Project Modul 7**:  
Membuat Library of reusable React components:
- Component library dengan storybook
- Compound components untuk kompleksitas UI
- Hook libraries untuk reusable logic
- Custom form components dengan validation
- Themeable components dengan styled-components
- Accessible component design
- Component API dokumentasi

### MODUL 8: PERFORMANCE OPTIMIZATION

#### Topik 8.1: Measuring Performance
**Durasi**: 1 hari  
**Materi**:
- React DevTools Profiler
- Chrome DevTools Performance tab
- Lighthouse audit
- Performance metrics (FCP, LCP, TTI, CLS)
- Performance budgets
- Identifying bottlenecks

**Hands-on Practice**:
```jsx
// Example of using React Profiler programmatically
import { Profiler } from 'react';

function onRenderCallback(
  id, // the "id" prop of the Profiler tree that just committed
  phase, // either "mount" (if the tree just mounted) or "update" (if it re-rendered)
  actualDuration, // time spent rendering the committed update
  baseDuration, // estimated time to render the entire subtree without memoization
  startTime, // when React began rendering this update
  commitTime, // when React committed this update
  interactions // the Set of interactions belonging to this update
) {
  // Log performance data
  console.log({
    id,
    phase,
    actualDuration,
    baseDuration,
    startTime,
    commitTime
  });
}

function App() {
  return (
    <Profiler id="main-app" onRender={onRenderCallback}>
      <MainComponent />
    </Profiler>
  );
}

// Custom hook to track component renders
function useRenderCount() {
  const count = useRef(1);
  
  useEffect(() => {
    count.current += 1;
  });
  
  return count.current;
}

function ExpensiveComponent({ data }) {
  const renderCount = useRenderCount();
  
  console.log(`ExpensiveComponent rendered ${renderCount} times`);
  
  // Simulate expensive calculation
  const processedData = useMemo(() => {
    console.time('processData');
    const result = expensiveCalculation(data);
    console.timeEnd('processData');
    return result;
  }, [data]);
  
  return (
    <div>
      <p>Render count: {renderCount}</p>
      <ul>
        {processedData.map(item => (
          <li key={item.id}>{item.name}</li>
        ))}
      </ul>
    </div>
  );
}
```

#### Topik 8.2: Component Optimization
**Durasi**: 1 hari  
**Materi**:
- React.memo
- shouldComponentUpdate
- PureComponent
- Using keys properly
- Avoiding props spreading
- Avoiding anonymous functions
- Avoiding inline objects

**Hands-on Practice**:
```jsx
// Before optimization
function ItemList({ items, onItemClick }) {
  console.log('ItemList rendering');
  
  return (
    <ul>
      {items.map(item => (
        <li 
          key={item.id}
          onClick={() => onItemClick(item.id)}
          style={{ margin: '10px', padding: '10px' }}
        >
          {item.name}
        </li>
      ))}
    </ul>
  );
}

// After optimization with React.memo
const MemoizedItem = React.memo(function Item({ item, onClick }) {
  console.log(`Item ${item.id} rendering`);
  
  // Extract inline function to component level
  const handleClick = () => {
    onClick(item.id);
  };
  
  // Extract inline styles
  const itemStyle = { margin: '10px', padding: '10px' };
  
  return (
    <li 
      onClick={handleClick}
      style={itemStyle}
    >
      {item.name}
    </li>
  );
});

const MemoizedItemList = React.memo(function ItemList({ items, onItemClick }) {
  console.log('ItemList rendering');
  
  return (
    <ul>
      {items.map(item => (
        <MemoizedItem 
          key={item.id}
          item={item}
          onClick={onItemClick}
        />
      ))}
    </ul>
  );
});

// Using useCallback to prevent function recreation
function ParentComponent() {
  const [items, setItems] = useState([/* items data */]);
  
  // Memoize the click handler
  const handleItemClick = useCallback((id) => {
    console.log(`Item ${id} clicked`);
    // Other logic...
  }, []);
  
  return (
    <MemoizedItemList 
      items={items}
      onItemClick={handleItemClick}
    />
  );
}

// Class component optimization with PureComponent
class PureList extends React.PureComponent {
  render() {
    const { items, onItemClick } = this.props;
    
    return (
      <ul>
        {items.map(item => (
          <li 
            key={item.id}
            onClick={() => onItemClick(item.id)}
          >
            {item.name}
          </li>
        ))}
      </ul>
    );
  }
}

// Manual shouldComponentUpdate implementation
class ManualOptimizedList extends React.Component {
  shouldComponentUpdate(nextProps) {
    // Only re-render if items array reference changed
    return this.props.items !== nextProps.items;
  }
  
  render() {
    const { items, onItemClick } = this.props;
    
    return (
      <ul>
        {items.map(item => (
          <li 
            key={item.id}
            onClick={() => onItemClick(item.id)}
          >
            {item.name}
          </li>
        ))}
      </ul>
    );
  }
}
```

#### Topik 8.3: Code Splitting & Lazy Loading
**Durasi**: 1 hari  
**Materi**:
- Dynamic imports
- React.lazy
- Suspense
- Route-based code splitting
- Component-based code splitting
- Preloading strategies
- Loading states

**Hands-on Practice**:
```jsx
import React, { Suspense, lazy } from 'react';
import { BrowserRouter as Router, Route, Switch } from 'react-router-dom';
import ErrorBoundary from './ErrorBoundary';

// Regular import
import Home from './pages/Home';
import Loading from './components/Loading';

// Lazy imports
const About = lazy(() => import('./pages/About'));
const Dashboard = lazy(() => import('./pages/Dashboard'));
const Profile = lazy(() => import('./pages/Profile'));

// Prefetch component when mouse hovers over link
function prefetchAbout() {
  import('./pages/About');
}

function App() {
  return (
    <Router>
      <nav>
        <a href="/">Home</a>
        <a href="/about" onMouseEnter={prefetchAbout}>About</a>
        <a href="/dashboard">Dashboard</a>
        <a href="/profile">Profile</a>
      </nav>
      
      <ErrorBoundary fallback={<p>Something went wrong</p>}>
        <Suspense fallback={<Loading />}>
          <Switch>
            <Route exact path="/" component={Home} />
            <Route path="/about" component={About} />
            <Route path="/dashboard" component={Dashboard} />
            <Route path="/profile" component={Profile} />
          </Switch>
        </Suspense>
      </ErrorBoundary>
    </Router>
  );
}

// Component-level code splitting
function MyImageGallery() {
  const [showGallery, setShowGallery] = useState(false);
  
  // Lazy load the heavy gallery component
  const Gallery = lazy(() => import('./components/Gallery'));
  
  return (
    <div>
      <button onClick={() => setShowGallery(true)}>
        Show Gallery
      </button>
      
      {showGallery && (
        <Suspense fallback={<p>Loading gallery...</p>}>
          <Gallery />
        </Suspense>
      )}
    </div>
  );
}
```

#### Topik 8.4: Virtualization & Windowing
**Durasi**: 1 hari  
**Materi**:
- Virtual scrolling concepts
- react-window
- react-virtualized
- IntersectionObserver
- Lazy loading images
- Infinite scroll implementation
- Load-on-demand strategies

**Hands-on Practice**:
```jsx
import { FixedSizeList } from 'react-window';
import { useState, useRef, useCallback } from 'react';

// Basic react-window implementation
function VirtualizedList({ items }) {
  // Row renderer
  const Row = ({ index, style }) => (
    <div style={style} className="list-item">
      {items[index].name}
    </div>
  );
  
  return (
    <FixedSizeList
      height={400}
      width="100%"
      itemCount={items.length}
      itemSize={50}
    >
      {Row}
    </FixedSizeList>
  );
}

// Infinite scroll with IntersectionObserver
function InfiniteScrollList() {
  const [items, setItems] = useState([]);
  const [page, setPage] = useState(1);
  const [loading, setLoading] = useState(false);
  const [hasMore, setHasMore] = useState(true);
  
  const observer = useRef();
  
  const lastItemRef = useCallback(node => {
    if (loading) return;
    
    if (observer.current) {
      observer.current.disconnect();
    }
    
    observer.current = new IntersectionObserver(entries => {
      if (entries[0].isIntersecting && hasMore) {
        loadMoreItems();
      }
    });
    
    if (node) {
      observer.current.observe(node);
    }
  }, [loading, hasMore]);
  
  const loadMoreItems = async () => {
    setLoading(true);
    try {
      const newItems = await fetchItems(page);
      if (newItems.length === 0) {
        setHasMore(false);
      } else {
        setItems(prev => [...prev, ...newItems]);
        setPage(prev => prev + 1);
      }
    } catch (error) {
      console.error('Error loading more items:', error);
    } finally {
      setLoading(false);
    }
  };
  
  return (
    <div className="infinite-scroll-list">
      {items.map((item, index) => (
        <div
          key={item.id}
          ref={index === items.length - 1 ? lastItemRef : null}
          className="list-item"
        >
          {item.name}
        </div>
      ))}
      {loading && <div className="loading">Loading...</div>}
      {!hasMore && <div>No more items</div>}
    </div>
  );
}

// Lazy loading images with IntersectionObserver
function LazyImage({ src, alt, placeholder }) {
  const [isLoaded, setIsLoaded] = useState(false);
  const imgRef = useRef();
  
  useEffect(() => {
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const img = entry.target;
          const realSrc = img.dataset.src;
          img.src = realSrc;
          img.addEventListener('load', () => {
            setIsLoaded(true);
            observer.unobserve(img);
          });
        }
      });
    });
    
    if (imgRef.current) {
      observer.observe(imgRef.current);
    }
    
    return () => {
      if (imgRef.current) {
        observer.unobserve(imgRef.current);
      }
    };
  }, []);
  
  return (
    <div className={`lazy-image ${isLoaded ? 'loaded' : ''}`}>
      <img
        ref={imgRef}
        data-src={src}
        src={placeholder}
        alt={alt}
      />
      {!isLoaded && <div className="placeholder" />}
    </div>
  );
}
```

#### Topik 8.5: Bundle Optimization
**Durasi**: 1 hari  
**Materi**:
- Webpack configuration
- Tree shaking
- Bundle analyzer
- Reducing bundle size
- Code splitting strategies
- Dynamic imports
- Compression techniques

**Hands-on Practice**:
```javascript
// webpack.config.js example
const path = require('path');
const BundleAnalyzerPlugin = require('webpack-bundle-analyzer').BundleAnalyzerPlugin;
const CompressionPlugin = require('compression-webpack-plugin');
const TerserPlugin = require('terser-webpack-plugin');

module.exports = {
  entry: './src/index.js',
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: '[name].[contenthash].js',
    chunkFilename: '[name].[contenthash].chunk.js',
  },
  optimization: {
    minimizer: [new TerserPlugin()],
    splitChunks: {
      chunks: 'all',
      cacheGroups: {
        vendors: {
          test: /[\\/]node_modules[\\/]/,
          name: 'vendors',
          chunks: 'all',
          priority: -10,
        },
        common: {
          name: 'common',
          minChunks: 2,
          priority: -20,
          reuseExistingChunk: true,
        }
      }
    },
  },
  plugins: [
    new BundleAnalyzerPlugin({
      analyzerMode: 'static',
      reportFilename: 'bundle-report.html',
    }),
    new CompressionPlugin({
      algorithm: 'gzip',
      test: /\.(js|css|html|svg)$/,
      threshold: 10240, // Only compress files > 10kb
      minRatio: 0.8,
    }),
  ],
};

// React code examples for optimizing imports
// Bad - imports the entire lodash library
import _ from 'lodash';

// Good - only imports the specific methods needed
import map from 'lodash/map';
import filter from 'lodash/filter';

// Using dynamic imports for code splitting
const importExpensiveModule = () => import('./ExpensiveModule');

function MyComponent() {
  const [module, setModule] = useState(null);
  
  const loadModule = async () => {
    try {
      const { default: ExpensiveModule } = await importExpensiveModule();
      setModule(ExpensiveModule);
    } catch (error) {
      console.error('Failed to load module:', error);
    }
  };
  
  return (
    <div>
      <button onClick={loadModule}>Load Module</button>
      {module && <module.Component />}
    </div>
  );
}
```

**Project Modul 8**:  
Optimizing an existing React application:
- Performance audit with Lighthouse
- Memoization dan component optimizations
- Implementing lazy loading dan code splitting
- Virtual scroll

// Class Component
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
    this.increment = this.increment.bind(this);
  }
  
  increment() {
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

#### Topik 2.4: Event Handling
**Durasi**: 1 hari  
**Materi**:
- Event handling di React
- SyntheticEvent
- Binding event handlers
- Event pooling
- Passing arguments ke event handlers

**Hands-on Practice**:
```jsx
function ToggleButton() {
  const [isOn, setIsOn] = React.useState(false);
  
  // Event handler dengan parameter
  const handleClick = (event, newState) => {
    console.log(event.type); // "click"
    setIsOn(newState);
  };
  
  return (
    <button 
      className={isOn ? "btn-on" : "btn-off"}
      onClick={(e) => handleClick(e, !isOn)}
    >
      {isOn ? "ON" : "OFF"}
    </button>
  );
}
```

#### Topik 2.5: Component Composition
**Durasi**: 1 hari  
**Materi**:
- Containment
- Specialization
- Props.children
- Composition vs Inheritance
- Extracting Components

**Hands-on Practice**:
```jsx
// Component composition
function Card({ title, children }) {
  return (
    <div className="card">
      <div className="card-header">{title}</div>
      <div className="card-body">{children}</div>
    </div>
  );
}

function App() {
  return (
    <Card title="Welcome">
      <p>This is a reusable card component.</p>
      <button>Click me</button>
    </Card>
  );
}
```

**Project Modul 2**:  
Konversi landing page dari Modul 1 ke React:
- Memecah UI menjadi component hierarchy
- Mengimplementasikan navigation sebagai component
- Membuat reusable UI components (Button, Card, etc.)
- Menerapkan props untuk konfigurasi components
- Menerapkan event handling untuk interaksi

### MODUL 3: REACT FUNDAMENTALS

#### Topik 3.1: State dan Hooks Dasar
**Durasi**: 2 hari  
**Materi**:
- State concept
- useState hook
- Multiple state variables
- State updates
- State lifting
- Lazy initial state

**Hands-on Practice**:
```jsx
function Counter() {
  // Basic state
  const [count, setCount] = useState(0);
  
  // Object state
  const [user, setUser] = useState({
    name: 'Guest',
    isLoggedIn: false
  });
  
  // Update object state properly
  const login = () => {
    setUser(prevUser => ({
      ...prevUser,
      name: 'John',
      isLoggedIn: true
    }));
  };
  
  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(0)}>Reset</button>
      
      <hr />
      
      <p>
        {user.isLoggedIn ? `Welcome, ${user.name}!` : 'Please log in'}
      </p>
      <button onClick={login} disabled={user.isLoggedIn}>
        Log in
      </button>
    </div>
  );
}
```

#### Topik 3.2: Effects dan Lifecycle
**Durasi**: 2 hari  
**Materi**:
- useEffect hook
- Dependency array
- Cleanup function
- Component lifecycle dengan hooks
- Common useEffect patterns
- API calls dengan useEffect

**Hands-on Practice**:
```jsx
function UserProfile({ userId }) {
  const [profile, setProfile] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);
  
  useEffect(() => {
    // Reset state when userId changes
    setLoading(true);
    setError(null);
    
    let isMounted = true;
    
    async function fetchProfile() {
      try {
        const response = await fetch(`/api/users/${userId}`);
        if (!response.ok) throw new Error('Failed to fetch');
        
        const data = await response.json();
        
        // Only update state if component is still mounted
        if (isMounted) {
          setProfile(data);
          setLoading(false);
        }
      } catch (err) {
        if (isMounted) {
          setError(err.message);
          setLoading(false);
        }
      }
    }
    
    fetchProfile();
    
    // Cleanup function
    return () => {
      isMounted = false;
    };
  }, [userId]); // Re-run when userId changes
  
  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error}</p>;
  if (!profile) return null;
  
  return (
    <div className="profile">
      <h2>{profile.name}</h2>
      <p>Email: {profile.email}</p>
    </div>
  );
}
```

#### Topik 3.3: Conditional Rendering
**Durasi**: 1 hari  
**Materi**:
- If statements
- Inline conditions with && operator
- Conditional (ternary) operator
- Preventing component rendering
- Switch statement patterns

**Hands-on Practice**:
```jsx
function StatusMessage({ status }) {
  // Pattern 1: If statement
  if (status === 'loading') {
    return <Spinner />;
  }
  
  // Pattern 2: Immediate return for error
  if (status === 'error') {
    return <ErrorMessage />;
  }
  
  // Pattern 3: Ternary operator
  return (
    <div>
      {status === 'success' 
        ? <SuccessMessage /> 
        : <p>Unknown status: {status}</p>}
      
      {/* Pattern 4: && operator */}
      {status === 'warning' && <WarningBanner />}
    </div>
  );
}
```

#### Topik 3.4: Lists dan Keys
**Durasi**: 1 hari  
**Materi**:
- Rendering multiple components
- Keys dan pentingnya
- Extracting components dengan keys
- Keys harus unik di antara siblings
- Best practices untuk keys

**Hands-on Practice**:
```jsx
function TodoList({ todos, onToggle, onDelete }) {
  return (
    <ul className="todo-list">
      {todos.map(todo => (
        <TodoItem
          key={todo.id}
          todo={todo}
          onToggle={onToggle}
          onDelete={onDelete}
        />
      ))}
    </ul>
  );
}

function TodoItem({ todo, onToggle, onDelete }) {
  return (
    <li className={todo.completed ? 'completed' : ''}>
      <input
        type="checkbox"
        checked={todo.completed}
        onChange={() => onToggle(todo.id)}
      />
      <span>{todo.text}</span>
      <button onClick={() => onDelete(todo.id)}>Delete</button>
    </li>
  );
}
```

#### Topik 3.5: Forms dan Controlled Components
**Durasi**: 2 hari  
**Materi**:
- Controlled components
- Handling multiple inputs
- Uncontrolled components
- Form validation
- React Hook Form

**Hands-on Practice**:
```jsx
function ContactForm() {
  const [formData, setFormData] = useState({
    name: '',
    email: '',
    message: ''
  });
  const [errors, setErrors] = useState({});
  
  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData(prev => ({
      ...prev,
      [name]: value
    }));
    
    // Clear error when user types
    if (errors[name]) {
      setErrors(prev => ({
        ...prev,
        [name]: null
      }));
    }
  };
  
  const validate = () => {
    const newErrors = {};
    
    if (!formData.name.trim()) {
      newErrors.name = 'Name is required';
    }
    
    if (!formData.email.trim()) {
      newErrors.email = 'Email is required';
    } else if (!/\S+@\S+\.\S+/.test(formData.email)) {
      newErrors.email = 'Email is invalid';
    }
    
    if (!formData.message.trim()) {
      newErrors.message = 'Message is required';
    }
    
    setErrors(newErrors);
    return Object.keys(newErrors).length === 0;
  };
  
  const handleSubmit = (e) => {
    e.preventDefault();
    
    if (validate()) {
      // Submit form data
      console.log('Form submitted:', formData);
      // Reset form
      setFormData({ name: '', email: '', message: '' });
    }
  };
  
  return (
    <form onSubmit={handleSubmit} className="contact-form">
      <div className="form-group">
        <label htmlFor="name">Name</label>
        <input
          type="text"
          id="name"
          name="name"
          value={formData.name}
          onChange={handleChange}
          className={errors.name ? 'error' : ''}
        />
        {errors.name && <p className="error-text">{errors.name}</p>}
      </div>
      
      <div className="form-group">
        <label htmlFor="email">Email</label>
        <input
          type="email"
          id="email"
          name="email"
          value={formData.email}
          onChange={handleChange}
          className={errors.email ? 'error' : ''}
        />
        {errors.email && <p className="error-text">{errors.email}</p>}
      </div>
      
      <div className="form-group">
        <label htmlFor="message">Message</label>
        <textarea
          id="message"
          name="message"
          value={formData.message}
          onChange={handleChange}
          className={errors.message ? 'error' : ''}
        />
        {errors.message && <p className="error-text">{errors.message}</p>}
      </div>
      
      <button type="submit" className="submit-btn">Send Message</button>
    </form>
  );
}
```

#### Topik 3.6: Styling di React
**Durasi**: 1 hari  
**Materi**:
- Inline styles
- CSS classes
- CSS Modules
- Styled Components
- CSS-in-JS libraries
- Tailwind CSS dengan React

**Hands-on Practice**:
```jsx
// CSS Modules example
import styles from './Button.module.css';

function Button({ variant = 'primary', children, ...props }) {
  return (
    <button
      className={`${styles.button} ${styles[variant]}`}
      {...props}
    >
      {children}
    </button>
  );
}

// Styled Components example
import styled from 'styled-components';

const StyledButton = styled.button`
  padding: 8px 16px;
  border-radius: 4px;
  font-weight: 600;
  cursor: pointer;
  
  ${props => props.variant === 'primary' && `
    background-color: #0070f3;
    color: white;
    border: none;
  `}
  
  ${props => props.variant === 'outline' && `
    background-color: transparent;
    color: #0070f3;
    border: 1px solid #0070f3;
  `}
`;

function Button({ variant = 'primary', children, ...props }) {
  return (
    <StyledButton variant={variant} {...props}>
      {children}
    </StyledButton>
  );
}
```

**Project Modul 3**:  
Membuat To-Do List Application:
- Fitur CRUD (Create, Read, Update, Delete)
- Form validasi untuk input task
- Filtering dan sorting tasks
- Persistent storage dengan localStorage
- Responsive design dengan multiple layout options
- Drag and drop untuk reordering tasks

### MODUL 4: REACT ECOSYSTEM & ROUTING

#### Topik 4.1: Introduction to React Router
**Durasi**: 1 hari  
**Materi**:
- React Router concepts
- BrowserRouter vs HashRouter
- Basic routing dengan Route
- Navigation dengan Link dan NavLink
- History API integration

**Hands-on Practice**:
```jsx
import { BrowserRouter, Routes, Route, Link, NavLink } from 'react-router-dom';

function App() {
  return (
    <BrowserRouter>
      <nav>
        <NavLink to="/" end className={({ isActive }) => 
          isActive ? 'active-link' : 'link'
        }>
          Home
        </NavLink>
        <NavLink to="/about" className={({ isActive }) => 
          isActive ? 'active-link' : 'link'
        }>
          About
        </NavLink>
        <NavLink to="/contact" className={({ isActive }) => 
          isActive ? 'active-link' : 'link'
        }>
          Contact
        </NavLink>
      </nav>
      
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
        <Route path="*" element={<NotFound />} />
      </Routes>
    </BrowserRouter>
  );
}
```

#### Topik 4.2: Advanced Routing
**Durasi**: 2 hari  
**Materi**:
- URL parameters
- Query parameters
- Nested routes
- Index routes
- Layout routes
- Outlet component

**Hands-on Practice**:
```jsx
function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<MainLayout />}>
          <Route index element={<Home />} />
          <Route path="about" element={<About />} />
          <Route path="products" element={<ProductsLayout />}>
            <Route index element={<ProductsList />} />
            <Route path=":productId" element={<ProductDetail />} />
          </Route>
          <Route path="contact" element={<Contact />} />
          <Route path="*" element={<NotFound />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}

function MainLayout() {
  return (
    <div className="main-layout">
      <header>
        <nav>
          <NavLink to="/">Home</NavLink>
          <NavLink to="/about">About</NavLink>
          <NavLink to="/products">Products</NavLink>
          <NavLink to="/contact">Contact</NavLink>
        </nav>
      </header>
      
      <main>
        <Outlet /> {/* Child routes render here */}
      </main>
      
      <footer>© 2025 My Company</footer>
    </div>
  );
}

function ProductsLayout() {
  return (
    <div className="products-layout">
      <h1>Products</h1>
      <Outlet /> {/* Nested product routes render here */}
    </div>
  );
}

function ProductDetail() {
  const { productId } = useParams();
  const [product, setProduct] = useState(null);
  const [loading, setLoading] = useState(true);
  
  useEffect(() => {
    // Fetch product data based on productId
    fetchProduct(productId).then(data => {
      setProduct(data);
      setLoading(false);
    });
  }, [productId]);
  
  if (loading) return <p>Loading...</p>;
  if (!product) return <p>Product not found</p>;
  
  return (
    <div className="product-detail">
      <h2>{product.name}</h2>
      <p>{product.description}</p>
      <p className="price">${product.price}</p>
    </div>
  );
}
```

#### Topik 4.3: Protected Routes & Authentication
**Durasi**: 1 hari  
**Materi**:
- Authentication flow di React
- Private routes
- Redirect non-authenticated users
- Persisting authentication state
- Role-based authorization

**Hands-on Practice**:
```jsx
const AuthContext = createContext(null);

function AuthProvider({ children }) {
  const [user, setUser] = useState(null);
  
  // Check for saved auth on initial load
  useEffect(() => {
    const savedUser = localStorage.getItem('user');
    if (savedUser) {
      setUser(JSON.parse(savedUser));
    }
  }, []);
  
  const login = async (credentials) => {
    // Call to auth API
    const response = await authService.login(credentials);
    const userData = response.data;
    
    // Save user in state and localStorage
    setUser(userData);
    localStorage.setItem('user', JSON.stringify(userData));
    return userData;
  };
  
  const logout = () => {
    setUser(null);
    localStorage.removeItem('user');
  };
  
  const value = {
    user,
    isAuthenticated: !!user,
    login,
    logout
  };
  
  return (
    <AuthContext.Provider value={value}>
      {children}
    </AuthContext.Provider>
  );
}

function useAuth() {
  return useContext(AuthContext);
}

function ProtectedRoute({ children }) {
  const { isAuthenticated } = useAuth();
  const location = useLocation();
  
  if (!isAuthenticated) {
    return <Navigate to="/login" state={{ from: location }} replace />;
  }
  
  return children;
}

function App() {
  return (
    <AuthProvider>
      <BrowserRouter>
        <Routes>
          <Route path="/" element={<MainLayout />}>
            <Route index element={<Home />} />
            <Route path="login" element={<Login />} />
            <Route path="dashboard" element={
              <ProtectedRoute>
                <Dashboard />
              </ProtectedRoute>
            } />
            <Route path="profile" element={
              <ProtectedRoute>
                <Profile />
              </ProtectedRoute>
            } />
          </Route>
        </Routes>
      </BrowserRouter>
    </AuthProvider>
  );
}
```

#### Topik 4.4: Code Splitting & Lazy Loading
**Durasi**: 1 hari  
**Materi**:
- Bundling concepts
- React.lazy
- Suspense component
- Route-based code splitting
- Preloading chunks
- Error boundaries

**Hands-on Practice**:
```jsx
import React, { Suspense, lazy } from 'react';
import { BrowserRouter, Routes, Route } from 'react-router-dom';
import LoadingFallback from './LoadingFallback';
import ErrorBoundary from './ErrorBoundary';

// Lazy load components
const Home = lazy(() => import('./pages/Home'));
const About = lazy(() => import('./pages/About'));
const Products = lazy(() => import('./pages/Products'));
const ProductDetail = lazy(() => import('./pages/ProductDetail'));
const Contact = lazy(() => import('./pages/Contact'));
const NotFound = lazy(() => import('./pages/NotFound'));

function App() {
  return (
    <BrowserRouter>
      <ErrorBoundary>
        <Suspense fallback={<LoadingFallback />}>
          <Routes>
            <Route path="/" element={<MainLayout />}>
              <Route index element={<Home />} />
              <Route path="about" element={<About />} />
              <Route path="products" element={<Products />} />
              <Route path="products/:id" element={<ProductDetail />} />
              <Route path="contact" element={<Contact />} />
              <Route path="*" element={<NotFound />} />
            </Route>
          </Routes>
        </Suspense>
      </ErrorBoundary>
    </BrowserRouter>
  );
}
```

**Project Modul 4**:  
Membuat Multi-page Application dengan React Router:
- Implementasi routing untuk multiple pages
- Login/registration pages dengan authentication
- Dashboard dengan protected routes
- Dynamic routes dengan parameter
- Lazy loading untuk semua pages
- Custom 404 page
- Breadcrumb navigation

### MODUL 5: STATE MANAGEMENT

#### Topik 5.1: React Context API
**Durasi**: 2 hari  
**Materi**:
- Context API basics
- createContext dan useContext
- Context Provider pattern
- Multiple contexts
- Context vs prop drilling
- Performance considerations

**Hands-on Practice**:
```jsx
// ThemeContext.js
import { createContext, useContext, useState } from 'react';

const ThemeContext = createContext();

export function ThemeProvider({ children }) {
  const [theme, setTheme] = useState('light');
  
  const toggleTheme = () => {
    setTheme(prevTheme => prevTheme === 'light' ? 'dark' : 'light');
  };
  
  const value = {
    theme,
    toggleTheme
  };
  
  return (
    <ThemeContext.Provider value={value}>
      {children}
    </ThemeContext.Provider>
  );
}

export function useTheme() {
  const context = useContext(ThemeContext);
  if (context === undefined) {
    throw new Error('useTheme must be used within a ThemeProvider');
  }
  return context;
}

// App.js
function App() {
  return (
    <ThemeProvider>
      <MainApp />
    </ThemeProvider>
  );
}

// ThemedButton.js
function ThemedButton({ children, ...props }) {
  const { theme, toggleTheme } = useTheme();
  
  return (
    <button
      className={`btn btn-${theme}`}
      onClick={toggleTheme}
      {...props}
    >
      {children}
    </button>
  );
}
```

#### Topik 5.2: Introduction to Redux
**Durasi**: 2 hari  
**Materi**:
- Redux principles
- Actions, reducers, dan store
- connect HOC
- mapStateToProps dan mapDispatchToProps
- Redux DevTools
- Redux middleware

**Hands-on Practice**:
```jsx
// actions.js
export const ADD_TODO = 'ADD_TODO';
export const TOGGLE_TODO = 'TOGGLE_TODO';
export const REMOVE_TODO = 'REMOVE_TODO';

export const addTodo = (text) => ({
  type: ADD_TODO,
  payload: {
    id: Date.now(),
    text,
    completed: false
  }
});

export const toggleTodo = (id) => ({
  type: TOGGLE_TODO,
  payload: { id }
});

export const removeTodo = (id) => ({
  type: REMOVE_TODO,
  payload: { id }
});

// reducers.js
const initialState = {
  todos: []
};

export function todoReducer(state = initialState, action) {
  switch (action.type) {
    case ADD_TODO:
      return {
        ...state,
        todos: [...state.todos, action.payload]
      };
      
    case TOGGLE_TODO:
      return {
        ...state,
        todos: state.todos.map(todo =>
          todo.id === action.payload.id
            ? { ...todo, completed: !todo.completed }
            : todo
        )
      };
      
    case REMOVE_TODO:
      return {
        ...state,
        todos: state.todos.filter(todo => todo.id !== action.payload.id)
      };
      
    default:
      return state;
  }
}

// store.js
import { createStore } from 'redux';
import { todoReducer } from './reducers';

const store = createStore(
  todoReducer,
  window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__()
);

export default store;

// TodoList.js (with connect)
import { connect } from 'react-redux';
import { toggleTodo, removeTodo } from './actions';

function TodoList({ todos, toggleTodo, removeTodo }) {
  return (
    <ul className="todo-list">
      {todos.map(todo => (
        <li key={todo.id} className={todo.completed ? 'completed' : ''}>
          <input
            type="checkbox"
            checked={todo.completed}
            onChange={() => toggleTodo(todo.id)}
          />
          <span>{todo.text}</span>
          <button onClick={() => removeTodo(todo.id)}>Delete</button>
        </li>
      ))}
    </ul>
  );
}

const mapStateToProps = (state) => ({
  todos: state.todos
});

const mapDispatchToProps = {
  toggleTodo,
  removeTodo
};

export default connect(mapStateToProps, mapDispatchToProps)(TodoList);
```

#### Topik 5.3: Modern Redux dengan Hooks
**Durasi**: 2 hari  
**Materi**:
- useSelector dan useDispatch
- Redux hooks vs connect
- Selecting data efficiently
- Memoization dan performance
- Redux best practices

**Hands-on Practice**:
```jsx
// TodoList.js (with hooks)
import { useSelector, useDispatch } from 'react-redux';
import { toggleTodo, removeTodo } from './actions';

function TodoList() {
  const todos = useSelector(state => state.todos);
  const dispatch = useDispatch();
  
  return (
    <ul className="todo-list">
      {todos.map(todo => (
        <li key={todo.id} className={todo.completed ? 'completed' : ''}>
          <input
            type="checkbox"
            checked={todo.completed}
            onChange={() => dispatch(toggleTodo(todo.id))}
          />
          <span>{todo.text}</span>
          <button onClick={() => dispatch(removeTodo(todo.id))}>
            Delete
          </button>
        </li>
      ))}
    </ul>
  );
}

// AddTodo.js
function AddTodo() {
  const [text, setText] = useState('');
  const dispatch = useDispatch();
  
  const handleSubmit = (e) => {
    e.preventDefault();
    if (!text.trim()) return;
    
    dispatch(addTodo(text));
    setText('');
  };
  
  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        value={text}
        onChange={(e) => setText(e.target.value)}
        placeholder="Add new todo"
      />
      <button type="submit">Add</button>
    </form>
  );
}
```

#### Topik 5.4: Redux Toolkit
**Durasi**: 2 hari  
**Materi**:
- configureStore
- createSlice
- createAsyncThunk
- Redux DevTools integration
- Immutability dengan Immer
- createEntityAdapter

**Hands-on Practice**:
```jsx
// todosSlice.js
import { createSlice, createAsyncThunk } from '@reduxjs/toolkit';
import todoApi from '../api/todoApi';

export const fetchTodos = createAsyncThunk(
  'todos/fetchTodos',
  async () => {
    const response = await todoApi.getTodos();
    return response.data;
  }
);

export const addNewTodo = createAsyncThunk(
  'todos/addNewTodo',
  async (text) => {
    const response = await todoApi.addTodo({ text, completed: false });
    return response.data;
  }
);

const todosSlice = createSlice({
  name: 'todos',
  initialState: {
    items: [],
    status: 'idle', // 'idle' | 'loading' | 'succeeded' | 'failed'
    error: null
  },
  reducers: {
    // Immer lets us write "mutating" logic
    toggleTodo: (state, action) => {
      const todo = state.items.find(todo => todo.id === action.payload);
      if (todo) {
        todo.completed = !todo.completed;
      }
    },
    removeTodo: (state, action) => {
      state.items = state.items.filter(todo => todo.id !== action.payload);
    }
  },
  extraReducers: (builder) => {
    builder
      .addCase(fetchTodos.pending, (state) => {
        state.status = 'loading';
      })
      .addCase(fetchTodos.fulfilled, (state, action) => {
        state.status = 'succeeded';
        state.items = action.payload;
      })
      .addCase(fetchTodos.rejected, (state, action) => {
        state.status = 'failed';
        state.error = action.error.message;
      })
      .addCase(addNewTodo.fulfilled, (state, action) => {
        state.items.push(action.payload);
      });
  }
});

export const { toggleTodo, removeTodo } = todosSlice.actions;
export default todosSlice.reducer;

// store.js
import { configureStore } from '@reduxjs/toolkit';
import todosReducer from './todosSlice';

export const store = configureStore({
  reducer: {
    todos: todosReducer
  }
});

// TodoList.js
function TodoList() {
  const dispatch = useDispatch();
  const { items, status, error } = useSelector(state => state.todos);
  
  useEffect(() => {
    if (status === 'idle') {
      dispatch(fetchTodos());
    }
  }, [status, dispatch]);
  
  if (status === 'loading') {
    return <div>Loading...</div>;
  }
  
  if (status === 'failed') {
    return <div>Error: {error}</div>;
  }
  
  return (
    <ul className="todo-list">
      {items.map(todo => (
        <li key={todo.id} className={todo.completed ? 'completed' : ''}>
          <input
            type="checkbox"
            checked={todo.completed}
            onChange={() => dispatch(toggleTodo(todo.id))}
          />
          <span>{todo.text}</span>
          <button onClick={() => dispatch(removeTodo(todo.id))}>
            Delete
          </button>
        </li>
      ))}
    </ul>
  );
}
```

#### Topik 5.5: Asynchronous Redux
**Durasi**: 2 hari  
**Materi**:
- Redux middleware concepts
- Thunks vs Sagas
- Redux Thunk middleware
- Error handling in async actions
- Loading states
- Optimistic updates

**Hands-on Practice**:
```jsx
// With Redux Thunk (without toolkit)
export const fetchTodos = () => async (dispatch) => {
  dispatch({ type: 'FETCH_TODOS_START' });
  
  try {
    const response = await fetch('/api/todos');
    const data = await response.json();
    
    dispatch({
      type: 'FETCH_TODOS_SUCCESS',
      payload: data
    });
  } catch (error) {
    dispatch({
      type: 'FETCH_TODOS_FAILURE',
      payload: error.message
    });
  }
};

// Optimistic update example
export const toggleTodoOptimistic = (id) => async (dispatch, getState) => {
  const todo = getState().todos.items.find(todo => todo.id === id);
  
  // Optimistically update UI
  dispatch({
    type: 'TOGGLE_TODO',
    payload: { id }
  });
  
  try {
    // API call to persist the change
    await fetch(`/api/todos/${id}`, {
      method: 'PATCH',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ completed: !todo.completed })
    });
  } catch (error) {
    // Revert on failure
    dispatch({
      type: 'TOGGLE_TODO',
      payload: { id }
    });
    
    dispatch({
      type: 'API_ERROR',
      payload: error.message
    });
  }
};
```

**Project Modul 5**:  
Membuat E-Commerce App dengan state management kompleks:
- Cart functionality dengan Redux
- Product listing dengan filtering dan sorting
- User authentication state management
- Wishlists dan saved items
- Order processing flow
- Product reviews dan ratings

### MODUL 6: DATA FETCHING & API INTEGRATION

#### Topik 6.1: Fetching Data in React
**Durasi**: 1 hari  
**Materi**:
- Fetch API
- Axios library
- Error handling
- Loading states
- AbortController untuk cancellation
- Handling race conditions

**Hands-on Practice**:
```jsx
function UserProfile({ userId }) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);
  
  useEffect(() => {
    let isMounted = true;
    const controller = new AbortController();
    const signal = controller.signal;
    
    async function fetchData() {
      setLoading(true);
      
      try {
        const response = await fetch(`/api/users/${userId}`, { signal });
        
        if (!response.ok) {
          throw new Error(`HTTP error! status: ${response.status}`);
        }
        
        const result = await response.json();
        
        if (isMounted) {
          setData(result);
          setError(null);
        }
      } catch (error) {
        if (error.name !== 'AbortError' && isMounted) {
          setError(error.message);
          setData(null);
        }
      } finally {
        if (isMounted) {
          setLoading(false);
        }
      }
    }
    
    fetchData();
    
    // Cleanup function
    return () => {
      isMounted = false;
      controller.abort();
    };
  }, [userId]);
  
  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error}</p>;
  if (!data) return null;
  
  return (
    <div>
      <h1>{data.name}</h1>
      <p>Email: {data.email}</p>
      {/* Other user info */}
    </div>
  );
}
```

#### Topik 6.2: Custom Hooks untuk Data Fetching
**Durasi**: 2 hari  
**Materi**:
- Creating reusable fetch hooks
- Separation of concerns
- Parameterized fetch hooks
- Caching results
- Polling dan refresh strategies
- Sequential vs parallel data fetching

**Hands-on Practice**:
```jsx
// useFetch.js - Basic fetch hook
function useFetch(url) {
  const [data, setData] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);
  
  useEffect(() => {
    let isMounted = true;
    const controller = new AbortController();
    
    async function fetchData() {
      setLoading(true);
      
      try {
        const response = await fetch(url, { signal: controller.signal });
        
        if (!response.ok) {
          throw new Error(`HTTP error! status: ${response.status}`);
        }
        
        const result = await response.json();
        
        if (isMounted) {
          setData(result);
          setError(null);
        }
      } catch (error) {
        if (error.name !== 'AbortError' && isMounted) {
          setError(error.message);
        }
      } finally {
        if (isMounted) {
          setLoading(false);
        }
      }
    }
    
    fetchData();
    
    return () => {
      isMounted = false;
      controller.abort();
    };
  }, [url]);
  
  return { data, loading, error };
}

// useResource.js - More advanced hook
function useResource(resourceType, id) {
  const [resource, setResource] = useState(null);
  const [loading, setLoading] = useState(true);
  const [error, setError] = useState(null);
  
  useEffect(() => {
    let isMounted = true;
    const controller = new AbortController();
    
    async function fetchResource() {
      if (!id) return;
      
      setLoading(true);
      
      try {
        const response = await fetch(`/api/${resourceType}/${id}`, {
          signal: controller.signal
        });
        
        if (!response.ok) {
          throw new Error(`HTTP error! status: ${response.status}`);
        }
        
        const data = await response.json();
        
        if (isMounted) {
          setResource(data);
          setError(null);
        }
      } catch (error) {
        if (error.name !== 'AbortError' && isMounted) {
          setError(error.message);
          setResource(null);
        }
      } finally {
        if (isMounted) {
          setLoading(false);
        }
      }
    }
    
    fetchResource();
    
    return () => {
      isMounted = false;
      controller.abort();
    };
  }, [resourceType, id]);
  
  return {
    data: resource,
    loading,
    error,
    refetch: () => {
      setLoading(true);
      // Re-run the effect by updating a ref
    }
  };
}

// Usage
function UserProfile({ userId }) {
  const { data: user, loading, error } = useResource('users', userId);
  
  // Dependent query - fetch user's posts once we have the user
  const { data: posts } = useResource('posts', user ? user.id : null);
  
  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error}</p>;
  if (!user) return null;
  
  return (
    <div>
      <h1>{user.name}</h1>
      <p>Email: {user.email}</p>
      
      <h2>Posts</h2>
      {posts ? (
        <ul>
          {posts.map(post => (
            <li key={post.id}>{post.title}</li>
          ))}
        </ul>
      ) : (
        <p>Loading posts...</p>
      )}
    </div>
  );
}
```

#### Topik 6.3: React Query
**Durasi**: 2 hari  
**Materi**:
- React Query basics
- Queries vs Mutations
- Caching dan stale data
- Refetching strategies
- Pagination dan infinite scroll
- Optimistic updates
- Dependent queries

**Hands-on Practice**:
```jsx
// React Query setup
import {
  QueryClient,
  QueryClientProvider,
  useQuery,
  useMutation,
  useQueryClient
} from 'react-query';

const queryClient = new QueryClient({
  defaultOptions: {
    queries: {
      staleTime: 1000 * 60 * 5, // 5 minutes
      cacheTime: 1000 * 60 * 30, // 30 minutes
      retry: 2,
      refetchOnWindowFocus: true
    }
  }
});

function App() {
  return (
    <QueryClientProvider client={queryClient}>
      <TodoApp />
    </QueryClientProvider>
  );
}

// API functions
const fetchTodos = async () => {
  const response = await fetch('/api/todos');
  if (!response.ok) {
    throw new Error('Network response was not ok');
  }
  return response.json();
};

const addTodo = async (newTodo) => {
  const response = await fetch('/api/todos', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(newTodo)
  });
  if (!response.ok) {
    throw new Error('Failed to add todo');
  }
  return response.json();
};

const updateTodo = async (todo) => {
  const response = await fetch(`/api/todos/${todo.id}`, {
    method: 'PUT',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(todo)
  });
  if (!response.ok) {
    throw new Error('Failed to update todo');
  }
  return response.json();
};

// Components
function TodoApp() {
  const queryClient = useQueryClient();
  
  // Query - fetching data
  const {
    data: todos,
    isLoading,
    isError,
    error,
    refetch
  } = useQuery('todos', fetchTodos);
  
  // Mutation - adding a todo
  const addMutation = useMutation(addTodo, {
    // When mutate is called:
    onMutate: async (newTodo) => {
      // Cancel any outgoing refetches
      await queryClient.cancelQueries('todos');
      
      // Snapshot the previous value
      const previousTodos = queryClient.getQueryData('todos');
      
      // Optimistically update to the new value
      queryClient.setQueryData('todos', old => [
        ...old,
        { id: Date.now(), ...newTodo }
      ]);
      
      // Return context with the snapshotted value
      return { previousTodos };
    },
    // If the mutation fails, use the context returned from onMutate to roll back
    onError: (err, newTodo, context) => {
      queryClient.setQueryData('todos', context.previousTodos);
    },
    // Always refetch after error or success:
    onSettled: () => {
      queryClient.invalidateQueries('todos');
    },
  });
  
  // Mutation - toggling a todo
  const updateMutation = useMutation(updateTodo, {
    onMutate: async (updatedTodo) => {
      await queryClient.cancelQueries('todos');
      const previousTodos = queryClient.getQueryData('todos');
      
      queryClient.setQueryData('todos', old =>
        old.map(todo =>
          todo.id === updatedTodo.id ? updatedTodo : todo
        )
      );
      
      return { previousTodos };
    },
    onError: (err, updatedTodo, context) => {
      queryClient.setQueryData('todos', context.previousTodos);
    },
    onSettled: () => {
      queryClient.invalidateQueries('todos');
    },
  });
  
  const handleAddTodo = (text) => {
    addMutation.mutate({ text, completed: false });
  };
  
  const handleToggle = (todo) => {
    updateMutation.mutate({
      ...todo,
      completed: !todo.completed
    });
  };
  
  if (isLoading) return <p>Loading...</p>;
  if (isError) return <p>Error: {error.message}</p>;
  
  return (
    <div>
      <button onClick={() => refetch()}>Refresh</button>
      
      <AddTodoForm onAdd={handleAddTodo} />
      
      <ul>
        {todos.map(todo => (
          <li
            key={todo.id}
            style={{ textDecoration: todo.completed ? 'line-through' : 'none' }}
            onClick={() => handleToggle(todo)}
          >
            {todo.text}
          </li>
        ))}
      </ul>
    </div>
  );
}
```

#### Topik 6.4: Authentication
**Durasi**: 2 hari  
**Materi**:
- JWT Authentication
- OAuth flows
- Authentication state management
- Protected routes
- Refresh tokens
- Persistent login
- Security considerations

**Hands-on Practice**:
```jsx
import { createContext, useContext, useState, useEffect } from 'react';

// Create auth context
const AuthContext = createContext(null);

export function AuthProvider({ children }) {
  const [user, setUser] = useState(null);
  const [loading, setLoading] = useState(true);
  
  // Check if user is already logged in
  useEffect(() => {
    async function loadUserFromToken() {
      const token = localStorage.getItem('token');
      
      if (!token) {
        setLoading(false);
        return;
      }
      
      try {
        // Validate token and get user info
        const response = await fetch('/api/auth/me', {
          headers: {
            'Authorization': `Bearer ${token}`
          }
        });
        
        if (!response.ok) {
          throw new Error('Invalid token');
        }
        
        const userData = await response.json();
        setUser(userData);
      } catch (error) {
        console.error('Failed to load user', error);
        localStorage.removeItem('token');
      } finally {
        setLoading(false);
      }
    }
    
    loadUserFromToken();
  }, []);
  
  // Login function
  const login = async (credentials) => {
    const response = await fetch('/api/auth/login', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(credentials)
    });
    
    if (!response.ok) {
      throw new Error('Login failed');
    }
    
    const { token, user: userData } = await response.json();
    
    // Store token in localStorage
    localStorage.setItem('token', token);
    
    // Set user state
    setUser(userData);
    
    return userData;
  };
  
  // Logout function
  const logout = () => {
    localStorage.removeItem('token');
    setUser(null);
  };
  
  // Registration function
  const register = async (userData) => {
    const response = await fetch('/api/auth/register', {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json'
      },
      body: JSON.stringify(userData)
    });
    
    if (!response.ok) {
      const error = await response.json();
      throw new Error(error.message || 'Registration failed');
    }
    
    const { token, user: newUser } = await response.json();
    
    localStorage.setItem('token', token);
    setUser(newUser);
    
    return newUser;
  };
  
  const value = {
    user,
    loading,
    login,
    logout,
    register,
    isAuthenticated: !!user
  };
  
  return (
    <AuthContext.Provider value={value}>
      {children}
    </AuthContext.Provider>
  );
}

// Custom hook to use the auth context
export function useAuth() {
  const context = useContext(AuthContext);
  if (context === undefined) {
    throw new Error('useAuth must be used within an AuthProvider');
  }
  return context;
}

// Login form component
function LoginForm() {
  const { login } = useAuth();
  const [credentials, setCredentials] = useState({
    email: '',
    password: ''
  });
  const [error, setError] = useState('');
  const [loading, setLoading] = useState(false);
  const navigate = useNavigate();
  
  const handleChange = (e) => {
    const { name, value } = e.target;
    setCredentials(prev => ({
      ...prev,
      [name]: value
    }));
  };
  
  const handleSubmit = async (e) => {
    e.preventDefault();
    setError('');
    setLoading(true);
    
    try {
      await login(credentials);
      navigate('/dashboard');
    } catch (error) {
      setError(error.message);
    } finally {
      setLoading(false);
    }
  };
  
  return (
    <form onSubmit={handleSubmit}>
      {error && <p className="error">{error}</p>}
      
      <div>
        <label htmlFor="email">Email</label>
        <input
          type="email"
          id="email"
          name="email"
          value={credentials.email}
          onChange={handleChange}
          required
        />
      </div>
      
      <div>
        <label htmlFor="password">Password</label>
        <input
          type="password"
          id="password"
          name="password"
          value={credentials.password}
          onChange={handleChange}
          required
        />
      </div>
      
      <button type="submit" disabled={loading}>
        {loading ? 'Logging in...' : 'Log In'}
      </button>
    </form>
  );
}
```

**Project Modul 6**:  
Membuat Dashboard App dengan integrasi API:
- Authentication dengan JWT
- Admin dashboard dengan CRUD operations
- Data visualization dengan real-time updates
- Search dan filtering dengan API parameters
- Pagination dan infinite scroll
- Optimistic UI updates
- Error handling dan retry mechanisms

### MODUL 7: ADVANCED HOOKS & PATTERNS

#### Topik 7.1: Advanced Hooks
**Durasi**: 1 hari  
**Materi**:
- useCallback
- useMemo
- useRef
- useLayoutEffect
- useReducer vs useState
- useImperativeHandle
- useDebugValue

**Hands-on Practice**:
```jsx
// useCallback example
function SearchResults({ query, onResultClick }) {
  const [results, setResults] = useState([]);
  
  // Prevent recreation of function on each render
  const handleResultClick = useCallback((id) => {
    console.log(`Result ${id} clicked`);
    onResultClick(id);
  }, [onResultClick]);
  
  // Memoize expensive calculation
  const sortedResults = useMemo(() => {
    console.log('Sorting results');
    return [...results].sort((a, b) => a.name.localeCompare(b.name));
  }, [results]);
  
  // useRef for previous value comparison
  const prevQuery = useRef(query);
  
  useEffect(() => {
    if (prevQuery.current !== query) {
      console.log(`Query changed from ${prevQuery.current} to ${query}`);
      prevQuery.current = query;
    }
  }, [query]);
  
  // useReducer for complex state
  const [state, dispatch] = useReducer((state, action) => {
    switch (action.type) {
      case 'FETCH_START':
        return { ...state, loading: true, error: null };
      case 'FETCH_SUCCESS':
        return { ...state, loading: false, data: action.payload };
      case 'FETCH_ERROR':
        return { ...state, loading: false, error: action.payload };
      default:
        return state;
    }
  }, {
    loading: false,
    data: null,
    error: null
  });
  
  // Component logic
  
  return (
    <div>
      {sortedResults.map(result => (
        <ResultItem
          key={result.id}
          result={result}
          onClick={() => handleResultClick(result.id)}
        />
      ))}
    </div>
  );
}

// useImperativeHandle example
const FancyInput = forwardRef((props, ref) => {
  const inputRef = useRef();
  
  useImperativeHandle(ref, () => ({
    focus: () => {
      inputRef.current.focus();
    },
    clear: () => {
      inputRef.current.value = '';
    },
    getValue: () => {
      return inputRef.current.value;
    }
  }), []);
  
  return <input ref={inputRef} {...props} />;
});

// Using the imperative handle
function Form() {
  const inputRef = useRef();
  
  const handleSubmit = (e) => {
    e.preventDefault();
    const value = inputRef.current.getValue();
    console.log('Input value:', value);
    
    // Clear the input
    inputRef.current.clear();
  };
  
  return (
    <form onSubmit={handleSubmit}>
      <FancyInput ref={inputRef} placeholder="Enter text" />
      <button type="button" onClick={() => inputRef.current.focus()}>
        Focus Input
      </button>
      <button type="submit">Submit</button>
    </form>
  );
}
