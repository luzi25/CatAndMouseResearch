# Lumon Research - AI Predator-Prey Simulation

A sophisticated web-based AI simulation featuring reinforcement learning agents in a predator-prey ecosystem with advanced visual effects and comprehensive customization options.

## 🎯 Features

### Core Simulation
- **Individual AI Agents**: Cat (predator) and Mouse (prey) with separate Q-learning algorithms, customizable learning parameters, and dynamically balanced reward systems
- **Dynamic Vision System**: Toggle between circular (360°) and directional cone vision with AI-controlled rotation that adapts with each step
- **Strategic Rotation AI**: Agents intelligently choose facing direction based on tactical situation - hunting vs evasion strategies
- **Dynamic Environment**: Customizable grid size, obstacle placement, and spawn points
- **Real-time Analytics**: Performance tracking with win/loss statistics, episode data, and AI balance analysis for optimal competitive gameplay
- **Training Persistence**: Save/load training data with environment configurations and intelligent button state management

### Visual Effects
- **CRT Monitor Simulation**: Phosphor glow, scanlines, contrast, brightness, and saturation controls
- **Fisheye Lens Effect**: Dramatic lens distortion with elliptical clipping and enhanced vignette
- **Unified Scramble Animation**: Header and footer feature matching mouse-proximity scramble text effects for consistent interactive feedback
- **Text Pressure Effects**: Dynamic character styling based on mouse proximity with weight, opacity, and scale effects

### User Interface
- **Hidden Advanced Settings**: All 4 settings tabs hidden by default, accessible via **Ctrl+M** keyboard shortcut for cleaner interface
- **Collapsible Interface**: Organized accordion panels for Learning Parameters, Display Controls, and Settings with consistent spacing
- **Individual Learning Controls**: Separate parameter controls for cat and mouse agents (learning rate, exploration rate) plus shared parameters
- **Smart Button States**: Dynamic Start/Continue button behavior based on training data status with visual upload feedback
- **Direct Character Editing**: Click-to-edit functionality for all game characters (·, C, M, O, ?, !)
- **Borderless Sliders**: Clean, modern range inputs without borders for minimalist design
- **Enhanced Performance**: Simulation speed up to 5000ms for extreme testing scenarios
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
- **Start/Continue Training**: Intelligent button that adapts based on existing training data
- **Stop Training**: Pause current session
- **Download/Upload**: Save and restore training data with visual feedback

### Vision System
- **Toggle Vision**: Enable/disable vision visualization
- **Cone Vision**: Switch between circular and directional cone vision
- **Vision Angle**: Adjust cone angle (30°-180°)
- **Dynamic Rotation**: Agents automatically rotate each step based on AI strategy (manual override available)
- **Strategic Behavior**: Cat hunts by facing toward mouse; Mouse uses evasion tactics with occasional opposite-direction rotation

### Learning Parameters
- **Individual Agent Controls**: Separate learning rate and exploration rate for cat and mouse
- **Shared Parameters**: Common discount factor and exploration decay settings
- **Collapsible Sections**: Organized accordion interface for better space management

### Visual Customization
- **CRT Effects**: Enable/disable retro monitor simulation
- **Fisheye Lens**: Adjust lens distortion intensity (0-5)
- **Scramble Animations**: Unified mouse-proximity text scrambling for header and footer
- **Character Editing**: Click any blue character value to edit
- **Advanced Settings**: Access all customization options via **Ctrl+M** shortcut

### Grid Settings
- **Font Size**: Character size in the game grid
- **Spacing**: Horizontal and vertical character spacing
- **Characters**: Customize all game symbols (empty space ·, cat C, mouse M, obstacles O, vision ?, collision !)

## 🔧 Technical Details

### AI Implementation
- **Individual Q-Learning Agents**: Separate algorithms with customizable learning parameters and dynamically balanced reward systems optimized for competitive 50/50 win rates
- **Dynamic Vision System**: Mathematical cone vision algorithm with AI-controlled rotation that adapts each step
- **Strategic Decision Making**: Agents choose both movement and facing direction based on exploration vs exploitation phases
- **State Space**: Grid position awareness with obstacle detection and line-of-sight calculations
- **Action Space**: Movement actions (up, down, left, right) plus dynamic rotation selection with intelligent tie-breaking
- **Reward System**: Dynamically balanced distance-based rewards with win/loss bonuses, vision-aware scoring, and strategic penalties designed for competitive gameplay (cat hunting +8, mouse escape +4/+2, danger penalties -0.5/-2)

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
- Vision Indicator: `?` (both agents)
- Vision Collision: `!` (overlapping vision areas)

### Color Scheme
- Primary: Cyan (`#7FE9E1`)
- Background: Dark Navy (`#101827`)
- Accent: Medium Gray (`#4B566A`)
- Text: Light Cyan for contrast

## 🔄 Recent Updates

### Major Features (Latest)
- **AI Reward System Rebalancing**: Comprehensive reward optimization based on training data analysis, addressing mouse dominance (69.9% win rate) with enhanced cat hunting rewards and strategic penalties for balanced competitive gameplay
- **Dynamic Agent Rotation**: AI agents now rotate their vision direction with each step based on strategic decision-making
- **Hidden Advanced Settings**: All customization options accessible via Ctrl+M shortcut for cleaner default interface
- **Enhanced Performance**: Simulation speed increased to 5000ms maximum for extreme testing scenarios
- **Unified Animations**: Header and footer now share matching scramble text effects
- **Cone Vision System**: Directional vision with adjustable angles and AI-controlled rotation
- **Individual Learning Parameters**: Separate AI controls for cat and mouse agents
- **Smart Button States**: Dynamic UI that adapts to training data status
- **Collapsible Interface**: Organized accordion panels for better space management

### Previous Updates
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
- **Individual Learning**: Customizable learning rate and exploration parameters with optimized reward system
- **Aggressive Hunting**: Enhanced reward system (+8 for hunting, +2 for exploration) encourages persistent pursuit
- **Dynamic Hunting**: Rotates vision cone toward mouse for strategic pursuit each step
- **Vision-Based Pursuit**: Utilizes directional cone vision for focused tracking with strategic penalties for retreating
- **Adaptive Behavior**: Balances exploration vs exploitation with separate epsilon decay and movement pressure (-0.1 for standing still)

### Mouse (Prey) Strategy
- **Separate AI System**: Independent learning parameters from cat agent with balanced reward constraints
- **Strategic Escape**: Rebalanced reward system (+4 for strategic escape, +2 for blind escape) requires more tactical thinking
- **Evasion Tactics**: Dynamically rotates between watching cat and looking away (30% evasion chance) with movement pressure (-0.2 for standing still)
- **Danger Awareness**: Enhanced penalty system (-0.5/-2) for approaching threats encourages smarter positioning
- **Survival Optimization**: Learns optimal movement and rotation patterns with risk/reward balance for competitive gameplay

## 🛠️ Development

The project is built with vanilla JavaScript, HTML5, and CSS3:
- No external dependencies
- Self-contained single-file application
- Modern web standards compliance

---

**Lumon Research** - Advanced AI Simulation Platform  
*Exploring the boundaries of artificial intelligence through interactive predator-prey dynamics*