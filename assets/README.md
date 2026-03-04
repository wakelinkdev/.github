# WakeLink Assets

Brand assets and logos for the WakeLink project.

## Logo Files

| File | Format | Colors | Usage |
|------|--------|--------|-------|
| `wakelink-logo.svg` | SVG | Brand colors | Primary logo (web/docs) |
| `wakelink-logo-black.svg` | SVG | Black | Light backgrounds |
| `wakelink-logo-white.svg` | SVG | White | Dark backgrounds |
| `wakelink-app-icon.svg` | SVG | White on `#0F1429` | App icons, main version |
| `wakelink-logo-circle-black.svg` | SVG | Black + white | Monochrome app icons |
| `wakelink-banner.svg` | SVG | White on `#0F1429` | GitHub Profile banner |
| `favicon.svg` | SVG | White on `#0F1429` | Website favicons |

## Android Resources

| File | Format | Purpose |
|------|--------|---------|
| `ic_launcher_foreground_branded.xml` | Vector Drawable | Android app icon (branded) |

## Logo Description

The WakeLink logo represents a WiFi signal with:
- **Dot**: The target device/computer
- **3 Waves**: WiFi signal strength/connectivity
- **Clean Design**: Modern, minimal aesthetic

## Brand Colors

| Color | HEX | RGB | Usage |
|-------|-----|-----|-------|
| **Primary** | `#6366F1` | `99, 102, 241` | Logo, accents, links |
| **Secondary** | `#10B981` | `16, 185, 129` | Success states, online indicators |
| **Background Dark** | `#0F1429` | `15, 20, 41` | Dark backgrounds, app icons |
| **Background Light** | `#F8FAFC` | `248, 250, 252` | Light backgrounds |
| **Text Dark** | `#0F1429` | `15, 20, 41` | Dark text on light |
| **Text Light** | `#F8FAFC` | `248, 250, 252` | Light text on dark |
| **Gray** | `#94A3B8` | `148, 163, 184` | Muted text, subtitles |

## Usage Guidelines

### Logo Placement
- Minimum clear space: 1/4 of logo height around logo
- Don't stretch or distort the logo
- Use appropriate contrast with background

### Colors
- Primary color `#6366F1` for all logo instances
- White `#FFFFFF` for dark backgrounds
- Maintain color consistency across all platforms

### File Formats
- Use **SVG** for web and scalable applications  
- Convert to PNG for specific size requirements
- Maintain aspect ratio in all conversions

## Favicon Generation

To generate favicons from the logo:

```bash
# Convert SVG to various PNG sizes
# 16x16, 32x32, 48x48, 96x96, 144x144, 192x192, 256x256, 512x512
```

## App Icons

For mobile applications, use `wakelink-logo-circle.svg` as base and follow platform guidelines:
- **Android**: Adaptive icons with proper padding
- **iOS**: Rounded corner requirements  
- **Desktop**: Platform-specific icon sizes
