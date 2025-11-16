# Standalone Web Map Workshop: Te Ara Hura Trail

This repository contains the materials for creating a standalone web map of **Te Ara Hura** (The Wandering Path) on Waiheke Island, Auckland, New Zealand. 

## Workshop Overview

This 3-hour workshop will guide you through creating your own standalone web map. By the end, you'll have a fully functional web map application that you can:
- Clone and customize for your own projects
- Host on GitHub Pages or any static hosting service
- Run entirely offline (no external dependencies)
- Share with others without requiring a server

## Map Context: Te Ara Hura

**Te Ara Hura** is a walking trail network on Waiheke Island, located in the Hauraki Gulf near Auckland, New Zealand. The trail offers beautiful coastal views and connects various parts of the island, making it an ideal subject for a web mapping workshop.

## Repository Structure

### Current Architecture (Initial Setup)

The repository starts with the following structure:

```
standalone_web_maps_foss4g2025/
├── README.md                    # This file
├── Caddyfile                    # Build and serve commands (uses Caddy)
├── lib/                         # Third-party libraries and resources (self-contained)
│   ├── maplibre-gl.5.10.0.js    # MapLibre GL JS library
│   ├── maplibre-gl.5.10.0.css   # MapLibre GL JS styles
│   └── pmtiles.4.3.0.js         # PMTiles library for tile serving
│   ├── fonts/                   # Noto Sans font files (for text rendering)
│   │   ├── Noto Sans Regular/
│   │   ├── Noto Sans Medium/
│   │   ├── Noto Sans Italic/
│   │   └── OFL.txt               # Open Font License
│   └── sprites/                  # Sprite sheets for map icons
│       ├── light.png
│       ├── light.json
|       ├── light@2x.png
│       └── light@2x.json   
└── sources/                     # Place to store source data files
```

### Final Architecture (After Workshop Completion)

By the end of the workshop, you will have this:

```
standalone_web_maps_foss4g2025/
├── README.md                    # This file
├── Caddyfile                    # Build and serve commands (uses Caddy)
├── index.html                   # Main HTML file for the web map (contains inline CSS and JavaScript)
├── style.json                   # MapLibre style specification (sources, layers, styling)
├── lib/                         # Third-party libraries (self-contained)
│   ├── maplibre-gl.5.10.0.js    # MapLibre GL JS library
│   ├── maplibre-gl.5.10.0.css   # MapLibre GL JS styles
│   ├── pmtiles.4.3.0.js         # PMTiles library for tile serving
│   ├── fonts/                   # Noto Sans font files (for text rendering)
│   │   ├── Noto Sans Regular/
│   │   ├── Noto Sans Medium/
│   │   ├── Noto Sans Italic/
│   │   └── OFL.txt               # Open Font License
│   └── sprites/                  # Sprite sheets for map icons
│       ├── light.png
│       ├── light.json
|       ├── light@2x.png
│       └── light@2x.json      
└── sources/                     # Source data files
    ├── waiheke_island.pmtiles   # PMTiles archive for Waiheke Island basemap - added in later steps
    └── te_ara_hura.geojson      # GeoJSON file for Te Ara Hura trail
```

## Technologies Used

- **MapLibre GL JS** (v5.10.0): Open-source map rendering library (fork of Mapbox GL JS)
- **PMTiles** (v4.3.0): Protocol for serving map tiles in a single archive file
- **HTML5/CSS3/JavaScript**: Standard web technologies
- **GeoJSON**: Vector data format for geographic features

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- A text editor or IDE
- Git (for cloning and version control)
- Basic familiarity with HTML, CSS, and JavaScript (helpful but not required)

### Setup Instructions

1. **Clone this repository** to your local machine:
   ```bash
   git clone <repository-url>
   cd standalone_web_maps_foss4g2025
   ```

2. **Fork the repository** to your own GitHub account so you can:
   - Save your customizations
   - Host your map on GitHub Pages
   - Share your finished project

3. **Serve the files locally** using the Makefile (which uses Caddy):
   ```bash
   make serve
   ```
   This will start a local web server using Caddy at `http://localhost:1234/`

4. **Open in your browser**: Navigate to `http://localhost:1234/` to see your map

## Workshop Goals

By the end of this workshop, you will:
- Understand the architecture of standalone web maps
- Learn how to integrate MapLibre GL JS into a web page
- Load and display GeoJSON data on a map
- Style map layers and customize the appearance
- Create interactive features (popups, tooltips, etc.)
- Understand the PMTiles format for efficient tile delivery
- Deploy your map to GitHub Pages or another hosting service

## Workshop Workflow

The workshop will proceed step by step, building the map application incrementally:

1. **Setup and Repository Structure** - Understanding the project structure
2. **Basic Map Display** - Creating your first map view
3. **Loading Source Data** - Adding the Te Ara Hura trail data
4. **Styling and Customization** - Making the map look great
5. **Interactivity** - Adding user interactions
6. **Polishing and Deployment** - Final touches and sharing your map

## File Descriptions

- **index.html**: The main HTML file containing the map container, inline CSS for styling, and JavaScript to initialize MapLibre
- **style.json**: MapLibre style specification defining data sources (GeoJSON, PMTiles) and layer styling
- **sources/**: Contains GeoJSON and PMTiles geographic data files for the map
- **lib/**: All third-party libraries (MapLibre, PMTiles), fonts, and sprites bundled locally (ensures offline functionality)

## Making It Your Own

After completing the workshop, feel free to:
- Replace the Te Ara Hura trail data with your own geographic features
- Customize the map style and colors
- Add your own interactive features
- Modify the design and layout
- Extend functionality with additional MapLibre GL JS features

## Resources

- [MapLibre GL JS Documentation](https://maplibre.org/maplibre-gl-js-docs/)
- [PMTiles Specification](https://github.com/protomaps/PMTiles)
- [GeoJSON Specification](https://geojson.org/)
- [Waiheke Island Information](https://www.waiheke.co.nz/)

## License

[Add your license information here - consider open source licensing for workshop materials]

## Workshop Instructor

This workshop is led by [Stephanie May](https://talks.osgeo.org/foss4g-2025/speaker/7A883D/), open source enthusiast, CNG board member, MapLibre board member, and cartographer at large.

Created for FOSS4G 2025 workshop attendees.

---

**Note**: This is a workshop repository. Feel free to fork, modify, and use it as a starting point for your own mapping projects!

