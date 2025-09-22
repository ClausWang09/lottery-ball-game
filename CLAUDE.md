# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a lottery ball drawing web game implemented as a single HTML file with embedded CSS and JavaScript. The game features three transparent spherical lottery boxes that draw balls with names from a user list.

## Key Files

- `index.html` - Main game file containing the complete web application
- `user.txt` - List of participant names (one per line), currently contains 18 names
- `gamescenario.txt` - Chinese game specification document describing the requirements and features

## Game Architecture

The application is built with vanilla JavaScript using an object-oriented approach:

### Core Classes
- `Ball` - Represents individual lottery balls with physics simulation (bouncing animation)
- `LotteryBox` - Manages collections of balls within each transparent box, handles drawing and animations

### Game Flow
1. Three lottery boxes each contain identical sets of balls with names from `user.txt`
2. Balls continuously animate (bouncing) within transparent spherical containers
3. Drawing sequence: left box → middle box → right box (with delays)
4. Winner determined when 2+ boxes show the same name
5. Two drawing modes: single draw and continuous draw (keeps drawing until winner found)

### Key Features
- Physics-based ball animation with collision detection
- Sequential drawing with visual feedback
- Winner highlighting with glowing animation effects
- Continuous draw mode for automatic re-draws
- Game state management (drawing/idle/ended)

## Development Notes

- No build process required - open `index.html` directly in browser
- No external dependencies - uses only vanilla HTML/CSS/JavaScript
- Names are hardcoded in JavaScript array but sourced from `user.txt`
- Responsive design with gradient backgrounds and smooth animations
- All styling embedded in `<style>` tags within the HTML

## Making Changes

When modifying the name list:
1. Update `user.txt` with new names (one per line)
2. Update the `names` array in the JavaScript section of `index.html`
3. The game automatically adjusts to the number of names provided

The game specification in `gamescenario.txt` is in Chinese and describes the detailed requirements for the lottery drawing mechanics and visual effects.