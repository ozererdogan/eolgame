# Electrical Safety Inspector Game

A browser-based educational game about electrical safety testing.

## Project Structure

```
electrical-safety-game/
├── index.html          # Main game file
├── config.json         # Game configuration (positions, equipment, etc.)
├── assets/            # Image folder
│   ├── electrician.png
│   ├── hand-cursor.png
│   ├── voltage-meter.png
│   ├── cables.png
│   ├── insulation-meter.png
│   ├── test-pass.png
│   ├── test-fail.png
│   ├── charger.png
│   └── factory-room.png (optional)
└── README.md          # This file
```

## Setup Instructions

1. Create a folder called `electrical-safety-game`
2. Put `index.html` and `config.json` in the root folder
3. Create a subfolder called `assets`
4. Put all your PNG images in the `assets` folder with these names:
   - `electrician.png` - Main character
   - `hand-cursor.png` - Cursor icon
   - `voltage-meter.png` - Handheld testing tool
   - `cables.png` - Colored cables
   - `insulation-meter.png` - Large testing equipment
   - `test-pass.png` - Green success screen
   - `test-fail.png` - Red failure screen
   - `charger.png` - Charging station
   - `factory-room.png` - Background (optional)

## How to Play Locally

1. Open `index.html` in any modern web browser
2. No server or build tools required!

## How to Host on GitHub Pages

1. Create a new repository on GitHub
2. Upload all files maintaining the folder structure
3. Go to Settings → Pages
4. Select "Deploy from main branch"
5. Your game will be live at: `https://your-username.github.io/repo-name`

## Configuration

All game settings are in `config.json`:

### Changing Image Positions
Edit the `x` and `y` values (percentages from left/top):
```json
"mainCharacter": {
  "x": 45,    // 45% from left
  "y": 55,    // 55% from top
  "width": 720,
  "height": 720
}
```

### Changing Equipment Test Areas
Edit equipment array to adjust clickable zones:
```json
{
  "id": "cabinet1",
  "name": "Cabinet Row 1",
  "x": 70,        // Position
  "y": 28,
  "width": 15,    // Size in % of screen
  "height": 8,
  "shouldPass": true  // Change to false to make it fail tests
}
```

### Changing Tool Positions and Sizes
```json
{
  "id": "voltageMeter",
  "name": "Voltage Meter",
  "x": 15,
  "y": 45,
  "size": 80     // Size in pixels
}
```

### Changing Test Result Display
```json
"testResultDisplay": {
  "x": 35,         // Center position
  "y": 35,
  "width": 264,    // 2x default size
  "height": 264
}
```

## Gameplay

1. Click on equipment to select it (charger, cabinet rows, test device)
2. Click on a tool to test the equipment
3. **WARNING**: Using the insulation meter causes an electrical fire!
4. Use voltage meter or cables for safe testing
5. Complete all tests to finish the inspection

## Customization Tips

- To change image files: Just replace the PNG files in the `assets` folder
- To adjust positions: Edit `config.json` - no code changes needed
- To add more equipment: Add entries to the `equipment` array in config
- To change which equipment passes/fails: Toggle `shouldPass` in config

## Browser Compatibility

Works in all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera

## License

Feel free to modify and use for educational purposes.
