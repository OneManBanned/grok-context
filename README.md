# grok-context

A Bash script that recursively scans a directory, outputs relative file paths and contents to `context.txt` in the input directory, and respects `.grokignore` exclusions using `.gitignore`-style patterns.

## Features
- Outputs file names (relative to input directory) and contents to `context.txt`.
- Excludes files/directories via `.grokignore` (e.g., `node_modules/`, `*.txt`).
- Overwrites `context.txt` each run.
- Validates directory and write permissions.

## Installation
1. Download:
   ```bash
   curl -o ~/.local/bin/grok-context https://raw.githubusercontent.com/OneManBanned/grok-context/main/grok-context

2. Make executable:

   chmod +x ~/.local/bin/grok-context

## Requires
bash, find, realpath/readlink (install coreutils if needed).

## Usage

grok-context [directory]

Defaults to current directory if none specified. Creates context.txt in the input directory.
Place .grokignore file in target [directory] using .gitignore-style patterns

##Example Output

File: src/main.js
console.log("Hello, world!");

File: lib/utils.js
function add(a, b) { return a + b; }

