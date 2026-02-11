# EPITECH C++ Coding Style Checker - YUM/DNF Repository

This repository hosts RPM packages for the EPITECH C++ Coding Style Checker.

## Installation

### Fedora/RHEL/CentOS

1. Add the repository:

```bash
sudo tee /etc/yum.repos.d/cpp-checker.repo << 'REPO_EOF'
[cpp-checker]
name=EPITECH C++ Coding Style Checker
baseurl=https://philibertg.github.io/cpp-checker-rpm-repo
enabled=1
gpgcheck=0
REPO_EOF
```

2. Install the package:

```bash
sudo dnf install cpp-coding-style-checker
```

3. Update the package:

```bash
sudo dnf upgrade cpp-coding-style-checker
```

## Requirements

- Docker or Podman
- Fedora 38+, RHEL 8+, CentOS 8+, AlmaLinux 8+, Rocky Linux 8+

## Usage

After installation, run:

```bash
cpp-coding-style-checker /path/to/project
cpp-coding-style-checker .  # Check current directory
```