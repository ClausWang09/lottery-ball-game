# Lottery Ball Drawing Game

A web-based lottery ball drawing game with physics-based animations and winner detection. Watch balls bounce around in transparent spherical boxes and see who gets selected!

## 🎮 How to Play

### Getting Started
1. Open `index.html` in any modern web browser
2. You'll see three transparent lottery boxes with bouncing balls
3. Each ball contains a name from the participant list

### Game Controls
- **Start Drawing**: Draws one ball from each box sequentially (left → middle → right)
- **Continuous Draw**: Keeps drawing until a winner is found or no balls remain
- **Restart Game**: Resets all balls back to the boxes and starts over

### How to Win
- A winner is determined when **2 or more boxes** show the **same name**
- The winning name will be highlighted with a golden glow animation
- If no winner is found in a round, you can draw again or use continuous mode

### Game Features
- **Physics Animation**: Balls bounce realistically within the spherical containers
- **Sequential Drawing**: Each box draws in order with visual feedback
- **Visual Effects**: Winner highlighting with glowing animations
- **Two Game Modes**: Single draw or continuous until winner
- **Customizable**: Easy to modify participant list

## 📝 Customizing Participants

### Method 1: Edit user.txt
1. Open `user.txt` in any text editor
2. Add/remove names (one name per line)
3. Save the file

### Method 2: Edit JavaScript directly
1. Open `index.html` in a text editor
2. Find the `names` array around line 183:
   ```javascript
   const names = [
       'Frank', 'Henry', 'Peter', 'Roger', 'David', 'Sean', 'Jill', 'Wendy',
       'Winyoung', 'Kris', 'Rick', 'Joey', 'Tyler', 'Jeffrey', 'Sylvia', 'Eddie', 'Hana', 'Jolie'
   ];
   ```
3. Modify the names in the array
4. Save and refresh the browser

## 🚀 GitHub Operations

### Cloning the Repository
```bash
git clone https://github.com/ClausWang09/lottery-ball-game.git
cd lottery-ball-game
```

### Making Changes and Contributing
1. **Make your changes** to the files
2. **Stage changes**:
   ```bash
   git add .
   ```
3. **Commit changes**:
   ```bash
   git commit -m "Description of your changes"
   ```
4. **Push to GitHub**:
   ```bash
   git push origin master
   ```

### Creating a New Feature
1. **Create a new branch**:
   ```bash
   git checkout -b feature-name
   ```
2. **Make your changes and commit them**
3. **Push the branch**:
   ```bash
   git push origin feature-name
   ```
4. **Create a Pull Request** on GitHub

### Staying Updated
```bash
git pull origin master
```

## 📁 Project Structure

```
lottery-ball-game/
├── index.html          # Main game file (complete web app)
├── user.txt           # List of participant names
├── gamescenario.txt   # Game specifications (Chinese)
├── CLAUDE.md          # Claude Code documentation
├── README.md          # This file
└── .gitignore         # Git ignore rules
```

## 🛠 Technical Details

- **Framework**: Vanilla HTML/CSS/JavaScript (no dependencies)
- **Compatibility**: Works in all modern web browsers
- **Architecture**: Object-oriented with Ball and LotteryBox classes
- **Animation**: CSS animations with JavaScript physics simulation
- **Responsive**: Adapts to different screen sizes

## 🎯 Game Mechanics

1. **Initialization**: Each box contains identical sets of balls with participant names
2. **Animation**: Balls continuously bounce within spherical containers using collision detection
3. **Drawing Process**:
   - Sequential drawing from left to right boxes
   - 1-second delay between each draw
   - Visual feedback during drawing process
4. **Winner Detection**: Checks for 2+ matching names across the three results
5. **Continuous Mode**: Automatically re-draws until winner or no balls remain

## 🔧 Troubleshooting

**Game not loading?**
- Ensure you're opening `index.html` in a web browser
- Check browser console for any JavaScript errors

**Names not updating?**
- Make sure you've updated both `user.txt` AND the JavaScript array in `index.html`
- Refresh the browser after making changes

**Animations not smooth?**
- Try using a different browser (Chrome/Firefox recommended)
- Close other resource-intensive applications

## 📜 License

This project is open source. Feel free to modify and distribute as needed.

---

**Repository**: https://github.com/ClausWang09/lottery-ball-game
**Game Type**: Web-based Lottery/Drawing Game
**Created**: 2025