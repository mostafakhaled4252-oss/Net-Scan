
# 🛡️ NET SCAN v2.0 - Professional Network & Port Scanner

An advanced, object-oriented network and port scanning utility built in Python. Designed specifically for security professionals and penetration testers to perform accurate, high-speed target analysis backed by stunning visual reports and robust audit logging.

---

## 🚀 Key Features

* **Object-Oriented Architecture (OOP):** Clean, modular, and maintainable code structure using classes.
* **High-Performance Multi-Threading:** Leverages `ThreadPoolExecutor` for lightning-fast concurrent port scanning.
* **Service Banner Grabbing:** Automatically extracts HTTP headers and service information from open ports.
* **Smart Offline Detection:** Automatically detects if an entire target host is offline/unreachable and skips lengthy closed-port readouts.
* **Batch Target Processing:** Scan multiple IP addresses easily by passing an external text file (`-f`).
* **Rich CLI Interface:** Beautiful colored tables, progress bars (`tqdm`), and an eye-catching ASCII art banner.
* **Audit Trail Logging:** Automatically records operational milestones, errors, and warnings into `cyber_log.txt`.
* **Professional Reporting:** Export scan results into structured **JSON** files and stunning dark-themed **HTML** security reports.

---

## 📦 Prerequisites & Dependencies

Make sure you have Python installed along with the required external libraries (`rich` and `tqdm`):

```bash
pip install rich tqdm

```

---

## ⚙️ Command-Line Arguments

| Flag | Argument | Description | Default |
| --- | --- | --- | --- |
| `-t` | `--target` | Target IP address or hostname | `127.0.0.1` |
| `-f` | `--file` | Text file containing a list of target IP addresses | `None` |
| `-s` | `--start` | Starting port number for the scan | `1` |
| `-e` | `--end` | Ending port number for the scan | `1024` |
| `--timeout` | `--timeout` | Connection timeout threshold in seconds | `0.5` |
| `--threads` | `--threads` | Number of concurrent execution threads | `100` |
| `--path` | `--path` | HTTP path to request for banner grabbing | `/` |
| `--common` | `--common` | Scan a curated list of common ports (80, 443, 8080, 623, 21, 22) | `False` |
| `--output` | `--output` | Filename to export scan results in JSON format | `None` |
| `--html` | `--html` | Filename to export a professional HTML security report | `None` |

---

## 💻 Usage Examples

### 1. Scan Common Ports on a Single Target with HTML & JSON Reports:

```bash
python ip_and_ports.py -t 192.168.1.1 --common --threads 150 --output report.json --html report.html

```

### 2. Batch Scan Multiple Targets from a Text File:

Create an `ips.txt` file containing your target IPs, then run:

```bash
python ip_and_ports.py --file ips.txt --common --threads 100 --html audit_report.html

```

---

## 📄 Output Files

* **`cyber_log.txt`**: Detailed background execution logs, timestamps, and error tracing.
* **`*.json`**: Structured raw data report for programmatic integration.
* **`*.html`**: Executive dark-themed security audit report ready for presentation.



*Developed as a professional security auditing tool.*
