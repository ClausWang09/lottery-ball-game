# Lottery Ball Drawing Game

A web-based lottery ball drawing game with physics-based animations and winner detection. Watch balls bounce around in transparent spherical boxes and see who gets selected!

## 🎮 How to Play

### Getting Started
1. Open `index.html` in any modern web browser
2. You'll see three transparent lottery boxes with bouncing balls
3. Each ball contains a name from the participant list

### Game Controls
- **Continuous Draw**: Automatically draws balls from all three boxes sequentially and continues until a winner is found or no balls remain
- **Restart Game**: Resets all balls back to the boxes, clears winner history, and starts over

### How to Win
- A winner is determined when **2 or more boxes** show the **same name**
- The winning name will be highlighted with a golden glow animation
- If no winner is found in a round, you can draw again or use continuous mode

### Game Features
- **Physics Animation**: Balls bounce realistically within the spherical containers
- **Enhanced Ball Animation**: Balls float upward, scale progressively (1x → 3.5x), and explode with golden effects
- **Real-time Probability Display**: Horizontal panel showing each participant's winning odds, updated after every draw
- **Sequential Drawing**: Each box draws in order with visual feedback and probability updates
- **Visual Effects**: Winner highlighting with glowing animations and explosion effects
- **Winners Hall**: Track all winners with a beautiful crown-topped list on the right side
- **Continuous Game Mode**: Automatic drawing until winner or balls depleted
- **Continue After Win**: No need to restart - continue drawing after each winner
- **Smart Probability Calculation**: Accurate mathematical calculation based on independent box draws
- **Simplified Interface**: Streamlined controls and clean layout design
- **Customizable**: Easy to modify participant list

## 📝 Customizing Participants

### Method 1: Edit user.txt
1. Open `user.txt` in any text editor
2. Add/remove names (one name per line)
3. Save the file

### Method 2: Edit JavaScript directly
1. Open `index.html` in a text editor
2. Find the `names` array around line 435:
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
- **Animation**: Advanced CSS animations with JavaScript physics simulation
- **Layout**: Vertical layout with probability panel, game area and winners panel
- **Effects**: Glassmorphism design, backdrop filters, and particle-like explosions
- **Mathematics**: Real-time probability calculations using binomial distribution
- **Responsive**: Adapts to different screen sizes

## 🎲 Probability Display Features

### Mathematical Accuracy
- **Independent Analysis**: Each box treated as separate probability space
- **Real-time Updates**: Probabilities recalculated after every single ball draw
- **Precise Formula**: Uses binomial probability for 2+ successes in 3 trials
- **Edge Cases**: Handles empty boxes and eliminated participants correctly

### Visual Design
- **Horizontal Layout**: Participants displayed in flowing horizontal cards
- **Sky Blue Theme**: Distinctive color scheme (#87CEEB) separate from winners
- **Compact Cards**: 120px minimum width with flexible wrap layout
- **Status Indicators**: Eliminated participants shown in grayscale
- **Percentage Display**: Probabilities shown to 1 decimal place (e.g., 15.3%)

### User Experience
- **Live Updates**: Watch probabilities change as balls are drawn
- **Elimination Tracking**: See when participants have no remaining chances
- **Competitive Analysis**: Compare all participants' odds at a glance
- **Educational Value**: Learn probability theory in action

## 🏆 Winners Hall Features

### Visual Design
- **Crown Icon**: Golden crown (👑) with drop-shadow effects
- **Glassmorphism**: Semi-transparent background with backdrop blur
- **Golden Border**: Elegant golden border with rounded corners
- **Gradient Effects**: Beautiful gradient backgrounds for winner items

### Functionality
- **Auto-numbering**: Each winner gets a sequential number (1, 2, 3...)
- **Slide Animation**: New winners appear with smooth slide-in effect
- **Scrollable List**: Supports unlimited winners with custom scrollbar
- **Auto-clear**: Winners list clears when "Restart Game" is pressed
- **Persistent Tracking**: Winners remain visible throughout the session

### Layout
- **Fixed Position**: 300px width panel on the right side
- **Flexible Height**: Adapts to content with scrolling when needed
- **Responsive Design**: Maintains visibility across different screen sizes

## 🎯 Game Mechanics

1. **Initialization**: Each box contains identical sets of balls with participant names
2. **Real-time Probability**: Horizontal panel displays each participant's winning probability (updated live)
3. **Animation**: Balls continuously bounce within spherical containers using collision detection
4. **Drawing Process**:
   - Sequential drawing from left to right boxes
   - **Enhanced Animation**: Selected balls float upward while scaling (1x → 3x → 3.5x → 4x)
   - **Explosion Effect**: Balls explode with golden glow and light effects when reaching box edge
   - Name appears on scoreboard precisely during explosion
   - **Probability Updates**: After each box draw, all participants' probabilities recalculated
   - 1-second delay between each draw
5. **Winner Detection**: Checks for 2+ matching names across the three results
6. **Mathematical Accuracy**: Probability calculation uses independent box analysis:
   ```
   P(Win) = P(exactly 2 matches) + P(exactly 3 matches)
   P(exactly 2) = p1×p2×(1-p3) + p1×(1-p2)×p3 + (1-p1)×p2×p3
   P(exactly 3) = p1×p2×p3
   ```
7. **Winners Tracking**: All winners automatically added to the Winners Hall with sequential numbering
8. **Continuous Mode**: Automatically re-draws until winner or no balls remain
9. **Seamless Continuation**: After winner found, continue drawing without manual restart

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

## 🎨 Interface Design

### Layout Structure
```
Lottery Ball Game (Title)
         ↓
[Probability Panel - Horizontal Cards]
         ↓
[Game Area] + [Winners Hall]
    ↓           ↓
[Scoreboards]  [Crown Icon]
[Lottery Boxes] [Winner List]
[Controls]     [Scroll Area]
```

### Control Simplification
- **Single Action**: "Continuous Draw" button for all drawing operations
- **Clean Reset**: "Restart Game" button for complete game reset
- **Streamlined UI**: Removed redundant "Start Drawing" option
- **Intuitive Flow**: One-button operation for seamless gameplay

### Color Scheme
- **Background**: Purple gradient (#667eea to #764ba2)
- **Probability Panel**: Sky blue theme (#87CEEB)
- **Winners Hall**: Golden theme (#FFD700)
- **Game Elements**: White/transparent with glassmorphism effects

---

**Repository**: https://github.com/ClausWang09/lottery-ball-game
**Game Type**: Web-based Lottery/Drawing Game with Real-time Probability Analytics
**Created**: 2025
**Features**: Physics Animation, Live Probability Calculation, Winners Tracking