# Difference between TLS and SSL

### SSL (Secure Sockets Layer)

- Original encryption protocol developed by Netscape in the 1990s  
- Considered **insecure** and should not be used anymore  
<br>

### TLS (Transport Layer Security) 
- Successor to SSL — standardized and more secure  
- Provides stronger encryption algorithms and faster handshakes  
- TLS replaces SSL  
- The term *“SSL certificate”* is still commonly used, but it actually refers to TLS certificates today  

-> Always use TLS 1.3 for modern IoT and web applications

---

# TLS / SSL Authentication

### Use Case
- Secure communication between all system components  
- Protects data transmitted between excavators, MQTT broker, gRPC services, and HTTPS endpoints
<br><br>

### TLS / SSL provides
- Confidentiality: <br> Prevents third parties from reading transmitted data  
- Integrity: <br> detects data tampering during transmission  
- Authentication – verifies that both server and client are legitimate

---

# Authorization

- Purpose: <br>
    Control *who* can do *what* in the system  
- Ensures only registered excavators can publish telemetry data  
- Servers and dashboards have restricted read access via tokens or certificates

---

# Enforcement Layers

### MQTT Broker

* Access Control Lists (ACLs) to restrict which devices can publish or subscribe
* Client identity can be verified using X.509 certificates or token-based authentication.
<br><br>
### Web API

* Protect REST or gRPC endpoints using **OAuth2 / JWT tokens**.
* Tokens can be issued by an Identity Provider (IdP) like Keycloak
* Middleware validates the token, extracts claims, and enforces access rules per endpoint
<br><br>
### Database Layer

* Role-based access control (RBAC) or row-level security
* Combine database-level roles with application-layer authorization for defense in depth.
