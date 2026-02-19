# FS-prac

## 📌 Table of Contents
1. [HR / Introduction Questions](#1-hr--introduction-questions)
2. [HTML, CSS & Responsive Design](#2-html-css--responsive-design)
3. [JavaScript (ES6+)](#3-javascript-es6)
4. [React.js](#4-reactjs)
5. [Node.js & Express.js](#5-nodejs--expressjs)
6. [Databases – MySQL & MongoDB](#6-databases--mysql--mongodb)
7. [REST APIs & Authentication](#7-rest-apis--authentication)
8. [DevOps, Docker & CI/CD](#8-devops-docker--cicd)
9. [Cloud – AWS](#9-cloud--aws)
10. [Version Control – Git & GitHub](#10-version-control--git--github)
11. [CRM & Third-Party API Integration](#11-crm--third-party-api-integration)
12. [Security Best Practices](#12-security-best-practices)
13. [Project-Based Questions (From Your Resume)](#13-project-based-questions-from-your-resume)
14. [System Design & Architecture](#14-system-design--architecture)
15. [Problem Solving & Data Structures](#15-problem-solving--data-structures)
16. [Soft Skills & Situational Questions](#16-soft-skills--situational-questions)
17. [Company & Role Specific Questions](#17-company--role-specific-questions)

---

## 1. HR / Introduction Questions

---

**Q1. Tell me about yourself.**

> **Answer:** My name is Kalai Muthu. I'm a final-year B.Tech CSE student at SRM Institute of Science and Technology with a CGPA of 8.45. I have hands-on experience in full stack web development, mobile development, and AI/automation. I recently completed an internship at Hogist Technologies where I built an AI-powered Voice Sales Automation Agent and a Social Media Automation platform. I'm proficient in React, Node.js, Express, MySQL, MongoDB, and AWS. I'm passionate about building scalable, impactful products and excited about this role at FRL because it aligns perfectly with my skillset.

---

**Q2. Why do you want to join Food Research Lab specifically?**

> **Answer:** FRL operates at an interesting intersection of food science and technology. Building a web portal for recipe databases, CRM integrations, and analytics dashboards is exactly the kind of product engineering challenge I enjoy. The company is globally oriented with complex, real-world requirements — that's a great environment for growth. I also appreciate that this role involves end-to-end ownership from frontend UI to backend architecture.

---

**Q3. Where do you see yourself in 3 years?**

> **Answer:** In 3 years, I see myself as a well-rounded full stack engineer with strong system design skills. I'd like to take ownership of larger modules or products, possibly leading a small team. I also want to deepen my knowledge in cloud architecture and scalable backend systems.

---

**Q4. What are your strengths and weaknesses?**

> **Strengths:** Problem-solving, quick learning, and ownership. At Hogist, I independently built complex AI pipelines and full-stack platforms without much hand-holding.
>
> **Weakness:** I tend to over-engineer solutions sometimes — I'm working on finding the right balance between perfection and shipping fast.

---

**Q5. Are you comfortable with the Monday–Saturday, 10 AM–7 PM WFO schedule?**

> **Answer:** Yes, absolutely. I understand that a fast-paced startup environment requires full commitment. I'm ready to work from office and adapt to the team's schedule.

---

## 2. HTML, CSS & Responsive Design

---

**Q6. What is the difference between `em`, `rem`, `px`, `%`, and `vw/vh` units in CSS?**

> **Answer:**
> - `px` – Absolute pixel unit. Fixed size regardless of screen.
> - `em` – Relative to the font-size of the **parent** element.
> - `rem` – Relative to the font-size of the **root** (`<html>`) element. Preferred for scalable designs.
> - `%` – Relative to the **parent container's** dimension.
> - `vw/vh` – Relative to **viewport width/height**. Useful for full-screen layouts.
>
> For responsive design, `rem`, `%`, and `vw/vh` are preferred over `px`.

---

**Q7. How does the CSS Box Model work?**

> **Answer:** Every HTML element is a box with four layers:
> 1. **Content** – the actual text/image area.
> 2. **Padding** – space between content and border (inside the border).
> 3. **Border** – surrounds the padding.
> 4. **Margin** – space outside the border, separating it from other elements.
>
> `box-sizing: border-box` makes padding and border included in the element's total width/height, which is the modern standard.

---

**Q8. What is Flexbox, and when would you use CSS Grid instead?**

> **Answer:** 
> - **Flexbox** is a one-dimensional layout system (either row or column). Best for navbars, card rows, centering elements.
> - **CSS Grid** is two-dimensional (rows AND columns). Best for full page layouts, dashboards, complex grids.
>
> Rule of thumb: Use Flexbox for components, Grid for page layout.

---

**Q9. How do you make a website responsive? What is mobile-first design?**

> **Answer:** Responsive design is achieved through:
> - Media queries (`@media screen and (max-width: 768px)`)
> - Fluid layouts using `%` or `vw`
> - Flexible images (`max-width: 100%`)
> - CSS Grid/Flexbox
> - Tailwind CSS utility classes (which you've used)
>
> **Mobile-first** means you write CSS for small screens first, then add `min-width` media queries to enhance for larger screens. It's better for performance and progressive enhancement.

---

**Q10. What are semantic HTML elements, and why do they matter?**

> **Answer:** Semantic elements clearly describe their purpose: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<aside>`. They matter because:
> - Improve **SEO** – search engines understand content structure.
> - Improve **accessibility** – screen readers navigate using semantic tags.
> - Improve **code readability** for developers.

---

**Q11. What is the difference between `display: none`, `visibility: hidden`, and `opacity: 0`?**

> **Answer:**
> - `display: none` – Element is removed from the DOM flow. Takes no space.
> - `visibility: hidden` – Element is invisible but still takes up space.
> - `opacity: 0` – Element is fully transparent but still takes space and is still interactive (clickable).

---

**Q12. How does Tailwind CSS differ from traditional CSS and Bootstrap?**

> **Answer:** Tailwind is a **utility-first** CSS framework. Instead of writing custom classes, you compose styles directly in HTML using utility classes like `flex`, `p-4`, `text-lg`, `bg-blue-500`.
> - vs. Bootstrap: Bootstrap is component-based with opinionated design. Tailwind is design-agnostic and highly customizable.
> - vs. Custom CSS: Tailwind reduces context switching between HTML and CSS files. It also purges unused styles for smaller build sizes.

---

## 3. JavaScript (ES6+)

---

**Q13. Explain `let`, `const`, and `var`. What are their differences?**

> **Answer:**
> | | `var` | `let` | `const` |
> |---|---|---|---|
> | Scope | Function | Block | Block |
> | Re-declare | Yes | No | No |
> | Re-assign | Yes | Yes | No |
> | Hoisting | Yes (undefined) | Yes (TDZ) | Yes (TDZ) |
>
> `const` and `let` (ES6) are preferred. `var` has unpredictable scoping and should be avoided.

---

**Q14. What is a closure in JavaScript? Give an example.**

> **Answer:** A closure is a function that "remembers" its outer scope even after the outer function has returned.
>
> ```javascript
> function makeCounter() {
>   let count = 0;
>   return function () {
>     count++;
>     return count;
>   };
> }
> const counter = makeCounter();
> counter(); // 1
> counter(); // 2
> ```
> The inner function retains access to `count` even after `makeCounter()` has finished executing.

---

**Q15. What is the difference between `==` and `===`?**

> **Answer:**
> - `==` performs **type coercion** before comparison. `"5" == 5` is `true`.
> - `===` is **strict equality** — no type coercion. `"5" === 5` is `false`.
>
> Always prefer `===` to avoid unexpected bugs.

---

**Q16. Explain Promises and async/await.**

> **Answer:** Promises handle asynchronous operations. A Promise is in one of three states: **pending**, **fulfilled**, or **rejected**.
>
> ```javascript
> // Promise
> fetch('/api/data')
>   .then(res => res.json())
>   .then(data => console.log(data))
>   .catch(err => console.error(err));
>
> // async/await (cleaner syntax)
> async function getData() {
>   try {
>     const res = await fetch('/api/data');
>     const data = await res.json();
>     console.log(data);
>   } catch (err) {
>     console.error(err);
>   }
> }
> ```
> `async/await` is syntactic sugar over Promises and makes async code look synchronous and more readable.

---

**Q17. What is event delegation and why is it useful?**

> **Answer:** Event delegation means attaching a single event listener to a **parent** element instead of individual child elements. Events bubble up from child to parent.
>
> ```javascript
> document.getElementById('list').addEventListener('click', (e) => {
>   if (e.target.tagName === 'LI') {
>     console.log(e.target.innerText);
>   }
> });
> ```
> Useful for dynamic content (items added after page load) and improves performance with fewer listeners.

---

**Q18. What are arrow functions, and how do they differ from regular functions?**

> **Answer:** Arrow functions (`=>`) are a concise syntax for functions and **do not have their own `this`** — they inherit `this` from the enclosing context.
>
> ```javascript
> // Regular
> function add(a, b) { return a + b; }
>
> // Arrow
> const add = (a, b) => a + b;
> ```
> Arrow functions are not suitable as constructors or object methods that rely on `this`.

---

**Q19. What is the event loop in JavaScript?**

> **Answer:** JavaScript is single-threaded. The event loop manages asynchronous execution:
> 1. **Call Stack** – Executes synchronous code.
> 2. **Web APIs** – Handles async tasks (setTimeout, fetch).
> 3. **Callback Queue / Microtask Queue** – Holds resolved callbacks.
> 4. **Event Loop** – Continuously checks if the call stack is empty and pushes callbacks from the queue.
>
> Promises (microtasks) are prioritized over `setTimeout` (macrotasks).

---

**Q20. What is destructuring in JavaScript?**

> **Answer:** Destructuring extracts values from objects or arrays into variables.
>
> ```javascript
> // Object destructuring
> const { name, age } = { name: 'Kalai', age: 22 };
>
> // Array destructuring
> const [first, second] = [10, 20];
>
> // With default values
> const { role = 'user' } = {};
> ```

---

## 4. React.js

---

**Q21. What is the difference between props and state in React?**

> **Answer:**
> - **Props** – Data passed from **parent to child**. Read-only (immutable from child's perspective).
> - **State** – Data managed **within** a component. Mutable and triggers re-render when changed via `setState` or `useState`.

---

**Q22. Explain the React component lifecycle (for functional components with hooks).**

> **Answer:**
> - **Mount:** `useEffect(() => { ... }, [])` – runs once after initial render.
> - **Update:** `useEffect(() => { ... }, [dependency])` – runs when dependency changes.
> - **Unmount:** Return a cleanup function inside `useEffect`.
>
> ```javascript
> useEffect(() => {
>   // runs on mount / dependency change
>   return () => {
>     // cleanup on unmount
>   };
> }, [dependency]);
> ```

---

**Q23. What is `useMemo` and `useCallback`? When would you use them?**

> **Answer:**
> - `useMemo` – Memoizes the **result** of an expensive computation.
> - `useCallback` – Memoizes a **function reference** to prevent unnecessary re-creation.
>
> Both are performance optimizations used when a child component or computation would re-run unnecessarily on every render. Use them sparingly — premature optimization adds complexity.

---

**Q24. What is the Context API? How is it different from Redux?**

> **Answer:** Context API allows sharing state globally without prop drilling.
>
> ```javascript
> const ThemeContext = React.createContext();
> // Wrap with Provider, consume with useContext
> ```
>
> **Context API** is simpler, built-in, and good for low-frequency updates (theme, auth state).
> **Redux** is more powerful, has a predictable state container with middleware (Thunk, Saga), dev tools, and is better for large-scale, complex state management.

---

**Q25. What are controlled vs. uncontrolled components in React forms?**

> **Answer:**
> - **Controlled:** Form input value is controlled by React state. Every keystroke updates state.
>   ```javascript
>   const [value, setValue] = useState('');
>   <input value={value} onChange={(e) => setValue(e.target.value)} />
>   ```
> - **Uncontrolled:** Form value is managed by the DOM itself, accessed via `useRef`.
>   ```javascript
>   const inputRef = useRef();
>   <input ref={inputRef} />
>   ```
> Controlled components are preferred for validation and predictability.

---

**Q26. How does React's Virtual DOM work?**

> **Answer:** React maintains a lightweight copy of the real DOM called the Virtual DOM. When state changes:
> 1. React creates a new Virtual DOM tree.
> 2. Diffs it with the previous tree (reconciliation).
> 3. Calculates the minimum number of changes.
> 4. Applies only those changes to the real DOM (patching).
>
> This avoids costly full DOM re-renders and makes React fast.

---

**Q27. What is `useRef` and how would you use it?**

> **Answer:** `useRef` returns a mutable object (`{ current: value }`) that persists across renders without causing re-renders.
>
> Common uses:
> - Access DOM elements directly (`inputRef.current.focus()`).
> - Store mutable values like previous state, timers.
>
> ```javascript
> const inputRef = useRef(null);
> <input ref={inputRef} />
> inputRef.current.focus(); // focus programmatically
> ```

---

**Q28. How would you optimize a slow React application?**

> **Answer:**
> - Use `React.memo` to prevent unnecessary re-renders of pure components.
> - Use `useMemo` and `useCallback` for expensive computations and stable function references.
> - Code splitting with `React.lazy` and `Suspense`.
> - Virtualize long lists with `react-window` or `react-virtual`.
> - Avoid anonymous functions in JSX (new reference on every render).
> - Use pagination instead of loading all data at once.
> - Profile with React DevTools.

---

## 5. Node.js & Express.js

---

**Q29. What is Node.js and what makes it suitable for web backends?**

> **Answer:** Node.js is a JavaScript runtime built on Chrome's V8 engine. It's suitable for backends because:
> - **Non-blocking, asynchronous I/O** – handles many concurrent requests efficiently.
> - **Single language** (JS) for both frontend and backend.
> - **npm ecosystem** – massive library ecosystem.
> - Ideal for **real-time applications** (chat, live dashboards) using WebSockets.
> - Not ideal for CPU-intensive tasks.

---

**Q30. Explain middleware in Express.js.**

> **Answer:** Middleware are functions that have access to `req`, `res`, and `next`. They execute in order and can:
> - Modify request/response objects.
> - End the request-response cycle.
> - Call `next()` to pass control to the next middleware.
>
> ```javascript
> app.use((req, res, next) => {
>   console.log(`${req.method} ${req.url}`);
>   next(); // pass to next middleware
> });
> ```
> Common middleware: `cors`, `express.json()`, `morgan`, `helmet`, authentication guards.

---

**Q31. How would you handle errors globally in Express?**

> **Answer:** Define a 4-argument error-handling middleware at the end of all routes:
>
> ```javascript
> app.use((err, req, res, next) => {
>   console.error(err.stack);
>   res.status(err.status || 500).json({ message: err.message || 'Internal Server Error' });
> });
> ```
> Pass errors to it with `next(err)` from route handlers or async functions.

---

**Q32. What is the difference between `process.nextTick()`, `setImmediate()`, and `setTimeout()`?**

> **Answer:**
> - `process.nextTick()` – Executes **before** the event loop moves to the next phase (highest priority among async callbacks).
> - `setImmediate()` – Executes in the **check** phase of the event loop, after I/O.
> - `setTimeout(fn, 0)` – Executes in the **timers** phase, after the specified delay (minimum 1ms).

---

**Q33. How do you manage environment variables in a Node.js application?**

> **Answer:** Use the `dotenv` package. Create a `.env` file:
>
> ```
> PORT=5000
> DB_URI=mongodb://localhost:27017/frl
> JWT_SECRET=supersecret
> ```
>
> Load it in your entry file:
> ```javascript
> require('dotenv').config();
> const port = process.env.PORT;
> ```
> Never commit `.env` to version control — add it to `.gitignore`.

---

**Q34. How would you structure a large Express.js project?**

> **Answer:**
> ```
> /src
>   /routes       – route definitions
>   /controllers  – request handlers
>   /services     – business logic
>   /models       – database schemas
>   /middleware   – auth, validation, error handling
>   /config       – DB, environment config
>   /utils        – helper functions
> index.js        – app entry point
> ```
> This follows the MVC pattern (Model-View-Controller) for separation of concerns.

---

## 6. Databases – MySQL & MongoDB

---

**Q35. What is the difference between SQL and NoSQL databases? When would you choose each?**

> **Answer:**
> | | SQL (MySQL) | NoSQL (MongoDB) |
> |---|---|---|
> | Schema | Fixed, structured | Flexible, dynamic |
> | Relationships | JOINs between tables | Embedded documents or references |
> | Scaling | Vertical | Horizontal |
> | ACID | Full | Partial (MongoDB 4+ supports ACID) |
>
> Choose **MySQL** for complex relationships, strict data integrity (e.g., financial data, academic systems).
> Choose **MongoDB** for flexible schemas, rapid development, hierarchical data (e.g., social media, content management).

---

**Q36. What are indexes in a database? Why are they important?**

> **Answer:** Indexes are data structures that improve the speed of data retrieval. Without an index, the database does a full table scan (O(n)). With an index, it's O(log n).
>
> ```sql
> CREATE INDEX idx_email ON users(email);
> ```
>
> Trade-off: Indexes speed up reads but slow down writes and use extra storage. Use them on columns frequently queried or used in WHERE, JOIN, ORDER BY.

---

**Q37. What is database normalization? Explain 1NF, 2NF, 3NF.**

> **Answer:** Normalization organizes tables to reduce redundancy and improve integrity.
> - **1NF** – Each column has atomic (indivisible) values; no repeating groups.
> - **2NF** – 1NF + no partial dependency (all non-key columns depend on the **whole** primary key).
> - **3NF** – 2NF + no transitive dependency (non-key columns depend only on the primary key, not on other non-key columns).

---

**Q38. What is a JOIN in SQL? Explain different types.**

> **Answer:**
> - `INNER JOIN` – Returns rows matching in **both** tables.
> - `LEFT JOIN` – All rows from the left table + matching from right (NULL if no match).
> - `RIGHT JOIN` – All rows from the right table + matching from left.
> - `FULL OUTER JOIN` – All rows from both tables (NULL where no match).
>
> ```sql
> SELECT u.name, o.total
> FROM users u
> INNER JOIN orders o ON u.id = o.user_id;
> ```

---

**Q39. What is a transaction in a database and what are ACID properties?**

> **Answer:** A transaction is a group of operations that execute as a single unit.
>
> **ACID:**
> - **Atomicity** – All or nothing. If one step fails, the whole transaction rolls back.
> - **Consistency** – Database moves from one valid state to another.
> - **Isolation** – Concurrent transactions don't interfere.
> - **Durability** – Committed transactions survive system failures.

---

**Q40. How would you prevent SQL injection?**

> **Answer:** Use **prepared statements / parameterized queries**. You did this in your University Management System.
>
> ```javascript
> // Vulnerable (don't do this)
> db.query(`SELECT * FROM users WHERE email = '${email}'`);
>
> // Safe
> db.query('SELECT * FROM users WHERE email = ?', [email]);
> ```
> Also: use ORM/ODM (Sequelize, Mongoose), validate/sanitize inputs, and limit DB user privileges.

---

**Q41. What is Redis and how did you use it in your internship?**

> **Answer:** Redis is an in-memory key-value data store used for caching, session management, and task queuing. In my internship at Hogist, I used Redis as a **message broker with Celery** for background task processing — specifically for scheduling social media posts asynchronously without blocking the main web server.

---

## 7. REST APIs & Authentication

---

**Q42. What are the HTTP methods and what does each do in a RESTful API?**

> **Answer:**
> | Method | Action |
> |---|---|
> | GET | Read/retrieve data |
> | POST | Create new resource |
> | PUT | Replace entire resource |
> | PATCH | Partially update resource |
> | DELETE | Delete resource |

---

**Q43. What is the difference between PUT and PATCH?**

> **Answer:**
> - `PUT` replaces the **entire** resource. If you don't send all fields, missing ones are set to null/default.
> - `PATCH` performs a **partial update** — only the provided fields are updated.

---

**Q44. What are HTTP status codes? Give examples.**

> **Answer:**
> - `200 OK` – Success
> - `201 Created` – Resource created
> - `400 Bad Request` – Invalid input
> - `401 Unauthorized` – Authentication required
> - `403 Forbidden` – Authenticated but not allowed
> - `404 Not Found` – Resource not found
> - `500 Internal Server Error` – Server-side error

---

**Q45. How does JWT authentication work?**

> **Answer:** JWT (JSON Web Token) is a stateless authentication mechanism.
>
> 1. User logs in with credentials.
> 2. Server validates and generates a signed JWT: `Header.Payload.Signature`.
> 3. Client stores the token (usually in memory or HTTP-only cookie).
> 4. Client sends token in `Authorization: Bearer <token>` header on each request.
> 5. Server verifies the signature and extracts the payload (userId, role, etc.).
>
> ```javascript
> // Sign
> const token = jwt.sign({ userId: user.id }, process.env.JWT_SECRET, { expiresIn: '7d' });
>
> // Verify middleware
> const decoded = jwt.verify(token, process.env.JWT_SECRET);
> ```

---

**Q46. What is the difference between authentication and authorization?**

> **Answer:**
> - **Authentication** – Verifying *who* the user is (login, JWT verification).
> - **Authorization** – Verifying *what* the user can do (role-based access, permissions).
>
> Example: You're authenticated as a user, but not **authorized** to access the admin dashboard.

---

**Q47. How would you implement role-based access control (RBAC)?**

> **Answer:**
> 1. Store `role` in the JWT payload (e.g., `admin`, `faculty`, `student`).
> 2. Create a middleware that checks role:
>
> ```javascript
> const requireRole = (role) => (req, res, next) => {
>   if (req.user.role !== role) return res.status(403).json({ message: 'Forbidden' });
>   next();
> };
>
> app.get('/admin/dashboard', authMiddleware, requireRole('admin'), controller);
> ```
> You implemented multi-user roles in your University Management System project.

---

## 8. DevOps, Docker & CI/CD

---

**Q48. What is Docker and why would you use it?**

> **Answer:** Docker is a containerization platform that packages an application and all its dependencies into a portable container.
>
> Benefits:
> - **Consistency** – "Works on my machine" problem is eliminated.
> - **Isolation** – Each service runs in its own container.
> - **Scalability** – Easily spin up multiple instances.
> - **Lightweight** – Faster than VMs.

---

**Q49. What is the difference between a Docker image and a container?**

> **Answer:**
> - **Image** – A read-only blueprint (like a class). Built from a `Dockerfile`.
> - **Container** – A running instance of an image (like an object). Mutable at runtime.

---

**Q50. What is a Dockerfile? Write a basic one for a Node.js app.**

> **Answer:**
> ```dockerfile
> FROM node:18-alpine
> WORKDIR /app
> COPY package*.json ./
> RUN npm install
> COPY . .
> EXPOSE 5000
> CMD ["node", "index.js"]
> ```

---

**Q51. What is CI/CD and what tools have you used?**

> **Answer:** CI/CD stands for **Continuous Integration / Continuous Delivery (or Deployment)**.
> - **CI** – Automatically test and build code on every push/PR.
> - **CD** – Automatically deploy passing builds to staging/production.
>
> Tools: GitHub Actions, Jenkins, GitLab CI. In your internship you gained hands-on experience with CI/CD pipelines and AWS deployment.

---

## 9. Cloud – AWS

---

**Q52. What is Amazon EC2 and how would you deploy a Node.js app on it?**

> **Answer:** EC2 (Elastic Compute Cloud) is AWS's virtual server service.
>
> Steps to deploy:
> 1. Launch an EC2 instance (Ubuntu).
> 2. SSH into the instance.
> 3. Install Node.js, npm, PM2.
> 4. Clone your repo and run `npm install`.
> 5. Use PM2 to run the app as a daemon: `pm2 start index.js`.
> 6. Configure security groups to open port 80/443.
> 7. Optionally set up Nginx as a reverse proxy.

---

**Q53. What is Amazon S3 and what would you use it for in a web portal?**

> **Answer:** S3 (Simple Storage Service) is AWS's object storage service.
>
> In FRL's portal, I would use S3 for:
> - Storing and serving uploaded files (reports, PDFs, images).
> - Storing static assets (frontend build files if using S3 + CloudFront).
> - Allowing signed URLs for secure, temporary file access.

---

## 10. Version Control – Git & GitHub

---

**Q54. What is the difference between `git merge` and `git rebase`?**

> **Answer:**
> - `git merge` – Combines two branches and creates a **merge commit**. Preserves history.
> - `git rebase` – Moves or "replays" commits from one branch onto another. Creates a **linear history** (cleaner, but rewrites history).
>
> Use merge for feature branches going into main. Use rebase carefully on local branches to clean up commits before a PR.

---

**Q55. What is a pull request (PR) and what is its purpose?**

> **Answer:** A PR is a request to merge changes from one branch into another. It enables:
> - **Code review** – Team members can review and comment.
> - **Discussion** – Collaborative problem-solving.
> - **CI checks** – Automated tests run before merging.
> - **Audit trail** – Track what changed and why.

---

**Q56. How do you resolve a merge conflict?**

> **Answer:**
> 1. `git pull` or `git merge` triggers the conflict.
> 2. Git marks conflicting lines in the file with `<<<<<<`, `=======`, `>>>>>>`.
> 3. Manually edit the file to keep the correct code.
> 4. `git add <file>` to mark as resolved.
> 5. `git commit` to complete the merge.

---

## 11. CRM & Third-Party API Integration

---

**Q57. What is a CRM and how would you integrate Zoho CRM with a web portal?**

> **Answer:** CRM (Customer Relationship Management) software helps manage customer interactions. For FRL, this might include client inquiries, leads, and service requests.
>
> Zoho CRM integration:
> 1. Generate OAuth 2.0 credentials from Zoho developer console.
> 2. Use the Zoho CRM REST API to create/read/update records.
> 3. Sync form submissions from the FRL portal to Zoho CRM via API calls.
> 4. Handle webhooks from Zoho to update the portal in real-time.

---

**Q58. How would you integrate a payment gateway like Razorpay?**

> **Answer:**
> 1. Install Razorpay SDK (`npm install razorpay`).
> 2. Backend creates an order:
>    ```javascript
>    const order = await razorpay.orders.create({ amount: 50000, currency: 'INR' });
>    ```
> 3. Frontend opens Razorpay checkout with `order_id`.
> 4. On payment success, Razorpay sends `razorpay_payment_id` and `razorpay_signature`.
> 5. Backend **verifies** the signature using `crypto` module to confirm payment authenticity.
> 6. Update the database on successful verification.

---

**Q59. You worked with Meta Graph API and YouTube Data API in your internship. How do OAuth flows work for these APIs?**

> **Answer:**
> 1. User is redirected to the provider's (Meta/Google) login page.
> 2. User grants permission to specific scopes (e.g., `publish_to_groups`, `youtube.upload`).
> 3. Provider redirects back to your app with an **authorization code**.
> 4. Your backend exchanges the code for an **access token** (and optionally a refresh token).
> 5. Use the access token in API requests.
> 6. Refresh tokens are used to obtain new access tokens when they expire without re-prompting the user.

---

## 12. Security Best Practices

---

**Q60. What is CORS and how do you handle it in Express?**

> **Answer:** CORS (Cross-Origin Resource Sharing) is a browser security policy that restricts web pages from making requests to a different domain than the one that served the page.
>
> In Express:
> ```javascript
> const cors = require('cors');
> app.use(cors({
>   origin: ['https://frl.com', 'http://localhost:3000'],
>   methods: ['GET', 'POST', 'PUT', 'DELETE'],
>   credentials: true
> }));
> ```

---

**Q61. What is XSS and how do you prevent it?**

> **Answer:** XSS (Cross-Site Scripting) is an attack where malicious scripts are injected into web pages viewed by other users.
>
> Prevention:
> - **Sanitize and escape** user input before rendering in HTML.
> - Use `Content-Security-Policy` headers.
> - React escapes JSX expressions by default (safe from XSS in most cases).
> - Use libraries like `DOMPurify` for rich text.
> - Set `HttpOnly` cookies (inaccessible to JavaScript).

---

**Q62. What security headers should you set on a web application?**

> **Answer:** Use `helmet` in Express which sets secure HTTP headers:
> ```javascript
> const helmet = require('helmet');
> app.use(helmet());
> ```
> Key headers:
> - `Content-Security-Policy` – Prevents XSS.
> - `X-Content-Type-Options: nosniff` – Prevents MIME sniffing.
> - `X-Frame-Options: DENY` – Prevents clickjacking.
> - `Strict-Transport-Security` – Enforces HTTPS.

---

## 13. Project-Based Questions (From Your Resume)

---

**Q63. Walk me through your Hidden Camera Detector app. What challenges did you face?**

> **Answer:** I built a cross-platform mobile app using React Native and TensorFlow.js that detects hidden cameras using magnetometer data and AI-based image processing.
>
> **Challenge:** Getting TensorFlow.js to run efficiently on mobile devices was tricky due to limited compute. I optimized by using a pre-trained lightweight model and ran inference only when significant magnetic field anomalies were detected, rather than continuously — reducing battery drain significantly. Implementing dark/light theme with accessibility was also a learning experience in React Native's styling system.

---

**Q64. How did you secure your University Management System against SQL injection?**

> **Answer:** I used **prepared statements with JDBC** in Java. Instead of building SQL strings with string concatenation (vulnerable), I used `PreparedStatement`:
>
> ```java
> PreparedStatement ps = conn.prepareStatement("SELECT * FROM students WHERE id = ?");
> ps.setInt(1, studentId);
> ResultSet rs = ps.executeQuery();
> ```
> The `?` placeholder is bound separately from the query, so even if the input contains SQL characters, it's treated as a literal value, not SQL syntax.

---

**Q65. Explain the architecture of your AI-Powered Voice Sales Automation Agent at Hogist.**

> **Answer:** The system had several layers:
> 1. **Telephony Layer** – Integrated Tele CMI virtual telephony API for outbound calls.
> 2. **STT (Speech-to-Text)** – Used Deepgram to transcribe caller responses in real-time, fine-tuned for Indian English accents.
> 3. **NLP/Intent Layer** – Built intent detection and objection handling modules to understand what the prospect said.
> 4. **Conversation Engine** – Designed dynamic, context-aware conversation flows (state machine).
> 5. **TTS (Text-to-Speech)** – Used ElevenLabs to generate natural-sounding Indian voice responses.
> 6. **Analytics** – Logged all calls and analyzed conversation data to improve the model.
> 7. **Infrastructure** – Deployed on AWS using PyTorch/TensorFlow for model serving.

---

**Q66. How did you handle scalable scheduling in your Social Media Automation Tool?**

> **Answer:** I used **Celery with Redis** as the message broker. When a user schedules a post for a future time:
> 1. The task is serialized and pushed to a Redis queue with an ETA.
> 2. Celery workers pick up tasks from the queue at the scheduled time.
> 3. The worker calls the Meta Graph API or YouTube Data API to publish the post.
>
> This decouples the web server from long-running background tasks and allows scaling workers independently.

---

**Q67. How would you apply your experience to building FRL's recipe database portal?**

> **Answer:** Based on my experience:
> - **Backend:** I'd design RESTful APIs with Node.js/Express for CRUD operations on recipes, ingredients, and categories, secured with JWT and role-based access.
> - **Database:** Use MySQL for structured recipe data (normalized tables for recipes, ingredients, tags, nutritional info) and potentially MongoDB for flexible metadata.
> - **Frontend:** Build a responsive React UI with Tailwind CSS — dynamic search, filters, dashboards for analytics.
> - **File Management:** Use AWS S3 for storing recipe PDFs and images.
> - **CRM Integration:** Sync user inquiries and client data with Zoho CRM via REST API.

---

## 14. System Design & Architecture

---

**Q68. How would you design a scalable file upload system for FRL's portal (uploading/downloading research reports)?**

> **Answer:**
> 1. Frontend sends a request to the backend for a **pre-signed S3 URL**.
> 2. Frontend uploads the file directly to S3 using the pre-signed URL (bypasses backend, reducing load).
> 3. On upload success, frontend notifies backend with the S3 file key.
> 4. Backend stores file metadata (name, key, uploader, timestamp) in the database.
> 5. For download, generate a **signed URL** with an expiry time so only authorized users can access files.
>
> This approach is scalable, secure, and doesn't burden the backend server with file bytes.

---

**Q69. How would you design the user role management system for FRL's portal?**

> **Answer:**
> - **Roles:** Admin, Project Manager, Researcher, Client.
> - DB table: `users` (id, name, email, role, created_at).
> - JWT payload includes `role`.
> - Middleware checks role before granting access to protected routes.
> - Admin UI to assign/change roles.
> - Fine-grained permissions can be stored in a `permissions` table for complex access control.

---

**Q70. How would you handle real-time dashboard updates for social analytics data?**

> **Answer:** I would use **WebSockets** (via Socket.io) or **Server-Sent Events (SSE)**:
> - Backend emits analytics updates via Socket.io rooms.
> - Frontend subscribes to the relevant room and updates the UI in real-time.
>
> Alternatively, for polling-based dashboards, use SWR or React Query with `refetchInterval` for automatic periodic data fetching without WebSockets.

---

## 15. Problem Solving & Data Structures

---

**Q71. What is the time complexity of common operations in an array vs. a hash map?**

> **Answer:**
> | Operation | Array | Hash Map |
> |---|---|---|
> | Access by index/key | O(1) | O(1) avg |
> | Search | O(n) | O(1) avg |
> | Insert at end | O(1) amortized | O(1) avg |
> | Delete | O(n) | O(1) avg |

---

**Q72. How would you find duplicates in an array? What is the optimal approach?**

> **Answer:**
> ```javascript
> function findDuplicates(arr) {
>   const seen = new Set();
>   const duplicates = new Set();
>   for (const item of arr) {
>     if (seen.has(item)) duplicates.add(item);
>     else seen.add(item);
>   }
>   return [...duplicates];
> }
> ```
> Time: O(n), Space: O(n). Using a Set for O(1) lookups.

---

**Q73. What is recursion? Give an example.**

> **Answer:** Recursion is when a function calls itself with a smaller input until it hits a base case.
>
> ```javascript
> function factorial(n) {
>   if (n <= 1) return 1; // base case
>   return n * factorial(n - 1); // recursive case
> }
> factorial(5); // 120
> ```

---

## 16. Soft Skills & Situational Questions

---

**Q74. Describe a time you had to learn a new technology quickly.**

> **Answer:** During my internship at Hogist, I had to quickly learn **Deepgram STT API** and **ElevenLabs TTS** for the Voice Automation project. I had no prior experience with speech processing. I spent a weekend going through their documentation, ran small experiments, and within a week, I had an integrated pipeline working. The key was to start with minimal working examples and iterate fast rather than trying to learn everything upfront.

---

**Q75. How do you handle tight deadlines and multiple tasks?**

> **Answer:** I prioritize tasks based on impact and dependency. I use a simple Kanban approach — what's blocking others comes first. I communicate early if something is at risk of slipping. At Hogist, I simultaneously worked on two projects by time-boxing focused work sessions for each and syncing with my manager daily.

---

**Q76. Have you worked in an Agile/Scrum environment?**

> **Answer:** Yes. At Hogist, we followed Agile practices — daily standups, sprint planning, and retrospectives. I'm familiar with breaking work into user stories, estimating complexity, and delivering incremental working features each sprint. I've also used GitHub Projects and task boards to track progress.

---

**Q77. How do you handle a situation where you disagree with your team lead's technical approach?**

> **Answer:** I'd first understand the reasoning behind their approach by asking questions rather than immediately pushing back. Then I'd present my alternative with clear reasoning, trade-offs, and data. If we still disagree, I respect their final decision and execute it professionally — but I document my concerns in case we revisit. Disagreements handled well actually strengthen team trust.

---

## 17. Company & Role Specific Questions

---

**Q78. What does FRL do, and how does technology help their business?**

> **Answer:** Food Research Lab is a CDMO (Contract Development and Manufacturing Organization) specializing in food, beverages, nutraceuticals, and pet food. Technology helps FRL by:
> - Digitizing recipe databases for faster R&D iteration.
> - Managing client relationships via CRM integration.
> - Providing analytics dashboards to track project progress and performance.
> - Automating document generation and report sharing with clients.
> - Enabling regulatory IP management digitally.

---

**Q79. What features would you prioritize for FRL's web portal in the first 30 days?**

> **Answer:**
> 1. **User authentication & role management** – Foundation for all other features.
> 2. **Recipe database CRUD** – Core product value.
> 3. **File upload/download system** – For sharing R&D reports.
> 4. **Basic CRM integration** – To capture and manage client inquiries.
> 5. **Responsive UI layout** – Ensure the portal is usable across devices.
>
> I'd start with a solid backend architecture and basic frontend before adding analytics and payment features.

---

**Q80. Do you have any questions for us?**

> **Suggested questions to ask the interviewer:**
> - What does the current tech stack look like, and are there plans to evolve it?
> - What does the onboarding process look like for interns?
> - What are the biggest technical challenges the team is currently facing?
> - How is code reviewed and what does the deployment pipeline look like?
> - What does success look like for this role in the first 3 months?

---

## 🎯 Quick Revision Cheat Sheet

| Topic | Key Points |
|---|---|
| React Hooks | useState, useEffect, useRef, useMemo, useCallback, useContext |
| JWT Flow | Login → Sign token → Send in header → Verify in middleware |
| REST Methods | GET, POST, PUT, PATCH, DELETE |
| SQL vs NoSQL | Structured/ACID vs Flexible/Scalable |
| Docker | Image = blueprint, Container = running instance |
| CORS | Cross-origin policy, solved with `cors` middleware |
| SQL Injection | Prevented with prepared statements (you did this!) |
| Event Loop | Call Stack → Web APIs → Queue → Loop |
| Closure | Inner function remembers outer scope |
| Normalization | 1NF (atomic) → 2NF (no partial dep) → 3NF (no transitive dep) |

---
