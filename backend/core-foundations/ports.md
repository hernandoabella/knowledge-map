## Ports
A port is a virtual endpoint for network communications on a device, allowing multiple applications to use the network simultaneously through a single IP address.

```mermaid
flowchart TD
    A[Single IP Address<br/>192.168.1.100] --> B[Multiple Ports]
    B --> C[Port 80: Web Server]
    B --> D[Port 443: HTTPS]
    B --> E[Port 3306: MySQL]
    B --> F[Port 22: SSH]
    B --> G[Port 3000: Node.js App]
    
    style A fill:#e1f5fe
    style C fill:#c8e6c9
    style D fill:#c8e6c9
    style E fill:#c8e6c9
    style F fill:#c8e6c9
    style G fill:#c8e6c9
```

**Simple analogy:** Ports are like apartment numbers in a building 🏢 – the IP is the building address, ports are individual apartments where different services live.

### How Ports Work
```mermaid
sequenceDiagram
    participant C as Client
    participant S as Server (192.168.1.100)
    
    Note over C,S: Client wants to access multiple services<br/>on the same server
    
    C->>S:80: GET / (HTTP Request)
    S->>C:80: HTML Response (Web Server)
    
    C->>S:443: GET /api (HTTPS Request)
    S->>C:443: JSON Response (API Server)
    
    C->>S:22: SSH Connection
    S->>C:22: Shell Access
    
    C->>S:5432: Database Query
    S->>C:5432: Query Results
    
    Note over C,S: All on same IP, different ports!
```

### Key Concepts:
- **Port Range:** 0 to 65535
- **Format:** IP:Port (e.g., 192.168.1.100:3000)
- **Purpose:** Multiplexing – multiple services on one IP
- **Transport Protocols:** TCP (reliable) and UDP (fast)

### Port Categories
```mermaid
graph TB
    A[Port Categories] --> B[Well-Known Ports<br/>0-1023]
    A --> C[Registered Ports<br/>1024-49151]
    A --> D[Dynamic/Private Ports<br/>49152-65535]
    
    B --> E[System/Privileged<br/>Require admin rights]
    C --> F[User Applications<br/>Common services]
    D --> G[Ephemeral Ports<br/>Client-side connections]
    
    style B fill:#ffcdd2
    style C fill:#c8e6c9
    style D fill:#bbdefb
```

### 1. Well-Known Ports (0-1023)
```bash
# System services, require admin privileges
20/21: FTP (File Transfer)
22: SSH (Secure Shell)
25: SMTP (Email)
53: DNS (Domain Name System)
80: HTTP (Web)
443: HTTPS (Secure Web)
3306: MySQL
5432: PostgreSQL
```

### 2. Registered Ports (1024-49151)
```bash
# Common application ports
27017: MongoDB
6379: Redis
8080: HTTP Alternate
3000: Node.js Development
4200: Angular Development
5000: Flask Development
8000: Django Development
9200: Elasticsearch
```

### 3. Dynamic/Private Ports (49152-65535)
- Ephemeral ports for client connections
- Assigned dynamically by operating system
- Short-lived connections

### Essential Ports Every Developer Should Know:
| Port  | Service        | Protocol | Description                    |
|------|----------------|----------|--------------------------------|
| 22   | SSH            | TCP      | Secure remote access          |
| 80   | HTTP           | TCP      | Unencrypted web traffic        |
| 443  | HTTPS          | TCP      | Encrypted web traffic          |
| 53   | DNS            | UDP/TCP  | Domain name resolution         |
| 25   | SMTP           | TCP      | Email sending                   |
| 3306 | MySQL          | TCP      | MySQL database                  |
| 5432 | PostgreSQL     | TCP      | PostgreSQL database             |
| 27017| MongoDB        | TCP      | MongoDB database                |
| 6379 | Redis          | TCP      | Redis cache/database            |
| 9200 | Elasticsearch  | TCP      | Search engine                   |
| 3000 | Node.js        | TCP      | Common dev port                 |
| 8080 | HTTP Alt       | TCP      | Alternative web port            |
| 9000 | PHP-FPM        | TCP      | PHP FastCGI                     |


### Ports in Development Workflow
```mermaid
graph LR
    subgraph "Development Environment"
        A[Local Development] --> B[Port 3000: React App]
        A --> C[Port 3001: Node.js API]
        A --> D[Port 5432: PostgreSQL]
        A --> E[Port 6379: Redis]
        A --> F[Port 27017: MongoDB]
    end
    
    subgraph "Production Environment"
        G[Production Server] --> H[Port 443: HTTPS]
        G --> I[Port 80: HTTP Redirect]
        G --> J[Port 22: SSH Access]
        G --> K[Port 3306: MySQL]
    end
    
    style B fill:#c8e6c9
    style C fill:#c8e6c9
    style D fill:#c8e6c9
    style E fill:#c8e6c9
    style F fill:#c8e6c9
    style H fill:#ffccbc
    style I fill:#ffccbc
    style J fill:#ffccbc
    style K fill:#ffccbc
```

### Development vs Production Ports:

| Environment       | Common Ports              | Notes |
|------------------|----------------------------|------|
| Local Development | 3000, 4200, 8080, 5000    | Avoid privileged ports |
| Docker            | Mapped ports (e.g., 8080:80) | Host:Container mapping |
| Production        | 443, 80, 22, 3306          | Standard service ports |
| Cloud             | Varies by service           | Often load balancer ports |

### Port Commands & Tools
```bash
# Check listening ports
netstat -tuln              # All listening ports
ss -tuln                   # Modern alternative
lsof -i -P -n              # Show processes using ports

# Check specific port
nc -zv localhost 3000      # Test if port is open
telnet localhost 3000      # Test TCP connection
nmap -p 3000 localhost     # Port scanning

# Port forwarding
ssh -L 5432:localhost:5432 user@server  # Local port forward
ssh -R 3000:localhost:3000 user@server  # Remote port forward

# Kill process on port
sudo lsof -ti:3000 | xargs kill -9      # Kill process on port 3000

# Find which process uses port
sudo netstat -tulnp | grep :3000
sudo ss -tulnp | grep :3000
```