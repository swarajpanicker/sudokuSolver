# Sudoku Solver

A browser-based Sudoku puzzle solver and validator built as a single HTML file. It lets you enter puzzles manually, solve them with backtracking, validate conflicts, and import grids from CSV/XLSX files.

## Features

- Interactive 9x9 Sudoku grid
- Click-to-select cells and keyboard input
- Numpad for fast value entry
- Real-time conflict highlighting
- Candidate hints toggle
- Solver that finds up to 10 solutions
- Multiple-solution display with clickable previews
- Clear solved values and reset the board
- Import puzzles from `.csv` or `.xlsx` files
- Responsive UI for desktop and smaller screens

## Files

- `sudoku_solver.html` — complete application (HTML, CSS, and JavaScript in one file)

## How to Run

1. Open `sudoku_solver.html` in a browser.
2. Click a cell and enter numbers using the keyboard or on-screen numpad.
3. Click `Solve Puzzle` to generate a solution.

You can also open the file directly from your local filesystem without any build step.

## Usage

### Manual Entry
- Select any cell in the grid.
- Type a number from `1` to `9`.
- Use `Backspace`, `Delete`, or `0` to clear a value.
- Arrow keys move between cells.

### Validation
- Click `Validate` to check for duplicate values in rows, columns, and 3x3 boxes.
- Conflicting cells are highlighted in red.

### Hints
- Enable or disable candidate hints using the toggle in the side panel.
- These are possible valid values for empty cells.

### Importing a Puzzle
- Use the Excel import panel.
- Supported formats: `.csv` and `.xlsx`.
- Expected input format: a 9x9 grid with `0` or blank cells for empty spots.

Example CSV:

```csv
5,3,0,0,7,0,0,0,0
6,0,0,1,9,5,0,0,0
0,9,8,0,0,0,0,6,0
8,0,0,0,6,0,0,0,3
4,0,0,8,0,3,0,0,1
7,0,0,0,2,0,0,0,6
0,6,0,0,0,0,2,8,0
0,0,0,4,1,9,0,0,5
0,0,0,0,8,0,0,7,9
```

## Solver Behavior

The app uses recursive backtracking to search for valid solutions. It stops after finding up to 10 solutions and displays the first one on the board.

It enforces the standard Sudoku rules:
- Each row contains numbers 1–9 once
- Each column contains numbers 1–9 once
- Each 3x3 block contains numbers 1–9 once

## Notes

- A valid Sudoku puzzle generally needs at least 17 clues to be uniquely solvable.
- The solver can detect if a board has no valid solution.
- Multiple valid solutions are supported and shown in the solution panel.

## License

This project is provided as-is for educational and personal use. Add a license if you plan to distribute it publicly.

## Author

Built for quick Sudoku solving in the browser.
