## Request and Response Cycle

The request & response cycle is the process that happens every time a client (browser, mobile app, API consumer) communicates with a server.

It is the foundation of how the web works.

```mermaid
flowchart TD
    A[👤 User Action<br/>Click/Type/Load] --> B[📤 Client Request]
    B --> C[🌐 Internet Journey]
    C --> D[🖥️ Server Processing]
    D --> E[📥 Server Response]
    E --> F[📱 Client Rendering]
    F --> A
    
    style B fill:#e1f5fe
    style C fill:#c8e6c9
    style D fill:#ffccbc
    style E fill:#d1c4e9
    style F fill:#bbdefb
```

**Simple analogy:** Like ordering food at a restaurant 🍽️
- **Request** = Your order (what you want, how you want it)
- **Processing** = Kitchen prepares your food
- **Response** = Server brings your meal (success) or explains issues (errors)

### 1. Client Makes a Request

The cycle starts when a client sends a request to a server.

This can happen when:
- You open a website
- You click a button
- An app fetches data
- A form is submitted

A request includes:
URL / Endpoint
**Example:** ```/products/5```

**HTTP Method**
- GET – Retrieve data
- POST – Send data
- PUT / PATCH – Update data
- DELETE – Remove data

**Headers**
Metadata like:
- Content-Type
- Authorization token
- User-Agent

**Body (optional)**
Data sent to the server (usually JSON):
```json
{
  "email": "user@email.com",
  "password": "123456"
}
```

### 2. The Request Travels Through the Internet

```mermaid
sequenceDiagram
    participant C as Client
    participant D as DNS
    participant R as Router
    participant F as Firewall
    participant LB as Load Balancer
    participant RP as Reverse Proxy
    participant S as Server
    
    C->>D: DNS Query: api.example.com?
    D->>C: IP: 192.0.2.1
    
    Note over C,R: Request begins journey
    C->>R: HTTP Request to 192.0.2.1
    R->>F: Route through network
    F->>LB: Check security rules
    LB->>RP: Distribute to available server
    RP->>S: Forward to actual server
    Note over S: Server receives request
```

The request travels through:

- DNS (to resolve the domain → IP)
- Routers
- Firewalls
- Load balancers (if any)
- Reverse proxies (if any)

Until it reaches the server.

### 3. The Server Processes the Request

Once the request reaches the server:

1. Server receives the request

2. A router checks the URL:
    - /users
    - /orders/5

3. Middleware runs:
    - Authentication
    - Validation
    - Logging
    - CORS rules
4. Controller / handler is executed

5. Server may:
    - Query a database
    - Read files
    - Call another API
    - Process business logic

**Example (Node / Express):***
```javascript
app.get('/users/:id', (req, res) => {
  const userId = req.params.id;
  const user = getUserFromDB(userId);
  res.json(user);
});
```

### 4. The Server Sends a Response

After processing, the server sends back a response, which includes:

Status code
Headers
Body (data)

**Example response:**

**http:**
```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**json:**
```json
{
  "id": 5,
  "name": "Hernando Abella",
  "role": "Backend Developer"
}
```

### 5. The Client Receives & Uses the Response
The client then:
- Shows content on the page
- Displays an error
- Stores a token
- Updates the UI
- Continues another request

**Example in frontend JS:**
```javascript
fetch('/api/users/5')
  .then(res => res.json())
  .then(data => console.log(data));
```

### HTTP Request Components
```mermaid
graph TB
    subgraph HTTP_Request_Components[" "]
        A["HTTP Request"] --> B["Start Line"]
        A --> C["Headers"]
        A --> D["Body"]
        
        %% Start Line
        B --> E["Method (GET / POST / PUT / DELETE)"]
        B --> F["URL (/api/users/5)"]
        B --> G["HTTP Version (HTTP/1.1)"]
        
        %% Headers
        C --> H["Content-Type: application/json"]
        C --> I["Authorization: Bearer <token>"]
        C --> J["User-Agent: Browser info"]
        C --> K["Accept: Expected response type"]
        
        %% Body
        D --> L["JSON / Form-Data / Binary"]
    end

    %% Styles
    style B fill:#c8e6c9,stroke:#333
    style C fill:#ffccbc,stroke:#333
    style D fill:#d1c4e9,stroke:#333
```

### Complete HTTP Request Example:
```http
POST /api/login HTTP/1.1
Host: api.example.com
Content-Type: application/json
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64)
Accept: application/json
Content-Length: 56

{
  "email": "user@example.com",
  "password": "securePass123"
}
```

### HTTP Methods Explained:

```mermaid
graph LR
    subgraph "HTTP Methods"
        GET["🔍 GET<br/>Retrieve data"]
        POST["📨 POST<br/>Create data"]
        PUT["✏️ PUT<br/>Update entire resource"]
        PATCH["🩹 PATCH<br/>Partial update"]
        DELETE["🗑️ DELETE<br/>Remove data"]
        OPTIONS["🔧 OPTIONS<br/>Preflight check"]
    end
    
    style GET fill:#c8e6c9
    style POST fill:#ffccbc
    style PUT fill:#bbdefb
    style PATCH fill:#d1c4e9
    style DELETE fill:#ffcdd2
    style OPTIONS fill:#fff9c4
```

### HTTP Methods Overview

| Method   | Idempotent | Safe | Body Allowed | Use Case                  |
|---------|-------------|------|--------------|---------------------------|
| GET     | ✅ Yes       | ✅ Yes | ❌ No        | Fetch data, search        |
| POST    | ❌ No       | ❌ No | ✅ Yes        | Create new resource        |
| PUT     | ✅ Yes       | ❌ No | ✅ Yes        | Replace entire resource    |
| PATCH   | ❌ No       | ❌ No | ✅ Yes        | Update partial resource    |
| DELETE  | ✅ Yes       | ❌ No | ❌ No        | Remove resource             |
| OPTIONS | ✅ Yes       | ✅ Yes | ❌ No        | CORS preflight              |

### Common Request Headers

| Header         | Purpose                         | Example                |
|---------------|----------------------------------|------------------------|
| Content-Type   | Format of request body           | application/json       |
| Authorization  | Authentication credentials        | Bearer token123         |
| User-Agent     | Client identification             | Mozilla/5.0...          |
| Accept         | Expected response format          | application/json         |
| Cookie         | Session data                       | sessionId=abc123        |
| Origin         | Source domain (CORS)               | https://example.com     |
| Content-Length | Size of request body               | 256                    |

