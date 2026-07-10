# Big Data Log Harvester System

## Project Overview
The Big Data Log Harvester System is a Python-based application that collects log data from multiple simulated branch servers using TCP socket communication. The received logs are validated, converted into structured binary records, and stored in dynamically created partition files based on branch and log severity.

## Objectives
- Simulate multiple branch log servers.
- Collect logs using TCP sockets.
- Validate log entries using Regular Expressions.
- Store logs in binary format.
- Dynamically partition logs by branch and severity.
- Read and decode binary log files.

## Project Files

| File Name | Description |
|-----------|-------------|
| log_server_simulator.py | Simulates multiple branch servers and continuously sends log messages. |
| log_harvester_daemon.py | Connects to all servers, validates logs, and stores them into binary partition files. |
| read_binary_logs.py | Reads binary partition files and converts them into readable log records. |

## Technologies Used
- Python 3.x
- Socket Programming
- Multi-threading
- Regular Expressions (Regex)
- Binary File Handling
- Struct Module

## Features
- Multi-threaded log collection
- TCP socket communication
- Real-time log processing
- Regex-based validation
- Binary data storage
- Dynamic partition creation
- Binary log reader
- Live statistics monitoring

## Project Workflow

1. Start the Log Server Simulator.
2. Run the Log Harvester Daemon.
3. Logs are received through TCP sockets.
4. Valid logs are converted into structured binary records.
5. Binary records are stored inside the `partitions` folder.
6. Use the Binary Log Reader to decode and display stored logs.

## How to Run

### Step 1
Run the server simulator.

```bash
python log_server_simulator.py
```

### Step 2
Open another terminal and run:

```bash
python log_harvester_daemon.py
```

### Step 3
After partition files are created, read them using:

```bash
python read_binary_logs.py partitions/swiggy-chennai_INFO.bin
```

## Output

- Live log collection
- Binary partition files
- Decoded readable log records
- Real-time statistics

## Folder Structure

```
Big Data/
│
├── log_server_simulator.py
├── log_harvester_daemon.py
├── read_binary_logs.py
├── partitions/
│   ├── swiggy-chennai_INFO.bin
│   ├── swiggy-chennai_ERROR.bin
│   ├── swiggy-bangalore_INFO.bin
│   └── ...
└── README.md
```

## Future Enhancements

- Database integration
- Dashboard for live monitoring
- Log compression
- Cloud storage support
- Web-based log viewer

## Developed By

**S. Brindha**

Bachelor of Computer Applications (BCA)

Kamaraj College

Academic Year: 2026
