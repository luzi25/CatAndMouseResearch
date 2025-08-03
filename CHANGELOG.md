# Changelog

All notable changes to the Lumon Research project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- **Settings Dropdown with Accordion Behavior**: New "Settings" dropdown in analytics panel containing all control panels (Grid Font, CRT, Text Pressure, Typography, Character Customization) with accordion behavior where only one section can be open at a time
- **Enhanced CRT Screen Warp Effect**: Added screen warp parameter to CRT controls with subtle 3D curvature effect using CSS transforms (perspective, rotateX, rotateY, scale, border-radius)
- **Font Size Value Display Toggle**: Added toggle in Typography Controls to show/hide value displays (hidden by default)
- **Character Customization Settings**: New settings panel allowing users to modify render characters (•, C, M, O, ?, !) with Apply button and dynamic legend updates
- **Obstacle Count Display**: Added actual obstacle count display to analytics panel
- **Training Data Persistence**: Enhanced training system with consistent spawn points throughout sessions and comprehensive data persistence including spawn points, obstacles, and character mappings
- **End Result Screen Close Button**: Added square close button with cyan "X" icon in top-right corner of performance chart

### Changed
- **Main Title Font**: Changed to Scriptorama Tradeshow JF with Google Fonts import
- **Default Render Character**: Changed from period (.) to bullet (•) throughout the system
- **Mouse Cursor Behavior**: Implemented cursor rules - default arrow pointer, finger pointer only for interactive elements (buttons, inputs)
- **Chart Styling**: Updated performance chart with cyan color scheme, proper data labeling (M for predator, C for prey), and cyan-themed axes, grid, and text
- **Agent Movement Logic**: Fixed Q-learning action selection bias by implementing random tie-breaking instead of defaulting to 'up' movement

### Fixed
- **Obstacle Count Bug**: Fixed obstacle count variable to accurately reflect actual number of obstacles instead of always displaying 10
- **Border Spawning Issue**: Modified object spawning logic to prevent objects from spawning on map borders (first/last rows and columns)
- **Agent Movement Bias**: Eliminated agents' tendency to wander north at session start by fixing action selection algorithm

### Removed
- **Tick Icons**: Removed tick icons from all checkbox buttons for cleaner appearance

### Technical Improvements
- Enhanced download/upload training functionality with environment data persistence
- Improved accordion UI behavior for better user experience
- Added comprehensive character mapping system with real-time updates
- Implemented consistent spawn point system for training sessions