# Advent of Code Starter Repository

Easily set up a lightweight [Advent of Code](https://adventofcode.com) starter repository with utility scripts to fetch the puzzle description and input data, while maintaining folder organization across different programming languages.

## Prerequisites

- **`curl`**: Required for fetching puzzle and input files.
- **Advent of Code Session Cookie**: You must have your Advent of Code session cookie value set as an environment variable `AOC_SESSION`. This is essential for authentication with the Advent of Code website to download puzzle inputs.
- **`pandoc` (optional)**: Used for converting the HTML puzzle description to Markdown format. Installation instructions can be found at [Pandoc's Installation Guide](https://pandoc.org/installing.html).

### Setting the Session Cookie

#### On Linux/macOS:

```bash
export AOC_SESSION="your_session_cookie_here"
```

#### On Windows (Command Prompt):

```cmd
set AOC_SESSION=your_session_cookie_here
```

Replace `your_session_cookie_here` with your actual session cookie value. **Note:** This setting persists only for the duration of the terminal session. Consider adding it to your profile or bashrc file for persistence.

## Getting Started

First, clone the repository and make the scripts executable:

```bash
git clone https://github.com/mertovun/aoc-starter.git
cd aoc-starter
chmod +x get start
```

### Downloading Puzzle Data

To download a specific day's puzzle and input:

```bash
./get <year> <day>
```

This downloads the Day `<day>` puzzle and input for year `<year>`, saving the puzzle in both HTML and Markdown formats (if `pandoc` is installed), and saving the input file in a directory structured like `./year/day/`.

### Setting Up a Language-specific Directory

Prepare a language-specific directory and starter file for coding:

```bash
./start <year> <day> <language>
```

This script fetches the puzzle and input for the specified year and day, moves them to a subdirectory named `/<language>`, and creates a `main.<language>` starter file. Replace `<year>`, `<day>`, and `<language>` with your desired values.

### Example

For a Python starter setup for December 1st, 2015:

```bash
./start 2015 1 py
cd 2015/1/py
```

Good Luck! 🎄

