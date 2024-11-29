# Multi-Threaded Web Server

This project is a multi-threaded web server implemented in Rust. It listens on port 7878 and uses a thread pool to handle incoming requests efficiently. The server is built using the following components:

- **ThreadPool**: Manages a pool of worker threads.
- **Worker**: Represents a single worker thread in the pool.
- **Channel**: Used for communication between the main thread and worker threads.
- **Jobs**: Represents the tasks that the workers execute.
- **Arc and Mutex**: Used to ensure safe sharing of data between threads.

## Features

- Multi-threaded request handling
- Efficient use of system resources
- Safe concurrency with `Arc` and `Mutex`

## Getting Started

### Prerequisites

- Rust installed on your system. You can download it from rust-lang.org.

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/tusharagrahari/Multi-Threaded-Web-Server.git
    cd Multi-Threaded-Web-Server
    ```

2. Build the project:
    ```sh
    cargo build
    ```

3. Run the server:
    ```sh
    cargo run
    ```

The server will start listening on `localhost:7878`.


## Project Structure
- src/main.rs: Entry point of the application.
- src/lib.rs: Contains the implementation of the ThreadPool, Worker, and job handling logic.
- src/worker.rs: Defines the Worker struct and its associated methods.
- src/thread_pool.rs: Defines the ThreadPool struct and its associated methods.
- src/job.rs: Defines the job struct and its associated methods.
