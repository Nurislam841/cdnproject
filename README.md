# CDN Project (Node.js)

## Overview

This project is a Node.js-based application that simulates a simplified **Content Delivery Network (CDN)**.

The application implements:

* HTTP server
* File storage management
* Node-to-node communication logic
* Request handling and routing
* Static file distribution

The goal of the project is to demonstrate the core mechanics behind content delivery and distributed file serving.

---

## Tech Stack

* Node.js
* Express (if used in project)
* Native `http` module (if implemented directly)
* File System (`fs`)
* Modular architecture using separate directories

---

## Project Structure

```
cdnproject-master/
│
├── index.js / server.js
├── package.json
├── routes/
├── controllers/
├── services/
├── storage/
└── utils/
```

*(Structure reflects modular separation found in the project.)*

---

## Core Components

### 1. Server Entry Point

Responsible for:

* Initializing the HTTP server
* Configuring routes
* Starting the application on a defined port

---

### 2. Routing Layer

Handles:

* Incoming HTTP requests
* File fetch requests
* Node communication endpoints

---

### 3. Storage Layer

Responsible for:

* Saving files locally
* Reading files from disk
* Managing file paths

Uses Node.js `fs` module.

---

### 4. CDN Logic

Implements:

* File retrieval from local storage
* Forwarding requests to other nodes (if applicable)
* Returning file responses to client

---

## How to Run

### 1. Install dependencies

```bash
npm install
```

### 2. Start the server

```bash
node index.js
```

or

```bash
npm start
```

Server runs on the port defined in the main file (commonly 3000 or 5000).

---

## Features

* HTTP-based file serving
* Modular structure
* Local file storage management
* Simulated distributed node behavior
* Basic CDN-style request handling

---

## Educational Purpose

This project demonstrates:

* Building an HTTP server in Node.js
* Structuring a backend project
* Implementing file storage logic
* Simulating distributed content delivery
* Designing modular server-side architecture
