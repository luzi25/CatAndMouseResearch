# Changelog

All notable changes to the Lumon Research project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
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
- **Close Button Z-Index**: Fixed end result screen close button by increasing z-index to 10000 to ensure clicks work properly above CRT overlay
- **Settings Dropdown Height**: Implemented strict height constraints (40vh max-height) with internal scrolling to prevent page scrolling and footer movement
- **Typography/Characters Spacing**: Made Typography and Characters sections extremely compact with reduced margins (0.15rem vs 0.3rem) and smaller fonts
- **Obstacle Count Bug**: Fixed obstacle count variable to accurately reflect actual number of obstacles instead of always displaying 10
- **Border Spawning Issue**: Modified object spawning logic to prevent objects from spawning on map borders (first/last rows and columns)
- **Agent Movement Bias**: Eliminated agents' tendency to wander north at session start by fixing action selection algorithm

### Removed
- **Screen Warp Effect**: Replaced basic screen warp with more dramatic fisheye lens effect
- **Tick Icons**: Removed tick icons from all checkbox buttons for cleaner appearance

### Technical Improvements
- Enhanced fisheye lens distortion with complex perspective transforms and radial gradients
- Implemented compact CSS classes for settings sections to reduce vertical space usage
- Added z-index management for proper overlay layering
- Enhanced download/upload training functionality with environment data persistence
- Improved accordion UI behavior for better user experience
- Added comprehensive character mapping system with real-time updates
- Implemented consistent spawn point system for training sessions