# CTF: Modern Flag Extraction & Formatting Tool
#### Accelerate Your Capture The Flag Challenges with Precision and Efficiency

## Overview

**CTF** is a cutting-edge command-line utility designed to streamline the extraction, formatting, and management of flags during Capture The Flag (CTF) competitions and cybersecurity challenges. Built with modern software engineering principles, CTF supports major platforms such as picoCTF and TryHackMe out-of-the-box—and can be easily extended with custom regular expressions to handle flags from any source.

## Key Features

- **Automated Flag Extraction:**  
  Built-in regex patterns for popular platforms:
  - **picoCTF:** `picoCTF\{[^}]+\}`
  - **TryHackMe:** `THM\{[^}]+\}`

- **Flag Formatting:**  
  Automatically standardizes flag output (e.g., trimming spaces, enforcing uppercase) for consistent submissions.

- **Customizable and Extensible:**  
  Users can override default regex patterns via a configuration file (`ctf.conf`) and extend functionality through a modular design.

- **In-Tool Documentation:**  
  Comprehensive help is available directly within the tool—simply run `./ctf.sh help` for detailed usage instructions.

- **Integration Ready:**  
  Ideal for both interactive use and automated pipelines, making it perfect for practice sessions and competitive environments.

- **Enhanced Logging and Debugging:**  
  A verbose mode provides detailed logs to assist in troubleshooting flag extraction issues.

## Usage

Display the help information:
```bash
./ctf.sh help
```

Commands
find
Extract flags from input using default or custom regex patterns.

Examples:
``` bash
# Extract flags from a file using default patterns:
./ctf.sh find --file challenge.txt

# Extract flags from a text string:
./ctf.sh find "Some text with picoCTF{example_flag} inside."

# Use a custom regex pattern:
./ctf.sh find --regex "CUSTOM\{[A-Za-z0-9_-]+\}" "Custom flag text."
```
