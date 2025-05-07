# IDME Tool

```
██╗██████╗ ███╗   ███╗███████╗
██║██╔══██╗████╗ ████║██╔════╝
██║██║  ██║██╔████╔██║█████╗  
██║██║  ██║██║╚██╔╝██║██╔══╝  
██║██████╔╝██║ ╚═╝ ██║███████╗
╚═╝╚═════╝ ╚═╝     ╚═╝╚══════╝
```

## Overview

IDME is a simple yet powerful command-line utility for Linux system administrators to quickly switch between users that own specific domain directories. Perfect for web hosting environments where you need to manage multiple domain users.

**Website**: [truconfig.com/idme](https://truconfig.com/idme)

## Features

- **Quick User Switching**: Easily switch to the user who owns a domain directory
- **Tab Completion**: Built-in tab completion for domain names
- **Cross-Distribution Support**: Works on AlmaLinux, CentOS, Ubuntu, and other popular Linux distributions
- **Automatic Setup**: One-command installation with `idme setup`

## Usage

```bash
# Show a simple greeting (testing the installation)
idme hello

# Set up the command and tab completion
idme setup

# Switch to the user who owns the domain directory
idme domainname.com

# Show help and usage information
idme
```

## Tab Completion

The tool supports tab completion for domain names in `/home/`:

```bash
# Type a partial domain name and press Tab
idme domain<TAB>

# Will complete to
idme domainname.com
```

## Installation

1. Clone the repository or copy the script to `/root/idme/`
2. Run the setup command:

```bash
idme setup
```

This will:
- Make the script executable
- Create a symlink in `/usr/local/bin/`
- Set up tab completion
- Configure system-wide loading of the completion script

## Troubleshooting

If tab completion isn't working, you can:

1. Open a new terminal window
2. Run: `source /etc/bash_completion.d/idme`
3. Log out and log back in

## System Requirements

- Bash shell
- Root privileges for installation
- `/home` directory structure with domain folders

## License

MIT License

Copyright (c) 2025 truconfig.com

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.