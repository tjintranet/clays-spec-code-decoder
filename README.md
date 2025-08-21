# Clays Specification Code Decoder

A web application for decoding print production specification codes used in the printing and publishing industry. This tool provides detailed breakdowns of multi-character codes that define product types, colour configurations, finishing options, material weights, and special processes.

## Features

### **Code Decoding**
- Real-time specification code validation and interpretation
- Support for 6-12 character codes
- Character-by-character breakdown with detailed explanations
- Error detection for invalid or unknown codes

### **Interactive Visualization**
- Visual representation of each character in the code
- Click-to-highlight functionality for easy reference
- Position indicators showing character sequence
- Color-coded results (green for valid, red for errors)

### **Smart Processing**
- Multi-character code recognition (e.g., "BE", "PB", "S1")
- Auto-uppercase input conversion
- Enter key support for quick decoding
- One-click field clearing on focus

### **Export & Share**
- Copy complete specifications to clipboard
- Formatted output ready for documentation
- Visual feedback for successful operations

### **Responsive Design**
- Mobile-friendly interface
- Bootstrap-based styling
- Consistent with modern web standards
- Professional appearance suitable for business use

## Specification Code Structure

The application decodes codes with the following character positions:

| Position | Description | Examples |
|----------|-------------|----------|
| **1st** | Product Type | C=Cover, W=Cover with Flaps, J=Jacket, T=Tip-In, F=Cover For Case |
| **2nd** | Colours (Outside) | 0=No Colour, 1-9=Various colour combinations |
| **3rd** | Colours (Inside) | 0=No Colour, 1-9=Various colour combinations |
| **4th** | Type of Finish | 0-9, A-Z=Different laminations, varnishes, UV treatments |
| **5th** | Surface Texture | P=Plain, G=Grained |
| **6th** | Material Weight | 1-7=Different GSM weights (130-265 gsm) |
| **7th-9th** | Special Processes | F=Fluorescent, BE=Block & Emboss, etc. |

## Usage Examples

### Basic 6-Character Codes
- `C45LP1` - Cover, 4 process + 1 self outside, 4 process inside, Gloss Spot UV, Plain, 190gsm
- `W20MP2` - Cover with Flaps, 2 self outside, no colour inside, Matt Spot UV, Plain, 220gsm
- `J11GP4` - Jacket, 1 self both sides, Grained, Plain, 150gsm

### Extended Codes with Special Processes
- `C45LP1F` - Basic code + Fluorescent ink
- `W23MP2BE` - Basic code + Block & Emboss (same pass)
- `T11GP4S1` - Basic code + Other Spot UV

## Technical Details

### Technology Stack
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Bootstrap 5.3.2, Bootstrap Icons
- **Browser Support**: Modern browsers with ES6 support
- **Dependencies**: None (all libraries loaded via CDN)

### File Structure
```
├── index.html          # Main application file
├── README.md           # This documentation
└── favicon files       # Optional favicon assets
```

### Browser Compatibility
- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Installation & Setup

1. **Download the Files**
   ```bash
   # Clone or download the repository
   git clone [repository-url]
   cd clays-specification-decoder
   ```

2. **Deploy to Web Server**
   - Upload `index.html` to your web server
   - Optionally add favicon files for branding
   - Access via web browser

3. **Local Development**
   ```bash
   # Simple local server using Python
   python -m http.server 8000
   
   # Or using Node.js
   npx http-server
   ```

4. **Access the Application**
   - Open `http://localhost:8000` in your browser
   - Or simply open `index.html` directly in a modern browser

## Code Specifications Reference

### Product Types (1st Character)
| Code | Description |
|------|-------------|
| C | Cover |
| W | Cover with Flaps |
| J | Jacket |
| T | Tip-In |
| F | Cover For Case |

### Colour Configurations (2nd & 3rd Characters)
| Code | Description |
|------|-------------|
| 0 | No Colour Print |
| 1 | 1 Self Colour |
| 2 | 2 Self Colour |
| 3 | 3 Self Colour |
| 4 | 4 Process Colours |
| 5 | 4 Process Colours + 1 Self Colour |
| 6 | 4 Process Colours + 2 Self Colour |
| 7 | 4 Self Colours |
| 8 | 4 Process Colours + 3 Self Colours |
| 9 | 4 Process Colours + 4 Self Colours |

### Material Weights (6th Character)
| Code | GSM |
|------|-----|
| 1 | 190 gsm |
| 2 | 220 gsm |
| 3 | 265 gsm |
| 4 | 150 gsm |
| 5 | 135 gsm |
| 6 | 130 gsm |
| 7 | 230 gsm |

### Special Processes (7th-9th Characters)
| Code | Description |
|------|-------------|
| F | Fluorescent |
| S | Self Colour |
| M | Non-Conventional Metallic |
| K | Conventional Metallic (used with M) |
| B | Blocked (after print, before laminate) |
| E | Embossed |
| D | Debossed |
| C | Die-Cutting |
| P | Print Over Foil |
| L | Block Over Laminate |
| U | Uncoated Printing |
| BE | Block & Emboss (same pass) |
| DE | Deboss & Emboss (same pass) |
| BD | Block & Deboss (same pass) |
| PB | Print Black Over Foil |
| S1 | Other Spot UV |
| S2 | Pile Spot UV |
| S3 | Glitter Spot UV |
| V1 | Glow Varnish |
| H1 | Holographic Lam |

## Contributing

To update the specification codes:

1. Modify the `specData` object in the JavaScript section
2. Add new codes following the existing pattern
3. Test with various code combinations
4. Update this documentation as needed

## Support

For technical issues or specification questions:
- Check the browser console for error messages
- Verify code format (6+ characters minimum)
- Ensure all characters are valid according to the specification

## License

This project is designed for internal business use in the printing and publishing industry.