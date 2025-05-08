# **Network Security Fundamentals**

Network security involves measures to protect data and ensure secure communication across networks. Its core principles include:

### **1. Confidentiality**

- Ensures that only the sender and intended receiver can access and understand the message.
- **Methods:**
    - **Encryption:** The sender encrypts the message.
    - **Decryption:** The receiver decrypts the message.

### **2. Authentication**

- Verifies the identities of both the sender and receiver to prevent impersonation.
- **Methods:**
    - Passwords, biometrics, digital certificates, and two-factor authentication (2FA).

### **3. Message Integrity**

- Ensures that the message is not altered during transmission or storage without detection.
- **Methods:**
    - **Hashing (e.g., SHA-256, MD5)**
    - **Digital signatures**

### **4. Access Control & Availability**

- Ensures that authorized users can access services when needed.
- **Methods:**
    - Firewalls, intrusion detection/prevention systems (IDS/IPS), and DDoS protection.

# **Web Application Security Best Practices**

## **Server-Side Protections**

1. **Information Gathering Prevention**
    - Add server-side comments explaining security measures
    - Disable directory listing
    - Limit verbose error messages
2. **Input Validation & Bypass Protection**
    - Implement strict server-side validation
    - Use whitelist approach for allowed inputs
    - Sanitize all user-provided data
3. **Query String Attacks**
    - Use CSRF tokens for sensitive actions
    - Avoid exposing sensitive data in URLs
    - Implement proper session management
4. **Cookies Protection**
    - Use HttpOnly and Secure flags
    - Implement token-based authentication
    - Set appropriate SameSite attributes
5. **Hidden Fields**
    - Never store sensitive information in hidden fields
    - Treat hidden fields as user-provided input (validate/sanitize)
    - Use server-side session storage instead

## **Session Protection**

1. **Session Jumping Prevention**
    - Implement proper authorization checks
    - Regenerate session IDs after login
    - Set appropriate session timeouts
2. **CSRF Protection**
    - Generate unique tokens for each form/page
    - Expire tokens after use or time limit
    - Validate tokens on server-side
3. **Session Hijacking Prevention**
    - Bind sessions to IP addresses
    - Implement device fingerprinting
    - Use secure, random session IDs

## **Injection Protection**

1. **XSS Prevention**
    - Use **`htmlentities()`** for HTML output
    - Apply **`json_encode()`** for JSON data
    - Implement Content Security Policy (CSP)
2. **SQL Injection Protection**
    - Use prepared statements with parameterized queries
    - Implement ORM with built-in protection
    - Apply principle of least privilege for DB users
3. **Directory Traversal Prevention**
    - Validate file paths contain only alphanumeric chars
    - Use basename() to remove path components
    - Store files outside web root when possible


