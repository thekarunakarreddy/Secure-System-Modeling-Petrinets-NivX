# NivX Car Rental System - Petri Nets Analysis

## Overview

This repository contains the formal specification and analysis of **NivX**, a secure web-based car rental platform using Petri Nets. The project demonstrates the application of formal methods for modeling, verifying, and analyzing concurrent system behaviors in a secure car rental application.

## Table of Contents

- [System Specification](#system-specification)
- [System Design](#system-design)
- [Petri Nets Models](#petri-nets-models)
- [Verification and Analysis](#verification-and-analysis)
- [Implementation](#implementation)
- [Security Mechanisms](#security-mechanisms)
- [Testing](#testing)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## System Specification

### Overview
NivX is a comprehensive car rental platform designed to deliver users a seamless, secure, and efficient experience for exploring, reserving, and managing car rentals. The system balances functionality, usability, and security while complying with rigorous security standards.

### Functional Requirements

| Category | Requirement |
|----------|-------------|
| **User Registration & Authentication** | - Account creation with name, email, and password<br>- Secure login with password hashing<br>- Session management<br>- Password recovery functionality |
| **Browsing & Searching** | - Browse cars by category (SUV, sedan, etc.)<br>- Search with filters (price, availability, features)<br>- Display rental rates and specifications |
| **Booking & Extras** | - Book cars with rental dates<br>- Add additional services (GPS, insurance)<br>- Review booking details before confirmation |
| **Payment Processing** | - Secure payment gateway integration<br>- Multiple payment methods<br>- Transaction logs and confirmations |
| **Account Management** | - Profile management<br>- Booking modifications and cancellations<br>- Password updates |

### Non-Functional Requirements

- **Security**: Protection against SQL injection, XSS, and CSRF
- **Performance**: Support for concurrent users with optimized load times
- **Reliability**: Fault-tolerant mechanisms and error handling
- **Usability**: Intuitive interface with accessibility features
- **Scalability**: Modular design for easy maintenance and growth

## System Design

### Architecture
The system follows secure design principles including:
- **Defense in Depth**: Multiple security layers
- **Least Privilege**: Minimal access rights
- **Security by Default**: Secure initial configurations
- **Input Validation**: Protection against malicious inputs

### Wireframes
1. **Login Page**: Secure user authentication interface
2. **Car Search & Browse**: Vehicle discovery with filtering
3. **Content Description**: Detailed car information
4. **Order List**: Booking management interface
5. **Order Confirmation**: Transaction completion

## Petri Nets Models

This project uses Petri Nets to formally model three critical system behaviors:

### Model 1: Cookie State Management for Cart Updates
- **Purpose**: Models session state management during cart operations
- **Components**: Session validation, cart state updates, cookie management
- **Verification**: Ensures data consistency and session integrity

### Model 2: Asynchronous API Call Handling and Response Processing
- **Purpose**: Models concurrent API request handling
- **Components**: Request queuing, processing, response management
- **Verification**: Prevents race conditions and ensures proper error handling

### Model 3: Cart Item Selection and DOM Updates
- **Purpose**: Models user interface interactions and updates
- **Components**: Item selection, DOM manipulation, state synchronization
- **Verification**: Ensures UI consistency and proper event handling

## Verification and Analysis

### Verification Tools
- **CTL (Computation Tree Logic)**: For property verification
- **Reachability Analysis**: For deadlock detection
- **State Space Analysis**: For behavior validation

### System Properties Verified
1. **Safety Properties**: No deadlocks or race conditions
2. **Liveness Properties**: System progress and responsiveness
3. **Security Properties**: Data integrity and access control
4. **Consistency Properties**: State synchronization across components

### CTL Properties Examples
```
AG(request_sent → AF response_received)
AG(cart_updated → session_valid)
AG(payment_initiated → AF(payment_completed ∨ payment_failed))
```

## Implementation

### Security Mechanisms
- **Authentication**: Secure password hashing and session management
- **Authorization**: Role-based access control (RBAC)
- **Data Encryption**: TLS for transmission, encryption for storage
- **Input Validation**: Protection against injection attacks
- **Session Security**: Secure cookies with HTTP-only flags
- **Access Control**: Principle of least privilege

### Technology Stack
- **Frontend**: HTML5, CSS3, JavaScript
- **Backend**: Secure server-side processing
- **Database**: Encrypted data storage
- **Security**: HTTPS, TLS encryption, secure headers

## Testing

### Testing Approaches
- **Static Analysis**: Code review and vulnerability scanning
- **Dynamic Analysis**: Runtime behavior testing
- **Penetration Testing**: Security vulnerability assessment
- **Coverage Analysis**: Comprehensive test coverage metrics

### Problem Resolution
- Systematic debugging and issue tracking
- Security vulnerability patches
- Performance optimization
- Compliance validation


## Usage

1. **User Registration**: Create an account with secure credentials
2. **Browse Vehicles**: Search and filter available cars
3. **Make Booking**: Select dates and additional services
4. **Payment**: Complete secure transaction
5. **Manage Booking**: View and modify reservations

## Security Best Practices

- All user inputs are validated and sanitized
- HTTPS is enforced for all communications
- Session timeouts prevent unauthorized access
- Regular security audits and updates
- Compliance with security standards

## Formal Methods Benefits

The use of Petri Nets in this project provides:
- **Ambiguity Elimination**: Clear, unambiguous system specification
- **Early Error Detection**: Design flaws identified before implementation
- **Property Verification**: Mathematical proof of system correctness
- **Security Validation**: Formal verification of security properties

## Strengths

- Comprehensive security implementation
- Formal verification of critical behaviors
- Scalable and maintainable architecture
- User-friendly interface design
- Robust error handling

## Limitations

- Complexity of formal modeling for large systems
- Performance overhead of security mechanisms
- Learning curve for formal methods
- Maintenance of formal specifications

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## References

- Centers for Medicare & Medicaid Services. (n.d). System Development Life Cycle
- Formal Methods in Software Engineering
- Petri Nets: Properties, Analysis and Applications
- Security Engineering Best Practices

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Contact

**Karunakar Reddy Machupalli**  
Student ID: N1334679  
Email: karunakarreddy2277@gmaill.com

---

*This project was developed as part of SOFT40171 - Design & Development of Secure Systems coursework, demonstrating the application of formal methods in secure system design.*
