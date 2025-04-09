# Intro to Web Services Oriented and Service Oriented Architecture

## Services

- Actions that help fulfill a *task*.

## Monolithic Computing

### Single-user Monolithic Computing

- Not connected to any network.
- Used by only one user at a time.
- Only uses resources within its *immediate* access.

### Multi-user Monolithic Computing

- Share resources using **timesharing**.
- A <span class="spurious-link"
  target="Mainframe Computers">***mainframe***</span> is used.
  - Accessed through **terminals** (keyboard and monitor)

1.  Mainframe Computers

    - Multi-user
    - Multi-programming
    - High performance

## Types of Computer Networks

1.  Personal Area Network (PAN or WPAN)
2.  Body Area Network (BAN)
    - Wearable or implantable
3.  Local Area Network (LAN)
    - Ethernet (10 Mbps)
    - Fast Ethernet (100 Mbps)
    - Gigabit Ethernet (1000 Mbps)
    - Wifi
4.  Campus Area Network (CAN)
5.  Metropolitan Area Network (MAN)
    - Usually established with optical fiber.
6.  Wide Area Network (WAN)
7.  Internet

## Distributed System

> Multiple software components that are on multiple computers but run as
> a single system.

- or Distributed Computing
- Collection of independent components (nodes)
  - Communicate and coordinate actions
- Appears as a single coherent system
  - Nodes can fail independently
- Can accept more requests and perform more jobs than a standard system

# Service Oriented Architecture

- Uses the *find-bind-execute*
  - Providers register service
  - Consumer searches registry
  - Registry contracts consumer for service

### Core Principles

- Reusability
- Composability
- Interopability
- Loose Coupling
- Autonomy

### Advantages

- Ease of integration
- Improved Flexibility
- Managed Complexity
- Platform Independence
- Loose Coupling
- Parallel Development
- Available
- Reliable
- Cost Efficiency

### Challenges

- Complexity
- Performance Overhead
- Service Discoverability
- Service Versioning and Backward Compatibility

### Components

1.  Functional Aspects

    - Transport
    - Service Communication Protocol
    - Service Description
    - Service
    - Business Process
    - Service Registry

2.  Quality of Service Aspects

    - Policy
    - Security
    - Transaction
    - Management

# Web Services

- Services that communicate over the WWW HTTP.
- *code on demand*
- A function or method we can call by sending an *HTTP request* to a
  URL.
  - The service returns the result back as a *response*.
- Platform independent

## Benefits

- Exposing the existing function on the network
- Interopability
- Standardized protocol
- Low cost communication

## Simple Object Access Protocol (`SOAP`)

- Is a protocol
- Traditional/**OLD**
- `XML`-based.
- Structured but complex
- Uses `WSDL` for describing functionalities (documentation)
  - <span class="spurious-link"
    target="Web Services Description Language (=WSDL=)">**Web Services
    Description Language**</span>
- Often used in <u>enterprise applications</u> where reliability and
  security are critical.

### Web Services Description Language (`WSDL`)

- Developed jointly by Microsoft and IBM.
- Integral part of <span class="spurious-link"
  target="Universal Description, Discovery, and Integration (=UDDI=)">*`UDDI`*</span>
- Describe the structure and behavior of `SOAP`-based web services

1.  Universal Description, Discovery, and Integration (`UDDI`)

    - Registry for web services
    - Also a specification standard

### Advantages

- `WS Security`
  - `SOAP` defines its own security.
- Platform independent

### Disadvantages

- Slow
  - Because of `XML` parsing
  - Consumes more bandwidth and resource
- `WSDL` dependent

## Representational State Transfer API (`REST`)

- Is an architectural style.
- Modern APIs, mobile apps
- Uses `JSON` and sometimes `XML`.
- Simple and lightweight
- Use `HTTP` requests
  - `GET`
  - `POST`
  - `PUT`
  - `DELETE`

### Advantages

- Efficient/Fast
- Language/Platform independent
- Flexible

# Web Services Architecture

## Four main layers

### Service Transport

- `HTTP`

### Messaging Layer

- `SOAP` or `REST` API

### Service Description

- `WSDL/UDDI` or `OpenAPI` (Swagger)

### Service Discovery

- `UDDI`
- Eureka (Spring Cloud Netflix)
- Consul (HashiCorp)
- Zookeeper (Apache)
- Kubernetes Service Discovery
- API Gateway
  - AWS
  - Kong
  - Apigee (Google Cloud)
  - Azure API Management
