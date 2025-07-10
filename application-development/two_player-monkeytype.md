# Two-Player Monkeytype Clone

## Objective

Build a real-time two-player typing game inspired by Monkeytype. This application allows two users on separate devices to connect and compete simultaneously by typing a common prompt. The interface is clean and minimal, and the typing speed of both players is displayed at the end of a timed session.

## Key Features to Implement

### 1. Real-Time Two-Player Typing via WebSockets

**Functionality:**  
Enable two users to type simultaneously and view each other’s typing progress in real time.

**Requirements:**
- WebSocket-based communication between clients and server.
- Shared prompt for both players.
- Real-time syncing of typed characters.
- Typing area visually shows both players’ progress.

### 2. Multiplayer Session Management

**Functionality:**  
Facilitate pairing of two players into a typing session.

**Requirements:**
- Simple match-making or room code system.
- Each room supports exactly two players.
- Indication when both players are connected and ready.

### 3. 30-Second Timer

**Functionality:**  
Countdown timer starts when both players are ready.

**Requirements:**
- 30-second countdown displayed on screen.
- Prevent typing before timer starts.
- Disable input after timer ends.

### 4. Typing Speed Results

**Functionality:**  
Display results after the session ends.

**Requirements:**
- Calculate WPM (Words Per Minute) for each player.
- Display WPM on the results screen.
- Accuracy tracking is not required.

### 5. Clean and Minimal UI

**Functionality:**  
Ensure a smooth and distraction-free user experience.

**Requirements:**
- Responsive design.
- Elegant font, neutral color palette, and intuitive layout.
- Real-time indicators for opponent progress and session status.

