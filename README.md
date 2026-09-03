# Minesweeper

A desktop implementation of the classic Minesweeper game built with Java Swing.

The game features a randomly generated minefield, flagging, automatic revealing of empty areas, and win/loss detection.

## Features

- Classic Minesweeper gameplay
- Randomly generated mine placement
- Numbers indicating adjacent mines
- Recursive revealing of connected empty fields
- Flag and unflag suspected mines
- Remaining mine counter
- Win and loss detection
- Graphical desktop interface built with Java Swing
- Configurable board size and number of mines

## Gameplay

The default game uses a **16 × 16 grid with 40 mines**.

- **Left click** a field to reveal it
- **Right click** a field to place or remove a flag
- Revealing an empty field automatically reveals connected empty areas
- Revealing a mine ends the game
- The game is won when all non-mine fields have been discovered and the mines are correctly flagged

## Tech Stack

- Java
- Java Swing / AWT

No external libraries or frameworks are required.

## Project Structure

```text
Minesweeper/
├── src/
│   ├── Main.java        # Application entry point
│   ├── GamePanel.java   # UI and game interaction
│   └── Grid.java        # Mine placement and grid logic
└── resources/
```

## Getting Started

### Prerequisites

A Java Development Kit (JDK) must be installed.

Check your installation with:

```bash
java --version
javac --version
```

### Clone the Repository

```bash
git clone https://github.com/filipgrgic/Minesweeper.git
cd Minesweeper
```

### Compile

```bash
javac -d out src/*.java
```

### Run

```bash
java -cp out Main
```

Alternatively, open the project in a Java IDE such as IntelliJ IDEA and run `Main.java`.

## Configuration

The board dimensions and number of mines can be changed in `Main.java`.

The default configuration is:

```java
new GamePanel(16, 16, 40);
```

The constructor parameters represent:

```text
rows, columns, number of mines
```

## Implementation

The application is split into two main components:

- `Grid` manages the minefield, randomly places mines, and calculates the number of neighboring mines for every field.
- `GamePanel` provides the Swing-based user interface and handles revealing fields, placing flags, recursive empty-field discovery, and win/loss detection.
