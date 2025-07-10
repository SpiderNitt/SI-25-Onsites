# Minesweeper with Powers

## Objective

The goal is to develop an enhanced version of the classic Minesweeper game that retains the original grid-based logic but introduces modern game mechanics and interactive elements. This includes power-ups, themes, sound effects, scoring history, and more to make gameplay more engaging and dynamic.

## Key Features to Implement

### 1. Classic Minesweeper Grid Mechanics

**Functionality:**  
Preserve the core gameplay rules of Minesweeper with a grid, bombs, and number indicators.

**Requirements:**
- Standard square grid with adjustable sizes (e.g., 9x9, 16x16).
- Randomly placed bombs.
- Cells display number of adjacent bombs.
- Left-click to reveal a cell, right-click to flag a cell.
- Game over on bomb click unless shield is available.

### 2. Timer and Reset Button

**Functionality:**  
Track the duration of each game session and allow users to restart.

**Requirements:**
- Timer starts on the first move.
- Display elapsed time in MM:SS format.
- Reset button to clear the board and restart the timer.

### 3. Power-Up: Shields

**Functionality:**  
Allow players to earn shields by reaching certain milestone scores, protecting them from one accidental bomb click.

**Requirements:**
- Milestones based on number of safe cells cleared or time.
- Players receive visual feedback when shield is earned/used.
- Shield prevents one game-over and clears the bombed cell instead.

### 4. Score Tracking & History

**Functionality:**  
Track and display scores from previous games.

**Requirements:**
- Maintain a history of recent games (score, time, difficulty).
- Option to view best time, highest score, and games played.
- Local storage or backend DB integration to persist history.

### 5. Bonus: Theming System

**Functionality:**  
Enhance visual engagement with switchable themes.

**Requirements:**
- Theme options: Classic, Horror, Cartoon, etc.
- Different background, UI skins, and icons per theme.
- Light/dark toggle (for Classic).

### 6. Bonus: Sound Effects

**Functionality:**  
Add immersive sound design for different interactions and themes.

**Requirements:**
- Sounds for cell reveal, flag, bomb, win, loss, and shield use.
- Theme-specific sound packs (e.g., spooky in Horror, fun in Cartoon).
- Volume control or mute toggle.

### 7. Difficulty Levels

**Functionality:**  
Allow players to select between Easy, Medium, or Hard.

**Requirements:**
- Easy: Smaller grid (e.g., 8x8), fewer bombs.
- Medium: Standard 16x16.
- Hard: Larger grid, more bombs.
- Difficulty affects scoring and milestone
