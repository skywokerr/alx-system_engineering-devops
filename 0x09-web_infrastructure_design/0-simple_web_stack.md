# Simple Web Infrastructure Design

<img width="522" height="821" alt="0-simple_web_stack_diagram" src="https://github.com/user-attachments/assets/3fbc3de4-56c6-48d1-97b7-6fcb4104ea84" />


## Infrastructure Components

1. **Server**  
   - A single physical/virtual machine hosting all components
   - IP Address: 8.8.8.8

2. **Domain Name & DNS**  
   - Domain: foobar.com
   - DNS Coniguration: 
     -ww.foobar. com -> CNAME -> foobar.com
   - foobar.com -> A Record -> 8.8.8.8

3. **Web Server (Nginx)**  
   - Handles HTTP/HTTPS requests
   - Serves static files (HTML, CSS, images)
   - Proxies dynamic requests to application server

5. **Application Server**  
   - Runs backend code(Python/Django)
   - Executes business logic
   - Interfaces with database

6. **Database (MySQL)**  
   - Central data repository
   - Manages user accounts, content, and application state

7. **Communication Flow**
   User → DNS → Web Server → Application Server → Database

## Infrastructure Issues

1. **Single Point of Failure (SPOF)**  
- Entire system fails if the single server goes down

2. **Maintenance Downtime**  
- Service interruptions during updates

3. **Vertical Scaling Limits**  
- Cannot handle traffic spikes (no load balancing)


4. **Security Exposure**  
- No firewall/HTTPS; shared resource vulnerabilities


