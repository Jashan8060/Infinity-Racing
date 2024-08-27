# 2D Infinite Racing Game in Scratch

Welcome to the 2D Infinite Racing Game! This game was created using Scratch as a part of Week 0 "Starting from Scratch" of Harvard University's CS50’s Introduction to Computer Science course. It features a racing experience with randomly appearing cars that continuously move down the screen.

## Game Overview

In this 2D infinite racing game, players will:
- Select their car from a choice of 7 different car designs.
- Press the space bar to start the game.
- Watch as cars appear randomly from the top of the screen and move downwards.
- Aim to achieve the highest score possible.

## Features

- **Car Selection:** Players choose a car from a variety of options.
- **Infinite Racing:** Cars appear randomly in both left and right lanes and move continuously down the screen.
- **Random Costumes:** Each car that appears has a randomly selected design.
- **Score Tracking:** Score increments every 0.5 seconds, keeping track of the player’s performance.
- **Speed Variable:** Adjusts the difficulty by changing the car's movement speed.

## How to Play

1. **Start the Game:**
   - Click the green flag to begin.
   - **Choose Your Car:**
     - Select your car from the available options (Enter a number from 1 to 7 and press enter).

2. **Begin Racing:**
   - Press the space bar to start the game.
   - Cars will start appearing at the top of the screen and move downwards.

## Game Mechanics

- **Car Movement:**
  - Cars spawn at coordinates `x: -37`, `y: 25` and move downwards until they exit the screen.
  - Each car is given a random costume from 7 available options.
  - Cars are created as clones, allowing multiple cars to appear and move independently.

- **Cloning and Timing:**
  - New cars are spawned every `x` seconds, where `x` is a variable that takes a random value from 4 to 8. This randomness makes the game more dynamic.
  - The previous car continues moving down the screen while new cars appear.

- **Score Variable:**
  - The score starts at 0 and increments by 1 every 0.5 seconds.
  - The game keeps track of the highest score achieved during the session.

- **Speed Variable:**
  - The speed variable starts at `-1`, representing the initial movement speed of the cars.
  - The speed changes by `0.4` every 3 seconds, increasing the difficulty as the game progresses.
  - The speed variable can be adjusted to make the game easier or more challenging.

## Implementation Details

### Car Selection

The game prompts the player to choose a car and sets the chosen car as the sprite's costume. This selection is handled through a variable that updates the costume based on user input.

### Cloning and Movement

- **Car Cloning:** 
  - Uses the `create clone of [myself]` block to generate new car instances.
  - Each clone moves independently down the screen.

- **Movement Script:**
  - Each clone moves down until its `y` position is less than `-470`.
  - The speed of the car’s movement is controlled by the `speed` variable, which changes over time to adjust the difficulty.
  - After moving off-screen, the clone is hidden and deleted to prevent stacking and overlapping.

### Handling Input

- The game waits for the space bar to be pressed before proceeding with the racing sequence.

### Score Management

- **Score Increment:** 
  - The score increases by 1 every 0.5 seconds, and the highest score is tracked.

### Music

- The game features background stock music and a crashing sound effect.

## Troubleshooting

- **Cars Stacking at the Bottom:** 
  - Ensure the `y` position check in the `repeat until` block is set correctly based on your stage dimensions.
  - Adjust the movement speed and hiding/deleting logic if cars do not disappear as expected.
  - Adding some empty pixels to the top of the car costume resolved this issue.

## Credits

This project was created using Scratch by Jashandeep Singh as a part of Week 0 "Starting from Scratch" of Harvard University's CS50’s Introduction to Computer Science course. Special thanks to the Scratch community and the CS50 course for providing a platform for creative coding and game development.

---
