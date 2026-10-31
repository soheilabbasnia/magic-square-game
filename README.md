# Magic Square Game

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Language: C#](https://img.shields.io/badge/Language-C%23-239120.svg?logo=csharp&logoColor=white)](https://docs.microsoft.com/en-us/dotnet/csharp/)
[![Framework: .NET WinForms](https://img.shields.io/badge/Framework-.NET%20Windows%20Forms-512BD4.svg?logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![Platform: Windows](https://img.shields.io/badge/Platform-Windows-0078D6.svg?logo=windows&logoColor=white)](https://www.microsoft.com/windows)

English | [فارسی](README_FA.md)

An interactive, graphical 3x3 **Magic Square** puzzle game and mathematical solver built with **C#** and **.NET Windows Forms**.

---

## Overview

A **Magic Square** is an $n \times n$ arrangement of distinct positive integers such that the sum of the integers in each row, each column, and both main diagonals equals the same constant magic number (for a $3 \times 3$ grid using numbers $1$ through $9$, the magic sum is **15**).

This desktop application provides an intuitive graphical interface for players to test their mathematical intuition and problem-solving skills, with built-in instant validation and an automatic backtracking solver.

Key highlights:
- **Interactive Gameplay**: Visual 3x3 numeric grid with real-time feedback.
- **Strict Input Validation**: Prevents duplicate numbers, out-of-range values ($<1$ or $>9$), and non-digit keystrokes.
- **Instant Solution Verification**: Checks row sums, column sums, and both diagonals against the target sum of 15.
- **Built-in Smart Solver**: Features an automated solver that computes and fills a valid magic square configuration at the click of a button.

---

## Rules of the Game

1. The grid consists of $3 \times 3$ cells (9 cells total).
2. Each cell must contain a distinct integer between **1** and **9** (no duplicates).
3. The sum of every row, column, and diagonal must equal **15**:
   $$\sum \text{Row} = \sum \text{Col} = \sum \text{Diagonal} = 15$$

---

## Getting Started

### Prerequisites

- Windows 10 / 11
- [.NET Framework 4.7.2+](https://dotnet.microsoft.com/download)
- Visual Studio 2022 (with .NET desktop development workload) or Rider

### Build & Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/soheilabbasnia/magic-square-game.git
   cd magic-square-game
   ```

2. **Open in Visual Studio**:
   Open `magic-square-game.sln`.

3. **Build and Run**:
   Press `F5` or click **Start** to compile and run the application.

4. **Command Line Build (MSBuild)**:
   ```cmd
   msbuild magic-square-game.sln /p:Configuration=Release
   ```
   The executable will be located in `magic-square-game/bin/Release/magic-square-game.exe`.

---

## Project Structure

```text
magic-square-game/
├── magic-square-game/           # C# Windows Forms application source code
│   ├── Form1.cs                 # Game logic, input validation, and solver
│   ├── Form1.Designer.cs        # WinForms visual component layout
│   ├── Form1.resx               # Form resource file
│   ├── Program.cs               # Application entry point
│   └── magic-square-game.csproj # C# project configuration
├── magic-square-game.sln        # Visual Studio solution file
└── LICENSE                      # MIT License
```

---

## Contributing

Contributions, enhancements, and alternative algorithmic solvers are welcome!
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/n-by-n-solver`).
3. Commit your changes (`git commit -m 'Add support for 4x4 magic squares'`).
4. Push to the branch (`git push origin feature/n-by-n-solver`).
5. Open a Pull Request.

---

## License

This project is licensed under the [MIT License](LICENSE).
Open source and free for educational use.

