# Kelper Execution Suite

Kelper is a lightweight, high-performance Luau script execution environment and injection framework designed for security research, environment analysis, and custom runtime execution.

## Features

* **Advanced Bootstrapper:** Automated, lightweight deployment cycle with memory-efficient process synchronization.
* **Isolated Runtime Environment:** Implements secure directory allocation using randomized identifiers to prevent cross-process workspace conflicts.
* **Optimized Dynamic Downloader:** Integrated asynchronous network layer utilizing reusable HTTP clients for reliable payload fetching.
* **Luau Compatibility:** Full support for extended Luau environments, complex script structures, and custom function routing.

## Architecture & Deployment

The suite utilizes a discrete two-stage deployment system:
1. **The Bootstrapper:** Manages updates, verifies integrity signatures, structures the temporary virtual environment, and handles secure post-execution cleanup.
2. **The Core Module:** The primary execution engine that interfaces with the target architecture to host the scripting runtime.

## Building from Source

### Prerequisites
* .NET 8.0 SDK or higher
* Visual Studio Code / Visual Studio 2022

### Compilation
To compile the single-file autonomous deployment binary, execute the following command in your terminal:

```bash
dotnet publish -c Release
