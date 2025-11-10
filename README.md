# 🐝 Beehive Construction Simulation

An interactive, real-time simulation of honeybee colony behavior and honeycomb construction. Watch as virtual bees build hexagonal cells, store honey, and maintain their hive with realistic behavioral patterns.

**Created by Kyros Koh**

![Beehive Simulation](https://img.shields.io/badge/JavaScript-Vanilla-yellow) ![HTML5 Canvas](https://img.shields.io/badge/HTML5-Canvas-orange) ![License](https://img.shields.io/badge/license-MIT-blue)

## 🌐 Live Demo

**[View Live Demo](https://kyroskoh.github.io/beehive-simulation/)** 🚀

## ✨ Features

### 🏗️ Dynamic Honeycomb Construction
- **Hexagonal Grid System**: Authentic hexagonal cell structure radiating from the center
- **Progressive Building**: Cells are constructed gradually, spreading outward from the hive center
- **Resource-Based Growth**: Construction speed depends on resource availability
- **Neighbor-Dependent Expansion**: New cells build faster when adjacent cells are complete

### 🐝 Realistic Bee Behavior
- **Autonomous Agents**: Each bee operates independently with its own decision-making
- **Task Switching**: Bees alternate between building, foraging, and honey storage
- **Pathfinding**: Smooth movement and navigation to target cells
- **Visual States**: Bees change color based on whether they're carrying resources (golden) or empty (orange)
- **Wing Animation**: Realistic flapping wing animation

### 🍯 Honey Storage System
- **Progressive Filling**: Cells fill with honey gradually as bees make multiple trips
- **Visual Feedback**: Cell color transitions from light yellow to deep orange as honey accumulates
- **Storage Indicators**: Small golden dots show honey levels within cells

### 🏠 Colony Management
- **Brood Cells**: Random cells are designated for raising young bees (shown in gray)
- **Cell States**: Empty, building, honey storage, and brood cell types
- **Age Tracking**: Each cell maintains its age and construction progress

### 🎮 Interactive Controls
- **Colony Size Slider**: Adjust the number of active bees (5-50 bees)
- **Resource Availability**: Control the rate of resource gathering (10-100%)
- **Hive Size Slider**: Set the maximum hive size (3-15 rings) with live resizing
- **Simulation Speed**: Control time flow (0.25x to 4x speed)
- **Individual Bee Tracking**: Click on any bee to follow its journey with visual tracking
- **Interactive Tooltips**: Hover over bees and cells to see detailed information
- **Pause/Resume**: Freeze the simulation at any moment
- **Reset Button**: Start fresh with a new hive
- **Clear Tracking**: Stop following the currently tracked bee

### 📊 Real-Time Statistics
- **Total Cells**: Count of fully constructed hexagonal cells
- **Honey Cells**: Number of cells containing stored honey
- **Hive Size**: Current radius of the hive in rings
- **Active Bees**: Current bee population in the colony

### 🎨 Beautiful UI
- Modern gradient background with purple gradients
- Smooth animations and transitions for all cell type changes
- Responsive design
- Color-coded legend for cell types
- Professional stat displays with 4 key metrics
- Real-time interactive tooltips with detailed information
- Visual tracking indicators (golden rings and lines)
- Dynamic speed control feedback

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, or Edge)
- No server or dependencies required!

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/kyroskoh/beehive-simulation.git
   cd beehive-simulation
   ```

2. **Open in browser**
   Simply open `index.html` in your web browser:
   - Double-click the file, or
   - Right-click and select "Open with" → your browser, or
   - Use a local server:
     ```bash
     # Python 3
     python -m http.server 8000
     
     # Python 2
     python -m SimpleHTTPServer 8000
     
     # Node.js (with http-server)
     npx http-server
     ```
   Then navigate to `http://localhost:8000`

### GitHub Pages Deployment

This project includes a GitHub Actions workflow for automatic deployment to GitHub Pages.

**To enable GitHub Pages:**

1. Go to your repository on GitHub
2. Navigate to **Settings** → **Pages**
3. Under "Build and deployment":
   - Source: Select **GitHub Actions**
4. Push to your `main` or `master` branch
5. The workflow will automatically deploy your site
6. Your site will be available at: `https://kyroskoh.github.io/beehive-simulation/`

The deployment happens automatically on every push to the main branch, or you can manually trigger it from the Actions tab.

## 🎯 How to Use

1. **Observe the Construction**: Watch as bees start building from the center cell outward
2. **Adjust Colony Size**: Use the slider to add or remove bees and see how it affects construction speed
3. **Change Resources**: Modify resource availability to simulate different environmental conditions:
   - Low resources (10-30%): Slow construction, bees carry less honey
   - Medium resources (40-60%): Balanced growth
   - High resources (70-100%): Rapid expansion and honey production
4. **Adjust Hive Size**: Set the maximum number of rings for your hive (3-15 rings)
   - Smaller hives (3-5 rings): Quick completion, compact colonies
   - Medium hives (6-10 rings): Balanced simulation
   - Large hives (11-15 rings): Expansive colonies, longer build times
5. **Control Speed**: Adjust simulation speed for different viewing experiences:
   - Slow motion (0.25x-0.75x): Study bee behaviors in detail
   - Normal speed (1.0x): Real-time simulation
   - Fast forward (1.25x-4x): Watch colony expansion rapidly
6. **Track Individual Bees**: Click on any bee to follow its journey
   - Golden ring appears around the tracked bee
   - Lines show the bee's current target destination
   - Click "Clear Tracking" to stop following
7. **Explore with Tooltips**: Hover over bees and cells to see:
   - Bee information: state, carrying status, speed, position
   - Cell information: type, build progress, honey level, age, coordinates
8. **Monitor Progress**: Keep track of statistics in the bottom panel:
   - Total Cells, Honey Cells, Hive Size (rings), Active Bees
9. **Pause/Resume**: Click the pause button to study the hive structure at any moment
10. **Reset**: Start over with a fresh hive to observe different growth patterns

## 🧬 Technical Details

### Architecture
- **Pure Vanilla JavaScript**: No frameworks or libraries required
- **HTML5 Canvas**: All rendering done with native Canvas API
- **Hexagonal Coordinates**: Uses axial coordinate system (q, r) for hex grid
- **Animation Loop**: Powered by `requestAnimationFrame` for smooth 60 FPS performance
- **Event-Driven Interactions**: Real-time mouse tracking, click handlers, and hover detection
- **Performance Optimized**: Efficient collision detection and rendering for large colonies

### Key Algorithms

#### Hexagonal Grid Generation
```javascript
// Generates concentric rings of hexagons around center point
// Uses axial coordinate system for efficient neighbor calculations
```

#### Bee AI States
- **Exploring**: Looking for cells to work on
- **Building**: Constructing new cells
- **Storing**: Depositing honey in completed cells

#### Construction Logic
- Center cells build automatically
- Outer cells require built neighbors before construction begins
- Build rate scales with resource availability
- Progress tracked per cell (0.0 to 1.0)

### Cell Types
| Type | Color | Description |
|------|-------|-------------|
| Empty | Light yellow | Completed but empty cell |
| Honey | Yellow to Orange | Contains stored honey (color intensity indicates fill level) |
| Brood | Gray | Cell designated for raising larvae |
| Building | Translucent | Cell under construction |

## 🎨 Customization

You can easily customize the simulation by modifying these variables in the JavaScript code:

```javascript
const config = {
    hexSize: 15,              // Size of each hexagonal cell
    centerX: canvas.width / 2,
    centerY: canvas.height / 2,
    colonySize: 10,           // Starting number of bees
    resourceAvailability: 50, // Starting resource level
    maxRings: 8,              // Maximum hive size (number of rings)
    simulationSpeed: 1.0      // Simulation time multiplier (0.25x to 4x)
};
```

### Color Schemes
Modify the cell colors in the `drawCell()` function:
- Empty cells: `#fff4e6`
- Honey cells: `rgb(255, ${intensity}, 0)`
- Brood cells: `#E8E8E8`
- Bee colors: `#FFD700` (carrying) / `#FFA500` (empty)

## 🔬 Educational Value

This simulation demonstrates:
- **Swarm Intelligence**: Emergent behavior from simple individual rules
- **Spatial Organization**: Self-organizing hexagonal structures
- **Resource Management**: Balance between gathering and construction
- **Agent-Based Modeling**: Independent entities creating complex systems
- **Hexagonal Grids**: Mathematical concepts in coordinate systems

## ✨ New Features (Recently Added)

### Interactive Enhancements
- **🎮 Speed Control**: Adjust simulation speed from 0.25x (slow motion) to 4x (fast forward)
- **🔍 Individual Bee Tracking**: Click any bee to follow it with visual indicators
- **💬 Information Tooltips**: Hover over bees and cells for detailed real-time data
- **🎨 Smooth Transitions**: All cell type changes now fade smoothly between colors
- **📏 Live Hive Resizing**: Adjust hive size without interrupting the simulation
- **📊 Statistics Tracking**: Monitor colony metrics in real-time

### User Experience Improvements  
- Visual tracking with golden rings and target lines
- Detailed tooltips showing bee states, cell properties, and coordinates
- Non-disruptive hive expansion/contraction
- Speed-adjusted animations for all behaviors
- Clear tracking button to release followed bees

## 🐛 Known Behaviors

- Bees may occasionally cluster in certain areas (realistic bee behavior!)
- At very low resource levels (<15%), construction can be extremely slow
- With 50 bees and high resources, the hive expands rapidly
- At 4x speed, animations may appear choppy but simulation remains accurate

## 🛠️ Future Enhancements

Potential features for future versions:

### 🐝 Advanced Bee Behaviors
- [ ] **Queen bee** with special behaviors (laying eggs, royal jelly production)
- [ ] **Worker bee specialization** (foragers, nurses, builders, guards)
- [ ] **Bee lifecycle** (eggs → larvae → pupae → adult bees)
- [ ] **Waggle dance communication** - bees sharing resource locations
- [ ] **Scout bees** - exploring for new hive locations when overcrowded
- [ ] **Drone bees** - male bees with different behaviors

### 🌍 Environmental Factors
- [ ] **Seasonal resource variations** (spring bloom, summer abundance, winter scarcity)
- [ ] **Temperature simulation** affecting bee activity and metabolism
- [ ] **Weather system** (rain, storms reducing foraging efficiency)
- [ ] **Day/night cycle** with bees resting at night
- [ ] **Flower fields** - visual representation of resource locations
- [ ] **Nectar vs pollen** - different resource types with different purposes

### 🏰 Hive Management
- [ ] **Multiple hive types** (wild vs managed, different shapes)
- [ ] **Swarming behavior** - hive splitting when too large
- [ ] **Disease spread** (varroa mites, foulbrood) and hive health
- [ ] **Hive temperature regulation** (heating/cooling behaviors)
- [ ] **Ventilation behaviors** (bees fanning to regulate humidity)
- [ ] **Wax production** - visual representation of cell wall building

### ⚔️ Threats & Challenges
- [ ] **Predator system** (wasps, bears, birds attacking the hive)
- [ ] **Colony collapse disorder** simulation
- [ ] **Pesticide effects** on bee health and behavior
- [ ] **Resource scarcity events** forcing adaptive behaviors
- [ ] **Hive defense mechanisms** (guard bees, alarm pheromones)

### 🎮 User Interaction
- [x] **Individual bee tracking** - follow a specific bee's journey ✅
- [x] **Speed control** (slow motion, fast forward, real-time) ✅
- [ ] **Multiple hive competition** - side-by-side colonies
- [ ] **Click to place flowers** - interactive resource management
- [ ] **Beekeeper interventions** (adding supers, harvesting honey)
- [ ] **Camera controls** (zoom, pan for large hives)

### 📊 Data & Visualization
- [ ] **Statistics graphs** (population over time, honey production rates)
- [ ] **Heat maps** (activity levels, resource density, temperature)
- [ ] **Pollen collection visualization** with different flower colors
- [ ] **Export simulation data** (CSV, JSON for analysis)
- [ ] **Performance metrics** (efficiency scores, survival rates)
- [ ] **Achievement system** (milestones, challenges)

### 🎨 Visual & Audio Enhancements
- [ ] **Sound effects** (buzzing, building, ambient hive sounds)
- [ ] **Background music** with nature themes
- [ ] **Particle effects** (pollen clouds, nectar drops)
- [ ] **3D visualization option** - depth and perspective
- [ ] **Different art styles** (realistic, stylized, minimalist)
- [ ] **Animation polish** (bee landing, takeoff, cell capping)

### 💾 Technical Features
- [ ] **Save/load hive states** (localStorage, file export)
- [ ] **Time-lapse recording** (video export, GIF generation)
- [ ] **Sharing system** (share hive configurations, leaderboards)
- [ ] **Mobile responsive design** with touch controls
- [ ] **WebGL rendering** for performance with large hives
- [ ] **Multiplayer mode** - collaborative or competitive hive building

### 📚 Educational Features
- [x] **Information tooltips** on hover (cell details, bee states) ✅
- [ ] **Tutorial mode** explaining bee biology and behavior
- [ ] **Comparison mode** - test different parameters side-by-side
- [ ] **Research challenges** - scientific questions to explore
- [ ] **Real-world data integration** (actual bee colony statistics)
- [ ] **Classroom mode** with teaching resources

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 👤 Author

**Kyros Koh**

## 👏 Acknowledgments

- Inspired by the fascinating collective behavior of real honeybees
- Hexagonal coordinate system based on [Red Blob Games' guide](https://www.redblobgames.com/grids/hexagons/)
- Built with passion for nature and computational biology

## 📧 Contact

Have questions or suggestions? Feel free to open an issue or reach out!

---

**Enjoy watching your virtual bees build their hive! 🐝🍯**

