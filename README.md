# uvalues

A CLI tool that extracts unique values from a column in a CSV file. Navigate headers with arrow keys and get a sorted list of every distinct value in the selected column.

## Installation

1. Clone the repo:

```bash
git clone https://github.com/breaker05/uniquevalues.git
cd uniquevalues
```

2. Make the script executable:

```bash
chmod +x uvalues
```

3. Create `~/bin` (if it doesn't exist) and symlink the script:

```bash
mkdir -p ~/bin
ln -s "$(pwd)/uvalues" ~/bin/uvalues
```

4. Make sure `~/bin` is in your PATH. Add this line to your `~/.zshrc` or `~/.bashrc` if it isn't already:

```bash
export PATH="$HOME/bin:$PATH"
```

Then reload your shell:

```bash
source ~/.zshrc
```

## Usage

From any directory, run:

```bash
uvalues <file.csv>
```

1. An interactive selector appears with all column headers
2. Use **↑/↓** arrow keys to highlight a column
3. Press **Enter** to confirm (or **Esc** / **Ctrl-C** to cancel)
4. All unique values in that column are printed, sorted alphabetically

## Example

```
$ uvalues data.csv

Select a column (↑/↓ to move, Enter to confirm):

    Name
  > Department
    Location

Unique values in 'Department' (4):

  Engineering
  Marketing
  Operations
  Sales
```

## Requirements

- Python 3 (uses only the standard library — no dependencies to install)
- A Unix-like terminal (macOS, Linux) for arrow key support
