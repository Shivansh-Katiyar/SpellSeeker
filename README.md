# 🎮 SPELLSEEKER  
*An engaging C++ terminal word-guessing game*

---

## 📖 Overview  
SPELLSEEKER is a text-based C++ game inspired by Hangman. It challenges players to guess hidden words using limited lives and strategic hints—perfect for vocabulary enhancement or casual fun.

---

## 🎯 Motivation  
This project serves as a compact demonstration of:
- File-based word selection  
- Object-oriented design in C++  
- Terminal UI with color and masked input  
It’s lightweight yet modular—ideal for learning and expansion.

---

## ✨ Features  
- **Multi-mode gameplay**:  
  - *Arcade*: 5 ascending difficulty levels (Very Easy → Very Hard)  
  - *Survival*: Endless words until lives run out  
  - *Multiplayer*: Two-player turn-based guessing  
- **Visual UI**: Lives shown as heart icons (♥), colorful feedback  
- **Hints**: After two wrong guesses  
- **Score & progression**: Level unlocking & high-score tracking  
- **Hidden input**: Secure word entry in multiplayer (via `_getch()`)  
- **Scalable design**: Add or adjust word lists easily

---

## 🕹️ Usage  
1. **Select mode**:
   - `1` → Arcade  
   - `2` → Survival  
   - `3` → Multiplayer  
2. **Guess letters** to reveal the word  
   - Every incorrect guess costs a life  
   - Every two wrong guesses triggers a hint  
3. **Win conditions**:
   - Arcade: Complete all levels  
   - Survival: Last until lives drop to zero  
   - Multiplayer: Higher score after set rounds

---

## 📁 Project Structure  
SPELLSEEKER/
│
├── game_sc.cpp                # Game source code
├── README.md               # Project documentation
├── Very Easy.csv           # Level 1 word database
├── Easy.csv                # Level 2 word database
├── Medium.csv              # Level 3 word database
├── Hard.csv                # Level 4 word database
├── Very Hard.csv           # Level 5 word database
├── Survival_Database.csv   # Random words for Survival mode


---

## 🧩 Architecture & Design  
The game follows a modular OOP framework:
- **File Loading**: Reads and parses CSV files per mode/level  
- **Game Flow**: Main loop branches by mode, managing lives, hints, and scoring  
- **Hidden Input**: `_getch()` from `conio.h` hides multiplayer entries  
- **Display Layer**: ANSI color codes and heart icons enhance feedback

---

## 🛠️ Under the Hood  
* C++ STL: `ifstream`, `vector`, `string`, `srand()`  
* Input masking: `_getch()` for secret word entry  
* Terminal UI: ANSI codes for colored text output  
* Scoring: Lives-based and completion-based scoring models  
* Data-driven: Word pools defined externally in CSV files

---

## 🔭 Roadmap  
- 🎨 Cross-platform support (Linux/macOS input handling)  
- 🌐 UI layers (menu navigation, ASCII art)  
- 🌟 Word frequency scoring  
- 📦 Dedicated game library for reuse in other projects  
- 🧪 Unit tests for core logic

---

## 🤝 Acknowledgements  
- Inspired by classic word games and Hangman-style logic  
- Special thanks to educational resources on C++ OOP and terminal UI

