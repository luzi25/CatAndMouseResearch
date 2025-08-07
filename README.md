# Cat and Mouse AI Reinforcement Learning Platform

A sophisticated web-based AI simulation featuring reinforcement learning agents in a predator-prey ecosystem with advanced visual effects and comprehensive customization options.

## 🎯 Features

### Core Simulation
- **Individual AI Agents**: Cat (predator) and Mouse (prey) with separate Q-learning algorithms
- **Dynamic Vision System**: Toggle between circular (360°) and directional cone vision with AI-controlled rotation
- **Strategic Rotation AI**: Agents intelligently choose facing direction based on tactical situation
- **Dynamic Environment**: Customizable grid size, obstacle placement, and spawn points
- **Real-time Analytics**: Performance tracking with win/loss statistics and episode data
- **Training Persistence**: Save/load training data with environment configurations

### Visual Effects
- **CRT Monitor Simulation**: Phosphor glow, scanlines, contrast, brightness, and saturation controls
- **Fisheye Lens Effect**: Dramatic lens distortion with elliptical clipping and enhanced vignette
- **Unified Scramble Animation**: Header and footer feature matching mouse-proximity scramble text effects
- **Lumon Hover Effects**: Discrete 3-level scaling system (5x, 3x, 2x) with character-type-specific glows on render grid
- **Text Pressure Effects**: Dynamic character styling on interface elements (title, controls)

### User Interface
- **Hidden Advanced Settings**: All settings accessible via **Ctrl+M** keyboard shortcut for cleaner interface
- **Collapsible Interface**: Organized accordion panels for Learning Parameters and Settings
- **Individual Learning Controls**: Separate parameter controls for cat and mouse agents
- **Smart Button States**: Dynamic Start/Continue button behavior based on training data status
- **Direct Character Editing**: Click-to-edit functionality for all game characters
- **Enhanced Performance**: Simulation speed up to 5000ms for extreme testing scenarios

## 🚀 Quick Start

1. Open `index.html` in a modern web browser
2. Click **"Start"** to begin the AI simulation
3. Use **Ctrl+M** to access advanced settings and customization options
4. Monitor agent performance in real-time through the analytics panel
5. Save training progress using the **Download** button

## 🎮 Controls

### Training Controls
- **Start/Continue**: Intelligent button that adapts based on existing training data
- **Stop**: Pause current session
- **New Round**: Start fresh training session (appears after training completion)
- **Download/Upload**: Save and restore training data with visual feedback

### Vision System
- **Toggle Vision**: Enable/disable vision visualization
- **Cone Vision**: Switch between circular and directional cone vision
- **Vision Angle**: Adjust cone angle (30°-180°)
- **Dynamic Rotation**: Agents automatically rotate each step based on AI strategy

### Learning Parameters
- **Individual Agent Controls**: Separate learning rate and exploration rate for cat and mouse
- **Shared Parameters**: Common discount factor and exploration decay settings
- **Collapsible Sections**: Organized accordion interface for better space management

### Advanced Settings (Ctrl+M)
- **Visual Customization**: CRT effects, fisheye lens, Lumon hover effects, text pressure effects
- **Lumon Hover Configuration**: Customizable effect radius, scaling thresholds, transition speed
- **Character Editing**: Customize all game symbols
- **Typography Controls**: Font sizes for all interface elements
- **Layout Positioning**: Adjust panel positions

## 🔧 Technical Details

### AI Implementation
- **Individual Q-Learning Agents**: Separate algorithms with customizable learning parameters
- **Dynamic Vision System**: Mathematical cone vision algorithm with AI-controlled rotation
- **Strategic Decision Making**: Agents choose both movement and facing direction
- **State Space**: Grid position awareness with obstacle detection and line-of-sight calculations
- **Action Space**: Movement actions plus dynamic rotation selection with intelligent tie-breaking
- **Reward System**: Dynamically balanced distance-based rewards designed for competitive gameplay

### Performance Features
- **Optimized Rendering**: Efficient DOM updates with differential grid rendering and element caching
- **Spatial Optimization**: Ultra-smooth mouse proximity effects with spatial partitioning
- **Adaptive Performance**: Automatic quality adjustment based on frame rate monitoring
- **Memory Management**: Persistent Q-tables with training data compression
- **Responsive UI**: Viewport-constrained layouts preventing scroll overflow

### Browser Compatibility
- Modern browsers with ES6+ support
- Hardware acceleration recommended for visual effects
- Minimum viewport: 1024x768 for optimal experience

## 📊 Analytics

The simulation provides comprehensive performance metrics:
- **Episode Tracking**: Current episode number and step count
- **Win Statistics**: Cat vs Mouse victory counts with percentages
- **Performance Charts**: Visual representation of training progress
- **Training Data**: Exportable session data with environment configuration
- **Performance Trends**: Win rate predictions and convergence monitoring

## 🎨 Customization

### Character Set
- Empty Space: `·` (middle dot)
- Cat (Predator): `C`
- Mouse (Prey): `M`
- Obstacles: `O`
- Vision Indicator: `?` (both agents)
- Vision Collision: `!` (overlapping vision areas)

### Color Scheme
- Primary: Cyan (`#7FE9E1`)
- Background: Dark Navy (`#101827`)
- Accent: Medium Gray (`#4B566A`)
- Text: Light Cyan for contrast
- Heat Maps: Tom and Jerry colors (gray for cat, brown/orange for mouse)

### Lumon Hover Effects
- **Cat (Predator)**: Red/Orange glow (`#FF6B6B` to `#FFAB91`)
- **Mouse (Prey)**: Green glow (`#4CAF50` to `#A5D6A7`)
- **Obstacles**: Yellow/Gold glow (`#FFD700` to `#FFF176`)
- **Vision Cells**: Blue/Cyan glow (`#00BCD4` to `#80DEEA`)
- **Collisions**: Purple/Magenta glow (`#E91E63` to `#F8BBD9`)
- **Empty Spaces**: Subtle white/cyan glow

## 🖱️ Mouse Interaction

### Render Grid Hover Effects
- **Lumon Scaling**: Move cursor over the simulation grid to see characters scale dynamically
- **3 Discrete Levels**: Large (5x scale), Medium (3x), Small (2x) based on cursor proximity  
- **Character-Specific Colors**: Each agent type has unique glow colors for better identification
- **Configurable Thresholds**: Adjust effect radius and scaling zones in advanced settings
- **Smooth Tracking**: Optimized mouse coordinate calculation for fluid responsiveness

### Interface Elements  
- **Text Pressure Effects**: Title and control text responds to cursor proximity with styling changes
- **Inline Editing**: Click parameter values to edit directly
- **Collapsible Panels**: Click section headers to expand/collapse settings groups

## ⌨️ Keyboard Shortcuts

- **Spacebar**: Start/Stop training
- **Ctrl+M**: Toggle advanced settings
- **H**: Toggle heat map display
- **V**: Toggle vision display
- **1-4**: Load environment presets
- **F1**: Show keyboard shortcuts help

## 🤖 AI Behavior

### Cat (Predator) Strategy
- **Individual Learning**: Customizable learning rate and exploration parameters
- **Aggressive Hunting**: Enhanced reward system encourages persistent pursuit
- **Dynamic Hunting**: Rotates vision cone toward mouse for strategic pursuit
- **Vision-Based Pursuit**: Utilizes directional cone vision for focused tracking
- **Adaptive Behavior**: Balances exploration vs exploitation with separate epsilon decay

### Mouse (Prey) Strategy
- **Separate AI System**: Independent learning parameters from cat agent
- **Strategic Escape**: Balanced reward system requires tactical thinking
- **Evasion Tactics**: Dynamically rotates between watching cat and looking away
- **Danger Awareness**: Enhanced penalty system encourages smarter positioning
- **Survival Optimization**: Learns optimal movement and rotation patterns

## 🛠️ Development

The project is built with vanilla JavaScript, HTML5, and CSS3:
- No external dependencies
- Self-contained single-file application
- Modern web standards compliance

## 📁 Project Structure

```
├── index.html           # Main application file
├── README.md           # This file
├── CHANGELOG.md        # Detailed change history
├── test_fisheye.html   # Fisheye effect test file
└── assets/
    ├── Lumon_logo.png
    └── Logo_Load_Up_Screen_2-3387166046 (1).gif
```

---

**Cat and Mouse AI Platform** - Advanced Reinforcement Learning Research Tool  
*Exploring the boundaries of artificial intelligence through interactive predator-prey dynamics*