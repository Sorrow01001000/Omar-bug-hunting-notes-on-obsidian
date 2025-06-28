
Advanced Programming Project:TypingSpeedTestGame Using JavaFx.
--------------------------------------------------

Typing Speed Test Game is a JavaFX-based typing game designed to test and improve a user's typing speed and accuracy. The game presents words one by one, and players must type them correctly within a time limit to earn points. It supports three difficulty modes: **Easy**, **Medium**, and **Hard**, which scale the score multiplier.

Features:
----------
- Player name input.

- Difficulty selection (Easy / Medium / Hard).

- Timer countdown.

- Score tracking with difficulty-based multiplier.

- Leaderboard system that saves scores to a file.

- Word loading by difficulty.

- Clean JavaFX interface.

-------------------------------------------------------------------------------
#### 🔹 `GameController.java`

**Purpose of this class:** Manages the core game logic — word display, score tracking, and timing.

**Key Features:**
- Loads words from `words.txt` by difficulty.

- Controls the game loop and timer.

- Calculates score with mode multiplier.

- Handles player input and word matching.

- Saves scores to `leaderboard.txt`.

**Example Code:**
![[Pasted image 20250526004641.png]]
![[Pasted image 20250526004808.png]]

-------------------------------------------------------------------------------
#### 🔹 `LeaderboardEntry.java`

**Purpose:** A simple model to hold leaderboard data for display.

**Key Features:**
- Stores rank, username, and score


**Example Code:**
![[Pasted image 20250526005046.png]]

-------------------------------------------------------------------------------

#### 🔹 `MainMenuController.java`

**Purpose:** Handles the main menu logic and difficulty selection.

**Key Features:**
- Takes username input

- Launches the game scene with selected difficulty

- Passes username and mode to `GameController`


**Example Code:**![[Pasted image 20250526010855.png]]


-------------------------------------------------------------------------------
🗂️ File Structure:
![[Pasted image 20250526011017.png]]

-------------------------------------------------------------------------------
Code Runs:

![[Pasted image 20250526011201.png]]

![[Pasted image 20250526011217.png]]

![[Pasted image 20250526011229.png]]

![[Pasted image 20250526011256.png]]

![[Pasted image 20250526011312.png]]


-------------------------------------------------------------------------------
Made by: Omar Radwan Mohammed Radwan Omar
ID: 20247502643
Course: Advanced Programming
Professor: Dr. Ahmed Mostafa

The Project Repository:
https://github.com/Sorrow01001000/TypingSpeedTestGame
