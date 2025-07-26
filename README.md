# VJ System - p5.js Version

An audio-reactive 3D visual jockey system converted from Processing to p5.js. This system creates immersive 3D visuals that respond to microphone input, perfect for live performances, music visualization, and creative coding.

## Features

- **Audio-Reactive Visuals**: Real-time response to microphone input using FFT analysis
- **Multiple Visual Modes**: 3 different rendering modes with unique combinations of visual elements
- **3D Flocking Boids**: Animated particles with realistic flocking behavior
- **Dynamic Grid Patterns**: Audio-reactive 3D grid formations
- **Sine Wave Patterns**: Mathematical sine wave visualizations in 3D space
- **Strobe Effects**: High-contrast strobing synchronized with audio
- **Interactive Controls**: Keyboard shortcuts for real-time manipulation

## Visual Modes

### Mode 0: Boids + Grid
- Flocking boids with 3 different shape variations (spheres, cubes, rectangular prisms)
- 3D grid patterns with noise-based animations
- Combined audio-reactive movement

### Mode 1: Boids + Sine Waves
- Smaller flock of boids
- Sine wave-based 3D patterns with audio reactivity
- Smooth flowing animations

### Mode 2: Full System
- All visual elements combined
- Boids, grid patterns, and sine waves
- Maximum visual complexity

## Controls

- **SPACE**: Trigger strobe effect (inverts colors)
- **A**: Manually switch between visual modes
- **R**: Toggle global rotation effect
- **Auto-switching**: System automatically changes modes based on audio intensity

## Setup and Usage

1. **Download Files**: Download all files (`index.html`, `sketch.js`, `boid.js`, `grid.js`, `sine.js`)

2. **Serve Locally**: Due to browser security restrictions, you need to serve the files from a local server:
   
   **Using Python (recommended):**
   ```bash
   # Navigate to the folder containing the files
   cd /path/to/vj-system
   
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   ```
   
   **Using Node.js:**
   ```bash
   npx http-server -p 8000
   ```
   
   **Using PHP:**
   ```bash
   php -S localhost:8000
   ```

3. **Open in Browser**: Navigate to `http://localhost:8000` in your web browser

4. **Enable Audio**: Click the "Start Audio" button and allow microphone access when prompted

5. **Enjoy**: The visuals will respond to sound from your microphone!

## Technical Details

### Audio Processing
- Uses p5.sound library for microphone input and FFT analysis
- 11-band frequency analysis with custom filtering
- Real-time signal processing for smooth visual response

### Visual Elements
- **Boids**: Implements Reynolds' flocking algorithm with separation, alignment, and cohesion
- **Grid**: Noise-based 3D grid with rotation and audio-reactive positioning
- **Sine**: Mathematical sine wave patterns with 3D transformations

### Performance
- Optimized for real-time performance
- Adjustable parameters for different hardware capabilities
- Responsive design that adapts to window size

## Conversion Notes

This p5.js version converts the original Processing sketch with the following changes:

- **Audio**: Minim library → p5.sound library
- **3D Camera**: camera3D library → p5.js built-in 3D
- **Signal Processing**: signal.library → custom moving average filter
- **Syntax**: Processing → JavaScript/p5.js conventions
- **Classes**: Processing classes → ES6 JavaScript classes

## Browser Compatibility

- **Chrome/Chromium**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Supported with some limitations
- **Edge**: Full support

**Note**: Microphone access requires HTTPS in production or localhost for development.

## Troubleshooting

### No Audio Response
1. Check that microphone permissions are granted
2. Ensure audio input is working (test with other applications)
3. Try refreshing the page and clicking "Start Audio" again

### Performance Issues
1. Close other browser tabs to free up resources
2. Try reducing browser window size
3. Check browser console for error messages

### Visual Issues
1. Ensure WebGL is supported in your browser
2. Update graphics drivers if needed
3. Try a different browser

## Customization

You can customize the system by modifying:

- **Colors**: Edit the `clr1` array in `sketch.js`
- **Boid Count**: Adjust the numbers in `initializeBoids()` functions
- **Audio Sensitivity**: Modify `audioAmp` and related variables
- **Visual Complexity**: Change grid and sine wave parameters

## Credits

Original Processing sketch converted to p5.js. Features audio-reactive 3D graphics with flocking behavior, grid patterns, and sine wave visualizations.

## License

This project is open source. Feel free to modify and use for your creative projects! 