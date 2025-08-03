# Lumon Research - AI Predator-Prey Simulation

A sophisticated web-based AI simulation featuring reinforcement learning agents in a predator-prey ecosystem with advanced visual effects and comprehensive customization options.

## 🎯 Features

### Core Simulation
- **Q-Learning AI Agents**: Cat (predator) and Mouse (prey) with independent learning algorithms
- **Dynamic Environment**: Customizable grid size, obstacle placement, and spawn points
- **Real-time Analytics**: Performance tracking with win/loss statistics and episode data
- **Training Persistence**: Save/load training data with environment configurations

### Visual Effects
- **CRT Monitor Simulation**: Phosphor glow, scanlines, contrast, brightness, and saturation controls
- **Fisheye Lens Effect**: Dramatic lens distortion with elliptical clipping and enhanced vignette
- **Text Pressure Effects**: Dynamic character styling based on mouse proximity with weight, opacity, and scale effects
- **Scramble Text Animation**: Footer text scrambling effect for enhanced immersion

### User Interface
- **Consolidated Settings Panel**: Organized dropdown with Typography and Character customization subsections
- **Direct Character Editing**: Click-to-edit functionality for all game characters (·, C, M, O, ?, !)
- **Themed Controls**: Custom sliders and styled input elements with cyan color scheme
- **Responsive Design**: Viewport-constrained interface that prevents layout overflow

### Typography System
- **Font Customization**: Individual size controls for all interface elements
- **Grid Character Control**: Adjustable character size and spacing for the game grid
- **Value Display Toggle**: Show/hide parameter value displays
- **Reset Functionality**: One-click reset to default typography settings

## 🚀 Quick Start

1. Open `lumon_research.html` in a modern web browser
2. Click **"Start Training"** to begin the AI simulation
3. Use the **Settings** dropdown to customize visual effects and characters
4. Monitor agent performance in real-time through the analytics panel
5. Save training progress using the **Download Training** button

## 🎮 Controls

### Training Controls
- **Start Training**: Begin new training session
- **Stop Training**: Pause current session
- **Continue Training**: Resume paused session
- **Download/Upload**: Save and restore training data

### Visual Customization
- **CRT Effects**: Enable/disable retro monitor simulation
- **Fisheye Lens**: Adjust lens distortion intensity (0-5)
- **Text Pressure**: Mouse-proximity-based text effects
- **Character Editing**: Click any blue character value to edit

### Grid Settings
- **Font Size**: Character size in the game grid
- **Spacing**: Horizontal and vertical character spacing
- **Characters**: Customize all game symbols (empty space, cat, mouse, obstacles, vision indicators)

## 🔧 Technical Details

### AI Implementation
- **Q-Learning Algorithm**: Reinforcement learning with epsilon-greedy exploration
- **State Space**: Grid position awareness with obstacle detection
- **Action Space**: 5 actions (up, down, left, right, stay)
- **Reward System**: Distance-based rewards with win/loss bonuses

### Performance Features
- **Optimized Rendering**: Efficient DOM updates for smooth animation
- **Memory Management**: Persistent Q-tables with training data compression
- **Responsive UI**: Viewport-constrained layouts preventing scroll overflow

### Browser Compatibility
- Modern browsers with ES6+ support
- Hardware acceleration recommended for visual effects
- Minimum viewport: 1024x768 for optimal experience

## 📊 Analytics

The simulation provides comprehensive performance metrics:
- **Episode Tracking**: Current episode number and step count
- **Win Statistics**: Cat vs Mouse victory counts
- **Performance Charts**: Visual representation of training progress
- **Training Data**: Exportable session data with environment configuration

## 🎨 Customization

### Character Set
- Empty Space: `·` (middle dot)
- Cat (Predator): `C`
- Mouse (Prey): `M`
- Obstacles: `O`
- Cat Vision: `?`
- Mouse Vision: `!`

### Color Scheme
- Primary: Cyan (`#7FE9E1`)
- Background: Dark Navy (`#101827`)
- Accent: Medium Gray (`#4B566A`)
- Text: Light Cyan for contrast

## 🔄 Recent Updates

- **Consolidated Settings**: Reorganized UI with accordion subsections
- **Fisheye Effects**: Enhanced visual distortion with dramatic lens effects
- **Character Editing**: Direct click-to-edit functionality
- **Layout Optimization**: Strict height constraints preventing footer displacement
- **Performance Improvements**: Optimized rendering and memory usage

## 📁 Project Structure

```
├── lumon_research.html    # Main application file
├── CHANGELOG.md          # Detailed change history
├── README.md            # This file
└── package.json         # Project metadata
```

## 🤖 AI Behavior

### Cat (Predator) Strategy
- Learns optimal hunting patterns
- Balances exploration vs exploitation
- Adapts to mouse movement patterns

### Mouse (Prey) Strategy
- Develops evasion tactics
- Learns safe zones and escape routes
- Optimizes survival probability

## 🛠️ Development

The project is built with vanilla JavaScript, HTML5, and CSS3:
- No external dependencies
- Self-contained single-file application
- Modern web standards compliance

---

**Lumon Research** - Advanced AI Simulation Platform  
*Exploring the boundaries of artificial intelligence through interactive predator-prey dynamics*