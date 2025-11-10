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
- **👑 Queen Bee**: Special royal bee with unique behaviors:
  - Lays eggs in brood cells automatically
  - Produces royal jelly for developing larvae
  - Moves slowly around hive center
  - Distinctive pink/magenta color with golden crown
  - Tracks eggs laid and royal jelly production
- **Worker Bee Specialization**: Five distinct bee types with unique behaviors:
  - **Foragers** (35%): Fast-moving bees focused on collecting nectar and pollen, perform waggle dances
  - **Builders** (30%): Specialized in constructing new cells efficiently
  - **Nurses** (20%): Care for brood cells and tend to larvae
  - **Scouts** (7%): Explore hive edges and beyond when overcrowded, searching for expansion areas
  - **Drones** (8%): Male bees that wander around the hive, don't perform work tasks
- **Bee Lifecycle System**: Complete lifecycle simulation:
  - **Eggs**: Laid by queen in brood cells (light yellow)
  - **Larvae**: Develop from eggs, fed by nurses (light orange)
  - **Pupae**: Transform in cocoons (light purple)
  - **Adult Bees**: Emerge as new workers, join the colony
  - Each stage progresses automatically with visual indicators
- **Royal Jelly Production**: Queen produces royal jelly for developing bees (golden sparkles)
- **Type-Specific Efficiency**: Each bee type has optimized performance in their specialty
- **Autonomous Agents**: Each bee operates independently with its own decision-making
- **Task Switching**: Bees adapt their tasks based on colony needs
- **Pathfinding**: Smooth movement and navigation to target cells
- **Visual Identification**: Bees colored by type (golden/orange foragers, dark orange builders, green nurses, sky blue scouts, brown drones)
- **Wing Animation**: Realistic flapping wing animation
- **Bee Naming System**: Each bee gets a unique random name or ID
  - Names appear in tooltips, tracked stats, and cell activity panels
  - Configurable naming formats (numbers, names, or mixed)
  - Names help identify and track individual bees throughout the simulation
- **Waggle Dance Communication**: Foragers perform dance movements when finding good resources
  - Dancing bees share resource locations with nearby foragers
  - Other bees can learn about resources from dances
  - Visual dance animation with golden indicator rings
- **Scout Bees**: Specialized explorers that activate when hive is overcrowded
  - Detect overcrowding automatically (bees per cell ratio)
  - Explore edges of hive and beyond for expansion opportunities
  - Sky blue color with triangular marker for easy identification
- **Drone Bees**: Male bees with unique non-working behavior
  - Wander around hive in circular patterns
  - Occasionally approach queen bee
  - Larger size and brown color, distinctive large eyes
  - Don't perform work tasks (no foraging, building, or nursing)

### 🍯 Honey Storage System
- **Progressive Filling**: Cells fill with honey gradually as bees make multiple trips
- **Visual Feedback**: Cell color transitions from light yellow to deep orange as honey accumulates
- **Storage Indicators**: Small golden dots show honey levels within cells

### 🏠 Colony Management
- **Brood Cells**: Random cells are designated for raising young bees (shown in gray)
- **Lifecycle Cells**: Cells containing developing bees (eggs, larvae, pupae)
- **Cell States**: Empty, building, honey storage, brood, egg, larva, and pupa cell types
- **Age Tracking**: Each cell maintains its age and construction progress
- **Population Growth**: New bees emerge from pupae, expanding the colony naturally
- **Royal Jelly**: Special substance produced by queen for developing bees
- **Swarming Behavior**: When hive becomes overcrowded (bees/cell ratio > 0.9), 30-40% of workers leave to form a new colony
- **Temperature Regulation**: Bees automatically cluster when cold or fan when hot to maintain optimal hive temperature (~35°C)

### 🌍 Environmental Factors
- **Seasonal Variations**: Automatic cycling through spring, summer, fall, and winter
  - **Spring**: 20% resource bonus (bloom season)
  - **Summer**: Normal resource availability
  - **Fall**: 20% resource reduction (scarcity)
  - **Winter**: 50% resource reduction (very scarce)
- **Temperature Effects**: Ambient temperature affects bee activity levels
  - **Optimal Range**: 20-30°C (100% activity)
  - **Cold Weather**: Below 20°C reduces activity (minimum 30% at 0°C)
  - **Hot Weather**: Above 30°C reduces activity (minimum 50% at 45°C)
- **Day/Night Cycle**: Automatic day and night transitions
  - **Day**: Full bee activity (100%)
  - **Night**: Reduced activity (30% - most bees rest)
  - **Visual**: Background changes from light yellow (day) to dark blue-gray (night)
- **Hive Temperature Regulation**: Bees maintain internal hive temperature
  - **Too Cold**: Bees cluster together to generate heat
  - **Too Hot**: 10% of bees stop working to fan and cool the hive
  - **Visual Indicator**: Fanning bees show blue circular indicator with rapid wing movement

### 🎮 Interactive Controls
- **Colony Size Slider**: Adjust the number of active bees (5-50 bees)
- **Resource Availability**: Control the rate of resource gathering (10-100%)
- **Hive Size Slider**: Set the maximum hive size (3-15 rings) with live resizing
- **Simulation Speed**: Control time flow (0.25x to 4x speed)
- **Temperature Control**: Adjust ambient temperature (0-45°C) affecting bee activity
- **Swarming Toggle**: Enable/disable automatic hive splitting when overcrowded
- **Bee Naming**: Enable/disable random names for bees with configurable formats
  - **Mixed Format**: Combination of numbers (e.g., `forager#001`) and names (e.g., `forager-ben`)
  - **Numbers Only**: Sequential IDs like `forager#001`, `builder#002`, `nurse#003`
  - **Names Only**: Random names like `forager-honey`, `builder-buzz`, `nurse-amber`
- **Individual Bee Tracking**: Click on any bee to follow its journey with visual tracking
- **Interactive Tooltips**: Hover over bees and cells to see detailed information (including bee names)
- **Pause/Resume**: Freeze the simulation at any moment
- **Reset Button**: Start fresh with a new hive
- **Clear Tracking**: Stop following the currently tracked bee

### 📊 Real-Time Statistics
- **Total Cells**: Count of fully constructed hexagonal cells
- **Honey Cells**: Number of cells containing stored honey
- **Hive Size**: Current radius of the hive in rings
- **Active Bees**: Current bee population (grows as new bees emerge)
- **Lifecycle Tracking**: Visual indicators for eggs, larvae, and pupae
- **Environmental Stats**: Current season, temperature, day/night status, and hive temperature
- **Growth Trends Chart**: Live mini-graph showing colony growth over time
  - Purple line: Total cells built
  - Gold line: Honey cells filled
  - Updates every 5 frames for smooth visualization

### 🎨 Beautiful UI
- Modern gradient background with purple gradients
- Smooth animations and transitions for all cell type changes
- Responsive design
- Color-coded legend for cell types and bee types
- Professional stat displays with 4 key metrics
- **Dual side panels**: Left for cell stats, right for bee stats
- **Visual connections**: Dashed lines show bees targeting tracked cells
- Real-time interactive tooltips with detailed information
- Visual tracking indicators (golden rings for bees, blue glow for cells)
- Dynamic speed control feedback
- Default 0.25x speed for easier observation

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
6. **Track Individual Bees or Cells**: Click on any bee or cell to track it
   - **Bees** (Right Panel): Golden ring appears around the tracked bee (works even when paused!)
     - **Right side stats panel** shows real-time bee statistics:
       - Bee type, state, carrying status
       - Speed and efficiency with visual bars
       - Current position and target distance
       - Target cell coordinates
     - Lines show the bee's current target destination
   - **Cells** (Left Panel): Blue glow appears around the tracked cell
     - **Left side stats panel** shows real-time cell statistics:
       - Cell type, lifecycle stage (if applicable)
       - Build progress and honey level with visual bars
       - Lifecycle progress (for eggs, larvae, pupae)
       - Age, coordinates, and position
       - Royal jelly indicator (if present)
       - **Incoming bees**: Count and types of bees targeting this cell
       - **Nearby bees**: Bees within proximity of the cell
       - Visual lines connect tracked cell to incoming bees
   - **Independent Tracking**: Track a bee and a cell simultaneously - both panels can be visible at once
   - Stats update continuously for easy monitoring
   - Click another bee/cell to switch tracking, or click empty space to clear
   - Click "Clear Tracking" button to stop following both
   - Perfect for studying bee behavior and cell development simultaneously when simulation is paused
7. **Explore with Tooltips**: Hover over bees and cells to see:
   - Bee information: type (Forager/Builder/Nurse), state, carrying status, speed, efficiency, position
   - Cell information: type, build progress, honey level, age, coordinates
8. **Observe Bee Specialization**: Watch how different bee types work:
   - **Queen Bee** (pink with crown): Lays eggs and produces royal jelly
   - **Foragers** (golden/orange): Fast movers collecting resources
   - **Builders** (dark orange): Focused on cell construction
   - **Nurses** (green): Tending to brood cells and developing bees
9. **Watch Bee Lifecycle**: Observe the complete development process:
   - Queen lays eggs in brood cells (white circles)
   - Eggs develop into larvae (orange wiggly shapes)
   - Larvae transform into pupae (purple cocoons)
   - Adult bees emerge and join the colony
   - Royal jelly appears as golden sparkles on developing cells
10. **Monitor Growth Trends**: Check the mini-chart showing:
   - Colony expansion (purple line)
   - Honey production (gold line)
11. **Monitor Progress**: Keep track of statistics in the bottom panel:
   - Total Cells, Honey Cells, Hive Size (rings), Active Bees
   - Growth Trends chart showing historical data
12. **Pause/Resume**: Click the pause button to study the hive structure at any moment
13. **Reset**: Start over with a fresh hive to observe different growth patterns

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
| Brood | Gray | Cell designated for raising young bees |
| Egg | Light yellow | Contains a developing egg (white circle indicator) |
| Larva | Light orange | Contains a developing larva (orange wiggly shape) |
| Pupa | Light purple | Contains a developing pupa (purple cocoon shape) |
| Building | Translucent | Cell under construction |

### Bee Types
| Type | Color | Description |
|------|-------|-------------|
| Queen | Pink/Magenta | Royal bee that lays eggs and produces royal jelly |
| Forager | Golden/Orange | Fast-moving resource collectors, perform waggle dances |
| Builder | Dark Orange | Construction specialists |
| Nurse | Green | Caretakers for developing bees |
| Scout | Sky Blue | Explorers that search for expansion areas when overcrowded |
| Drone | Brown | Male bees that wander, don't perform work tasks |

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
    simulationSpeed: 0.25,     // Simulation time multiplier (0.25x to 4x)
    beeNaming: {
        enabled: true,        // Enable/disable bee naming
        format: 'mixed'       // 'number', 'name', or 'mixed'
    }
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
- **📈 Growth Trends Chart**: Live mini-graph showing colony expansion and honey production
- **🐝 Worker Specialization**: Five bee types (Foragers, Builders, Nurses, Scouts, Drones) with unique behaviors and colors
- **👑 Queen Bee**: Royal bee that lays eggs and produces royal jelly
- **🔄 Bee Lifecycle**: Complete development cycle from egg to adult bee
- **🌍 Environmental Factors**: Seasonal variations, temperature effects, and day/night cycles
- **🏰 Hive Management**: Automatic swarming and temperature regulation behaviors

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
- [x] **Worker bee specialization** (foragers, nurses, builders) ✅
- [x] **Queen bee** with special behaviors (laying eggs, royal jelly production) ✅
- [x] **Bee lifecycle** (eggs → larvae → pupae → adult bees) ✅
- [x] **Waggle dance communication** - bees sharing resource locations
- [x] **Scout bees** - exploring for new hive locations when overcrowded
- [x] **Drone bees** - male bees with different behaviors

### 🌍 Environmental Factors
- [x] **Seasonal resource variations** (spring bloom, summer abundance, winter scarcity) ✅
- [x] **Temperature simulation** affecting bee activity and metabolism ✅
- [ ] **Weather system** (rain, storms reducing foraging efficiency)
- [x] **Day/night cycle** with bees resting at night ✅
- [ ] **Flower fields** - visual representation of resource locations
- [ ] **Nectar vs pollen** - different resource types with different purposes

### 🏰 Hive Management
- [ ] **Multiple hive types** (wild vs managed, different shapes)
- [x] **Swarming behavior** - hive splitting when too large ✅
- [ ] **Disease spread** (varroa mites, foulbrood) and hive health
- [x] **Hive temperature regulation** (heating/cooling behaviors) ✅
- [x] **Ventilation behaviors** (bees fanning to regulate humidity) ✅
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
- [x] **Statistics graphs** (population over time, honey production rates) ✅
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

