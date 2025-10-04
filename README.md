# Image Color Palette Swap

A comprehensive web-based application for advanced image color manipulation, palette extraction, and real-time color replacement. Transform any image using 25+ professionally curated color palettes, each expanded to 75 unique tonal variations, with pixel-perfect precision and instant visual feedback.

*Developed with AI assistance to create an intuitive and powerful color manipulation tool.*

## Features
## Core Functionality

### 🎨 Advanced Color Extraction & Analysis
- **Intelligent K-Means Clustering**: Extracts up to 75 dominant colors using optimized sampling algorithms
- **Perceptual Color Matching**: Uses Delta E color distance calculations for accurate color replacement
- **Red-Black Tree Optimization**: Efficient color matching with O(log n) lookup performance
- **Color Similarity Merging**: Automatically combine similar colors with adjustable threshold (1-80%)
- **Hue-Based Organization**: Smart color sorting by hue, saturation, and lightness for intuitive palette management

### 🖼️ Interactive Image Manipulation
- **Unlimited Zoom & Pan**: Smooth navigation with mouse wheel zoom and click-drag panning
- **Real-Time Color Highlighting**: Click any extracted color to see exactly where it appears in the image
- **Pixel-Perfect Replacement**: Replace individual colors or entire palettes with visual confirmation
- **Live Image Adjustments**: 
  - Brightness control (-100 to +100)
  - Saturation enhancement (-100 to +100)
  - Color pop effects (0 to 100)
  - Shadow/highlight adjustment (-100 to +100)
- **Undo/Redo System**: 50-step history for all color modifications

### 🎭 Professional Palette Library (25+ Built-in Palettes)
**Art & Design**: Vibrant Spectrum, Muted Harmony, Pastel, Material Design, Flat UI, Tailwind CSS  
**Gaming & Fantasy**: RPG Essentials, Magic Fantasy, Dark Dungeon, Characters & Clothing  
**Nature & Environment**: Natural World, Tropical Paradise, Ancient Echoes, Village Architecture  
**Mood & Atmosphere**: Warm Tones, Cool Tones, Neon, Cyberpunk, Vaporwave, Retro  
**Specialized**: Grayscale, Earth Tones, Ocean, Forest, Desert, Autumn, Spring, Sunset, Vintage, Neutrals

### 🛠️ Custom Palette Management
- **Create from Images**: Save extracted colors as reusable palettes
- **Manual Palette Creation**: Build custom palettes from scratch (75 colors each)
- **Import/Export**: Share palettes via JSON files
- **Real-Time Editing**: Double-click any palette color to modify it instantly
- **Drag & Drop Reordering**: Organize extracted colors by dragging
- **Palette Replacement**: Replace entire image palettes with closest matches from any palette

### ⚡ Advanced Features
- **Batch Color Operations**: Replace all image colors with palette matches in one click
- **Image Download**: Export processed images with all adjustments applied
- **Keyboard Shortcuts**: 
  - `Ctrl+S`: Save current palette
  - `Ctrl+I`: Save image palette  
  - `Ctrl+R`: Replace with active palette
  - `Ctrl+Z/Y`: Undo/Redo
  - `Ctrl+E`: Export palettes
  - `Escape`: Clear highlights/exit modes
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Local Processing**: All operations happen in-browser - no data uploaded to servers
## Quick Start Guide

### Basic Workflow
1. **Load Image**: Upload any image file (JPG, PNG, GIF, WebP)
2. **Explore Colors**: View automatically extracted color palette (up to 75 colors)
3. **Interact**: 
   - Click extracted colors to highlight them in the image
   - Double-click extracted colors to enter replacement mode
   - Use zoom/pan to examine details
4. **Transform**: 
   - Select any built-in palette from 25+ options
   - Click "Replace with Palette" for instant transformation
   - Or manually replace individual colors by clicking palette colors during replacement mode
5. **Fine-tune**: Adjust brightness, saturation, color pop, and shadows in real-time
6. **Save**: Download the processed image or save custom palettes for future use

### Advanced Techniques
- **Color Merging**: Use the similarity threshold slider to combine similar colors automatically
- **Palette Creation**: Save extracted colors as custom palettes for consistent branding
- **Precision Editing**: Use replacement mode for surgical color changes
- **Batch Processing**: Import/export palette collections for workflow efficiency

## Technology Stack

- **HTML5 Canvas**: For image manipulation and rendering
- **Vanilla JavaScript**: Core functionality and color processing algorithms
- **CSS3**: Modern styling with CSS Grid and custom properties
- **File API**: For image upload and processing

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/JosephPotapenko/Image-Color-Pallet-Swap.git
   ```

2. Navigate to the project directory:
   ```bash
   cd Image-Color-Pallet-Swap
   ```

3. Open `index.html` in your web browser or serve it using a local server:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (if you have live-server installed)
   npx live-server
   ```

## Technical Architecture

### Project Structure
```
├── index.html          # Main application interface
├── script.js           # Core JavaScript functionality (2,947 lines)
├── styles.css          # Responsive CSS styling (427 lines)
├── favicons/          # Application icons and manifest
└── README.md          # Documentation
```

### Algorithm Details

**Color Extraction Engine**
- Mini K-means clustering with optimized sampling (max 20,000 pixels for performance)
- Perceptual color distance using weighted RGB calculations
- Red-Black tree data structure for O(log n) color matching
- Intelligent palette expansion: 25 base palettes → 75 tonal variations each

**Image Processing Pipeline**
- Canvas-based pixel manipulation with ImageData API
- Real-time cluster assignment and recoloring
- Non-destructive editing with complete undo/redo history
- Memory-efficient processing for images up to several megapixels

**Performance Optimizations**
- Adaptive sampling rates based on image size
- Efficient color space conversions (RGB ↔ HSL)
- Debounced real-time adjustments
- Local storage for palette persistence

## Use Cases & Applications

### Digital Art & Design
- **Character Design**: Use RPG and fantasy palettes for consistent character theming
- **Environment Art**: Apply natural world palettes for realistic landscapes
- **UI/UX Design**: Leverage Material Design, Flat UI, and Tailwind palettes for modern interfaces
- **Brand Development**: Create and maintain consistent color schemes across projects

### Photography & Image Processing
- **Color Grading**: Apply cinematic color palettes to photos
- **Artistic Filters**: Transform photos with vintage, neon, or cyberpunk aesthetics
- **Product Photography**: Ensure consistent branding colors across product images
- **Social Media**: Create cohesive visual themes for content

### Game Development
- **Asset Consistency**: Maintain unified color schemes across game sprites and textures
- **Mood Setting**: Apply dark dungeon or tropical paradise palettes for atmosphere
- **Pixel Art**: Use specialized palettes designed for retro gaming aesthetics

## Browser Support & Requirements

**Minimum Requirements:**
- Modern browser with HTML5 Canvas support (Chrome 51+, Firefox 54+, Safari 10+, Edge 79+)
- JavaScript ES6+ support
- File API for image uploads
- 512MB+ available RAM for large image processing

**Optimal Performance:**
- Desktop/laptop with 2GB+ RAM
- Hardware acceleration enabled
- Modern GPU for smooth zoom/pan operations

## Development & Contributing

### Local Development
```bash
# Clone the repository
git clone https://github.com/JosephPotapenko/Image-Color-Pallet-Swap.git
cd Image-Color-Pallet-Swap

# Serve locally (choose one method)
python -m http.server 8000        # Python
npx live-server                   # Node.js
php -S localhost:8000            # PHP
```

### Contributing Guidelines
- **New Palettes**: Add themed color collections to `BASE_PALETTES` object
- **Algorithm Improvements**: Enhance color extraction or matching algorithms  
- **UI/UX**: Improve responsive design and accessibility
- **Performance**: Optimize for larger images and mobile devices
- **Documentation**: Expand usage examples and technical details

## License & Credits

**MIT License** - Free for commercial and personal use

**Created with AI assistance** to deliver professional-grade color manipulation capabilities while maintaining an intuitive user experience.

---

### 🚀 **Ready to transform your images?** 
**No installation required** - runs entirely in your browser with complete privacy (no uploads to external servers).