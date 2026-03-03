# CDN Project (Go + Distributed Nodes)

## Overview

This project implements a simplified **Content Delivery Network (CDN)** in Go.

The system simulates distributed nodes that store and serve content across different servers.
It demonstrates core CDN concepts such as:

* Content distribution
* Node-based request handling
* Static file serving
* Network-based communication

The project is structured to illustrate how content can be replicated and served efficiently across multiple nodes.

---

## Architecture

The system follows a distributed node-based structure:

```text
Client
   ↓
CDN Node
   ↓
Local Storage
```

Multiple nodes can be run independently to simulate distributed content delivery.

Each node:

* Listens on a defined port
* Serves stored content
* Handles incoming HTTP requests
* Can replicate or retrieve content from other nodes

---

## Project Structure

```text
cdnproject-master/
│
├── cmd/
│   └── main.go
│
├── internal/
│   ├── node/
│   │   └── node.go
│   │
│   ├── storage/
│   │   └── storage.go
│   │
│   ├── network/
│   │   └── communication.go
│   │
│   └── handler/
│       └── http_handler.go
│
├── go.mod
└── go.sum
```

---

## Core Components

### 1. Node

Defined in:

```text
internal/node/
```

Responsible for:

* Initializing server
* Managing local storage
* Coordinating network communication
* Handling request routing

---

### 2. Storage Layer

Defined in:

```text
internal/storage/
```

Handles:

* File saving
* File retrieval
* Local content management

---

### 3. Network Communication

Defined in:

```text
internal/network/
```

Handles:

* Inter-node communication
* Content replication
* Remote content fetching

---

### 4. HTTP Handler

Defined in:

```text
internal/handler/
```

Handles:

* Incoming HTTP requests
* File serving
* Routing logic

---

## How to Run

### 1. Clone repository

```bash
git clone <your-repository-url>
cd cdnproject-master
```

### 2. Install dependencies

```bash
go mod tidy
```

### 3. Run a node

```bash
go run cmd/main.go
```

The server starts on the configured port defined in `main.go`.

To simulate multiple CDN nodes, run the service on different ports.

---

## CDN Functionality

The project demonstrates:

* Static content storage
* Distributed file serving
* Basic replication logic
* Node communication
* HTTP-based content access

---

## Technologies Used

* Go
* net/http
* Modular internal architecture
* Distributed system principles

---

## What This Project Demonstrates

* Distributed systems fundamentals
* CDN architecture basics
* HTTP server implementation in Go
* Inter-node communication
* Modular service design
