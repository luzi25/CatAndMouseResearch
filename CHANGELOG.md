# Changelog

All notable changes to the Lumon Research project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- **Reward System Rebalancing**: Comprehensive reward system overhaul based on training data analysis showing mouse win rates of 69.9% vs cat 30.1%
- **Dynamic Agent Rotation System**: Agents can now rotate their vision direction with every step, choosing optimal facing directions based on strategic AI decision-making
- **Enhanced Simulation Speed**: Increased maximum simulation speed from 2000ms to 5000ms for extreme performance testing
- **Hidden Advanced Settings**: All 4 settings tabs (Settings, Typography, Characters, Layout Positioning) are now hidden by default and accessible via Ctrl+M keyboard shortcut
- **Header Scramble Animation**: Applied the same mouse-proximity scramble text effect to the header as used in the footer
- **Cone Vision System**: Implemented directional cone vision with adjustable angle (30°-180°) and individual rotation controls for cat and mouse agents with 45° directional increments
- **Individual Learning Parameters**: Split learning parameters into separate controls for cat (predator) and mouse (prey) with individual learning rates and exploration rates, while maintaining shared discount factor and exploration decay
- **Collapsible Learning Parameters**: Made Learning Parameters and Display Controls collapsible accordion sections for better UI organization
- **Advanced Button State Management**: Dynamic button states that change Start to Continue when training data is uploaded, with visual feedback during file operations
- **Vision Collision Detection**: Updated vision rendering system where both agents use '?' for vision indicators and '!' represents overlapping vision areas
- **Consolidated Settings Dropdown**: Reorganized Settings dropdown with Typography and Characters as collapsible subsections with accordion behavior
- **Fisheye Lens Effect**: Replaced screen warp with pronounced fisheye lens distortion featuring elliptical clipping, enhanced vignette, and center glow effects
- **Direct Character Editing**: Click-to-edit functionality for all character values (inline editing with blue highlighting)
- **Themed Slider Controls**: Replaced basic simulation speed control with styled themed slider
- **Settings Dropdown with Accordion Behavior**: New "Settings" dropdown in analytics panel containing all control panels (Grid Font, CRT, Text Pressure, Typography, Character Customization) with accordion behavior where only one section can be open at a time
- **Font Size Value Display Toggle**: Added toggle in Typography Controls to show/hide value displays (hidden by default)
- **Character Customization Settings**: New settings panel allowing users to modify render characters (·, C, M, O, ?, !) with Apply button and dynamic legend updates
- **Obstacle Count Display**: Added actual obstacle count display to analytics panel
- **Training Data Persistence**: Enhanced training system with consistent spawn points throughout sessions and comprehensive data persistence including spawn points, obstacles, and character mappings
- **End Result Screen Close Button**: Added square close button with cyan "X" icon in top-right corner of performance chart

### Changed
- **Reward System Balance**: Rebalanced cat vs mouse rewards for more competitive gameplay - cat hunting rewards increased (5→8), exploration rewards doubled (1→2), mouse escape rewards reduced (5→2), and higher danger penalties (-0.2/-1 → -0.5/-2) to encourage strategic play over random movement
- **Agent Rotation Behavior**: Vision direction now dynamically updates with each step based on AI strategy (exploration vs exploitation) rather than static slider settings
- **UI Accessibility**: Advanced settings now hidden by default with keyboard shortcut access for cleaner interface
- **Animation Consistency**: Header and footer now share identical scramble text effects for unified user experience
- **Slider Design**: Removed borders from all range input sliders for cleaner, more modern appearance
- **Learning Parameters Interface**: Removed hyperlink styling from Learning Parameters dropdown for streamlined appearance
- **UI Layout Consistency**: Standardized spacing throughout Settings and Analytics panels with consistent 0.4rem margins for all parameter elements
- **Footer Animation Settings**: Updated scramble text animation with increased radius (300px), longer duration (5 seconds), and restored fluid speed (80ms intervals)
- **Learning Parameter Architecture**: Restructured Q-learning system to support individual learning rates and exploration rates for cat and mouse agents
- **Vision System Logic**: Completely overhauled vision rendering to support both circular (360°) and cone-based directional vision modes
- **Character Legend System**: Updated legend to reflect new vision collision system with unified '?' for vision and '!' for overlaps
- **Empty Space Character**: Changed from bullet (•) to middle dot (·) for better visual consistency
- **Header Letter Spacing**: Reduced main title letter spacing from 6px to 2px for improved readability
- **Settings Layout**: Consolidated Typography and Character controls into compact subsections within main Settings dropdown
- **Settings Height Constraint**: Limited Settings dropdown to 40% viewport height with internal scrolling to prevent footer displacement
- **Reset Button Location**: Moved "Reset to Defaults" button from Typography to Characters section
- **Main Title Font**: Changed to Scriptorama Tradeshow JF with Google Fonts import
- **Mouse Cursor Behavior**: Implemented cursor rules - default arrow pointer, finger pointer only for interactive elements (buttons, inputs)
- **Chart Styling**: Updated performance chart with cyan color scheme, proper data labeling (M for predator, C for prey), and cyan-themed axes, grid, and text
- **Agent Movement Logic**: Fixed Q-learning action selection bias by implementing random tie-breaking instead of defaulting to 'up' movement

### Fixed
- **Collision Detection Bug**: Corrected operator precedence in collision detection logic to ensure cat wins when positions match
- **UI Spacing Inconsistencies**: Resolved spacing mismatches between param-row and param-item elements across all interface panels
- **Button State Synchronization**: Fixed upload workflow to properly update button states and provide visual feedback during file operations
- **Vision Character Rendering**: Updated Character Customization panel to reflect new vision system with proper character assignments
- **Individual Epsilon Decay**: Implemented separate epsilon decay handling for cat and mouse agents during training
- **Close Button Z-Index**: Fixed end result screen close button by increasing z-index to 10000 to ensure clicks work properly above CRT overlay
- **Settings Dropdown Height**: Implemented strict height constraints (40vh max-height) with internal scrolling to prevent page scrolling and footer movement
- **Typography/Characters Spacing**: Made Typography and Characters sections extremely compact with reduced margins (0.15rem vs 0.3rem) and smaller fonts
- **Obstacle Count Bug**: Fixed obstacle count variable to accurately reflect actual number of obstacles instead of always displaying 10
- **Border Spawning Issue**: Modified object spawning logic to prevent objects from spawning on map borders (first/last rows and columns)
- **Agent Movement Bias**: Eliminated agents' tendency to wander north at session start by fixing action selection algorithm

### Removed
- **Static Vision Direction**: Replaced fixed rotation sliders with dynamic AI-controlled rotation that adapts with each step
- **Header Text Pressure Animation**: Removed mouse-proximity font weight/opacity effects from main title, replaced with scramble animation
- **Learning Parameters Hyperlink**: Removed clickable help link from Learning Parameters dropdown title
- **Slider Borders**: Eliminated borders from all range input controls for minimalist design
- **Advanced Settings Visibility**: Hidden all 4 settings tabs by default, accessible only via Ctrl+M shortcut
- **Unified Learning Parameters**: Replaced single learning rate and epsilon with individual agent-specific parameters
- **Screen Warp Effect**: Replaced basic screen warp with more dramatic fisheye lens effect
- **Tick Icons**: Removed tick icons from all checkbox buttons for cleaner appearance

### Technical Improvements
- **AI Performance Analysis**: Implemented comprehensive training data analysis system that revealed mouse advantage (69.9% win rate) leading to reward system optimization for balanced 50/50 competitive gameplay
- **Dynamic Rotation AI System**: Implemented intelligent rotation selection with strategic vs random rotation based on exploration/exploitation phases
- **Real-time Vision Direction Updates**: Agents dynamically adjust facing direction each step with automatic UI synchronization
- **Strategic Decision Making**: Cat focuses toward mouse for hunting; Mouse employs evasion tactics with 30% opposite-direction probability
- **Keyboard Shortcut System**: Implemented Ctrl+M toggle functionality for advanced settings visibility with proper DOM manipulation
- **Enhanced Simulation Performance**: Extended speed range to 5000ms for high-performance training scenarios
- **Advanced Vision System**: Implemented mathematical cone vision algorithm with angle calculations and line-of-sight validation
- **Individual AI Agent Architecture**: Restructured Q-learning system with separate learning parameters and epsilon decay for each agent
- **Enhanced State Management**: Added comprehensive button state management with dynamic UI updates based on training data status
- **Accordion UI System**: Extended collapsible section functionality to learning parameters and display controls
- **Character Mapping System**: Unified character rendering system with real-time legend updates and customization persistence
- **Animation Parameter Control**: Granular control over scramble text animations with configurable radius, duration, and speed settings
- Enhanced fisheye lens distortion with complex perspective transforms and radial gradients
- Implemented compact CSS classes for settings sections to reduce vertical space usage
- Added z-index management for proper overlay layering
- Enhanced download/upload training functionality with environment data persistence
- Improved accordion UI behavior for better user experience
- Added comprehensive character mapping system with real-time updates
- Implemented consistent spawn point system for training sessions