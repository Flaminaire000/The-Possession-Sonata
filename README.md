# Possession Sonata - Web App

A gothic-themed web application companion for the board game **Possession Sonata**, a 1 vs 3 hidden-movement game where ghost musicians must reclaim their instruments and perform one final sonata before dawn.

## About the Game

**Possession Sonata** is an asymmetric board game where:
- **3 Ghosts** (deceased musicians) must retrieve their assigned instruments and perform them at specific locations
- **1 Johnny** (the Conductor/Ghost Hunter) tries to capture all ghosts before they complete their sonata
- The game lasts 6 game-hours, with victory conditions based on whether the ghosts complete their performance or Johnny captures them all

## Web App Features

### Atmospheric Interface
- Gothic-themed design with animated background and glowing effects
- Creepster font styling and dark color palette
- Floating particle effects for immersive atmosphere

### Audio System
- **6 Cursed Instruments**: Violin, Drums, Clarinet, Flute, Saxophone, Trumpet
- Dual audio system: attempts to load audio files, falls back to synthesized sounds
- Web Audio API integration with ADSR envelope synthesis
- Cross-browser compatibility with AudioContext management

### Spectral Detection System
- 3 detection levels with different audio feedback patterns
- Level 1 (Close Proximity): Rapid beeps with static noise and interference
- Level 2 (Medium Range): Moderate beep sequences
- Level 3 (Far Distance): Slow, faint beep patterns

## Technical Implementation

### Audio Architecture
- **Primary**: Attempts to load instrument audio files from local directory
- **Fallback**: Generates synthesized instrument sounds using Web Audio API
- **Features**: Frequency filtering, envelope shaping, and instrument-specific timbres

### Browser Support
- Modern browsers with Web Audio API support
- Automatic AudioContext activation on user interaction
- Error handling for audio loading failures

### File Structure
```
├── index.html          # Complete web application
├── sounds/             # Audio files directory (optional)
│   ├── VIOLIN.mp3
│   ├── DRUMS.mp3
│   ├── SAXOPHONE.mp3
│   ├── TRUMPET.mp3
│   ├── FLUTE.mp3
│   └── CLARINETTE.mp3
└── README.md
```

## Usage

### Basic Setup
1. Open `index.html` in a modern web browser
2. Click anywhere to activate audio context
3. Use the interface to play instrument sounds and detection effects
4. If and only if you are a ghost player, just scan the qr code that reddirect you into a netlify page

### For Board Game Integration
- **Ghost Players**: Use instrument buttons to play sounds when performing in-game actions
- **Detection System**: Use power level buttons (1-3) to provide audio feedback for Johnny's scanning actions
- **Atmosphere**: Let the app run in background for ambient gothic atmosphere

## Audio Files (Optional)

To use custom audio files instead of synthesized sounds:
1. Create a `sounds/` directory
2. Add MP3 files with these exact names:
   - `VIOLIN.mp3`
   - `DRUMS.mp3` 
   - `SAXOPHONE.mp3`
   - `TRUMPET.mp3`
   - `FLUTE.mp3`
   - `CLARINETTE.mp3`

If audio files are not found, the app automatically uses synthesized alternatives.

## Browser Compatibility

- **Recommended**: Chrome, Firefox, Safari, Edge (latest versions)
- **Requirements**: Web Audio API support
- **Note**: Audio autoplay policies require user interaction before audio can play

## Game Integration Notes

This web app serves as an atmospheric companion to the physical board game. While it provides audio feedback and ambiance, the core game mechanics (hidden movement, scanning, capturing) are handled through the physical board game components.

## Development

The application is built with vanilla HTML, CSS, and JavaScript:
- **No external dependencies** (except Google Fonts)
- **Self-contained**: Single HTML file with embedded CSS/JS
- **Responsive design**: Works on desktop and mobile devices

## License

This web app is a companion tool for the Possession Sonata board game. Please respect the intellectual property of the original game design.

---

*Developed as a companion app for Possession Sonata board game*