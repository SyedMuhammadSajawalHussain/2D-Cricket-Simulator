# 🏏 Cricket Simulator - Console-Based Game

A comprehensive C++ console-based cricket simulation game that allows players to experience the thrill of cricket through random ball-by-ball action with ASCII animations.

---

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [How to Play](#how-to-play)
- [Game Mechanics](#game-mechanics)
- [Technical Details](#technical-details)
- [Installation & Setup](#installation--setup)
- [How to Run](#how-to-run)
- [Game Screenshots](#game-screenshots)
- [Developer Information](#developer-information)
- [License](#license)
- [Future Improvements](#future-improvements)

---

## 🎯 Overview

**Cricket Simulator** is a turn-based cricket simulation game built in C++ that simulates a complete cricket match between the player and the computer. The game features:
- Random ball-by-ball outcome generation
- ASCII art animations for different cricket shots
- Full match simulation with two innings
- Realistic cricket scoring system

---

## ✨ Features

### 🎮 Gameplay Features
- **Two-Inning Match**: Both player and computer get a chance to bat
- **Randomized Outcomes**: Each ball produces random results (0-6 runs, wicket, wide, no-ball)
- **Realistic Scoring**: Tracks runs, wickets, balls, and overs
- **ASCII Animations**: Visual representations of:
  - Six (6 runs)
  - Four (4 runs)
  - Single (1 run)
  - Double (2 runs)
  - Wicket/Out
  - No Ball
  - Wide Ball

### 📊 Statistics Tracking
- **Live Score Updates**: Runs, wickets, balls bowled
- **Player Tracking**: Number of players (wickets) fallen
- **Overs Counter**: Tracks overs bowled
- **Bowler Economy**: Basic bowling statistics

---

## 🎮 How to Play

### Game Flow

1. **Start the Game**
   - Enter the number of overs for the match
   - Game automatically sets up two innings

2. **First Innings (Your Batting)**
   - Press any key to "play" each ball
   - Random outcomes determine your score
   - Continue until all overs are bowled or all players are out

3. **Second Innings (Computer Batting)**
   - Same process for the computer
   - The computer's score is generated randomly

4. **Result Declaration**
   - Game compares both scores
   - Declares winner, loser, or draw

### Controls
- Press any key to play each ball
- Follow on-screen prompts for actions
- No complex controls - simple and intuitive

---

## 📊 Game Mechanics

### Scoring System

| Outcome | Runs | Description |
|---------|------|-------------|
| Dot Ball | 0 | No run scored |
| Single | 1 | One run |
| Double | 2 | Two runs |
| Triple | 3 | Three runs |
| Four | 4 | Boundary |
| Five | 5 | Five runs |
| Six | 6 | Maximum runs |
| Wicket | 0 | Player dismissed |
| Wide | 1 | Extra run |
| No-Ball | 0 | No run (re-bowled) |

### Match Rules

- **Maximum Players**: 12 players (11 wickets)
- **Overs**: User-defined at start
- **Wicket Limit**: 10 wickets per innings
- **Wide/No-Ball**: Adds extra runs without consuming a legal ball
- **Target**: Second innings team needs to score 1 more run than the first

---

## 🛠️ Technical Details

### Dependencies
```cpp
#include <iostream>   // Input/Output operations
#include <cstdlib>    // Random number generation
#include <conio.h>    // Console I/O (Windows specific)
```

### Key Functions

| Function | Purpose |
|----------|---------|
| `six()` | Displays six-run animation |
| `four()` | Displays four-run animation |
| `single()` | Displays single-run animation |
| `dble()` | Displays double-run animation |
| `out()` | Displays wicket animation |
| `ball()` | Displays ball delivery animation |
| `nball()` | Displays no-ball animation |

### Random Generation
```cpp
int c = rand() % 9 + 1;  // Generates numbers 1-9
```

---

## 💻 Installation & Setup

### Prerequisites
- Windows Operating System (uses `conio.h`)
- C++ Compiler (MinGW, Visual Studio, or any C++ compiler)

### Download
1. Clone the repository or download the source code
2. Save as `cricket_simulator.cpp`

### Compilation

#### Using MinGW (Windows)
```bash
g++ cricket_simulator.cpp -o cricket_simulator.exe
```

#### Using Visual Studio
1. Create a new Console Application project
2. Add the source file
3. Build the solution (Ctrl+Shift+B)

#### Using Turbo C++ (Legacy)
```cpp
// Open the file in Turbo C++
// Press F9 to compile
// Press Ctrl+F9 to run
```

---

## 🚀 How to Run

### Option 1: Direct Execution
```bash
# On Windows
cricket_simulator.exe

# On Linux (with Wine)
wine cricket_simulator.exe
```

### Option 2: Run from IDE
1. Open in Visual Studio/Turbo C++/CodeBlocks
2. Click Run/Build
3. Follow console prompts

### Option 3: Command Line
```bash
g++ cricket_simulator.cpp -o cricket_simulator
./cricket_simulator
```

---

## 📸 Game Screenshots

### Main Menu
```
Developer:  Sajawal Bukhary
Contact:    0328-0841432
Soft-Type:  Cricket Simulator
Enter overs.
```

### In-Game Display
```
Balls.    5
Players.  3
Scores.   24
Enter for shot.
```

### Score Display
```
Balls.    120
Players.  10
Scores.   185
```

---

## 👨‍💻 Developer Information

**Developer:** Sajawal Bukhary  
**Contact:** 0328-0841432  
**Software Type:** Cricket Simulator (Console-Based)

---

## 📜 License

This project is licensed under the MIT License - see the LICENSE file for details.

```
MIT License

Copyright (c) 2024 Sajawal Bukhary

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:
```

---

## 🔮 Future Improvements

### Planned Features
- [ ] **Bowling Variations**: Add different bowling types (fast, spin, swing)
- [ ] **Player Selection**: Allow choosing team lineup
- [ ] **Scoreboard UI**: Enhanced visual score display
- [ ] **Sound Effects**: Add audio feedback for shots
- [ ] **Cross-Platform**: Make it compatible with Linux and Mac
- [ ] **Ball-by-Ball Commentary**: Text commentary for each ball
- [ ] **Statistics Dashboard**: Detailed match statistics
- [ ] **Multiplayer Mode**: Local multiplayer support
- [ ] **Save/Load Game**: Save match progress
- [ ] **Tournament Mode**: Multiple team tournament

### Technical Improvements
- [ ] Replace `conio.h` with cross-platform alternatives
- [ ] Use OOP principles for better code organization
- [ ] Add input validation for overs input
- [ ] Implement proper random seed initialization
- [ ] Create separate header files for better structure

---

## 🐛 Known Issues

1. **Windows Only**: Uses Windows-specific `conio.h` library
2. **Sleep Function**: Uses Windows-specific `sleep()` command
3. **Input Validation**: Lacks validation for overs input
4. **Random Seed**: No randomization seed set

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 Version History

- **v1.0.0** (Initial Release)
  - Basic cricket simulation
  - Two-inning match
  - ASCII animations
  - Random outcome generation

---

## 🙏 Acknowledgments

- Inspired by classic cricket simulation games
- ASCII art designed for retro gaming feel
- Special thanks to all cricket enthusiasts

---

## 📧 Contact

For questions, suggestions, or contributions:
- **Developer:** Sajawal Bukhary
- **Phone:** 0328-0841432

---

## ⭐ Support

If you like this project, please:
- Star the repository ⭐
- Share with your friends 📱
- Report issues 🐛
- Suggest features 💡

---

**Enjoy the Game! 🏏✨**

---

*This README was last updated on: 2026*

**Made with ❤️ for Cricket Lovers**
