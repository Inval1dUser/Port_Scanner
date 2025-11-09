# Port Scanner

A simple, minimal CLI port scanner written in Python.
This repository provides a lightweight proof-of-concept scanner for learning and local testing. Use only on hosts and networks you own or have explicit permission to scan. ([GitHub][1])

## Features

* Single-host TCP port scanning.
* Range and single-port support (example flags shown).
* Fast configurable timeout and concurrency hints.
* Minimal dependencies. Designed for learning and demonstrations.

## Warning — Legal & Ethical

Port scanning can be considered intrusive. Only scan hosts you own or are explicitly authorized to test. The author and this repository accept no liability for misuse.

## Requirements

* Python 3.8+ (installed on most systems)
* (Optional) `pip` for installing dev/test tools

## Installation (example)

Clone the repo and run with Python:

```bash
   git clone https://github.com/Inval1dUser/spscan.git
   cd spscan
   # Optionally create a virtual environment
   python -m venv .venv
```

build the package

```bash
   pip install --upgrade build
   python -m build
```

install

```bash
   pip install --force-reinstall dist/spscan-0.1.0-py3-none-any.whl
```

## Usage (example)

The exact CLI flags depend on the implementation. Below are safe example usages you can adapt.

Scan a single host for common ports:

```bash
   spscan 127.0.0.1--ports 20-1024
```

Quick scan with a short timeout:

```bash
   python -m port_scanner --host 10.0.0.5 --ports 1-1024 --timeout 0.5
```

## Example output

```
Scanning 192.0.2.10 ports 1-1024
Open: 22/tcp   (ssh)
Open: 80/tcp   (http)
Closed: 23/tcp
Scan complete. 2 open ports found.
```

## Contributing

1. Fork the repo.
2. Create a feature branch.
3. Open a clear PR with motivation and test(s).
4. Keep changes focused and documented.

