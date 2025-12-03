# Web114 Project Log

## HTML Files Index

### Root Directory

- [bootstrap_template.html](./bootstrap_template.html) - Bootstrap template
- [bt_template.html](./bt_template.html) - Bootstrap + jQuery starting template (Updated: 2025-11-05)
- [selecting.html](./selecting.html) - Psychological Test Application (Added: 2025-11-24)
- [comic_demo.html](./comic_demo.html) - Comic Scroll Effect Demo (Added: 2025-11-24)
- [demo_intersection.html](./demo_intersection.html) - IntersectionObserver visualizer and demo (Added: 2025-11-24)

### Basic HTML (basic-html/)
### Bootstrap (bt/)

### jQuery (jquery/)

- [jquery_basic.html](./jquery/jquery_basic.html) - jQuery basics
- [jquery02_detect_top_smooth_transition.html](./prompting/jquery02_detect_top_smooth_transition.html) - Detect top with smooth transition
- [jquery03_detect_top_html_first.html](./prompting/jquery03_detect_top_html_first.html) - Detect top (HTML first approach)
- [horizontal_nice.html](./horizontal/horizontal_nice.html) - Horizontal nice layout
- [horizontal_section.html](./horizontal/horizontal_section.html) - Horizontal section layout
### Video Projects (video-scroll/)
#### Scrolled Video Series
Update: created `video-scroll/video-triggered-wp2-text-over-video-title-page.html` - added landing section and 200vh theme layout with sticky 2x2 video grid; ensured background `video-section` videos continue playing while interacting/scrolling text and video areas (2025-11-12)
- [video-scrolled01.html](./video-scroll/video-scrolled01.html) - A fixed video followed by several content sections
- [video-scrolled02.html](./video-scroll/video-scrolled02.html) - Adding leading and ending sections
- [video-scrolled03.html](./video-scroll/video-scrolled03.html) - Only playing video in the sections after leading section and before ending section
- [video-scrolled04.html](./video-scroll/video-scrolled04.html) - Flying cards over video
- [video-scrolled05.html](./video-scroll/video-scrolled05.html) - Enhanced Performance

#### Triggered Video Series
- [video-triggered-cw01-bt.html](./video-scroll/video-triggered-cw01-bt.html) - Bootstrap template baseline for triggered video demos (Renamed: 2025-11-05)
- [video-triggered-cw02-better-video-control.html](./video-scroll/video-triggered-cw02-better-video-control.html) - Smoother JS-only play/pause via IntersectionObserver + rAF fallback (Renamed: 2025-11-05)
- [video-triggered-wp1-text-with-video.html](./video-scroll/video-triggered-wp1-text-with-video.html) - Triggered video with text (Renamed: 2025-11-05)
- [video-triggered-wp2-text-over-video.html](./video-scroll/video-triggered-wp2-text-over-video.html) - Triggered video with text overlay (Renamed: 2025-11-05)
- [video-triggered-wp2-text-over-video-title-page.html](./video-scroll/video-triggered-wp2-text-over-video-title-page.html) - Enhanced version with landing page and sticky 2x2 video grid layout (Added: 2025-11-12)
- [video-triggered-wp2-text-over-video-title02.html](./video-scroll/video-triggered-wp2-text-over-video-title02.html) - Cinematic intro with flip-card video reveal and auto-reset (Added: 2025-12-02)

### Parallax Scrolling
- [parallax-h1-section.html](./parallax/parallax-h1-section.html) - Parallax H1 section with jQuery scroll effects
- [parallax-pure-css.html](./parallax/parallax-pure-css.html) - Pure CSS parallax demo
- [parallax-storytelling-horizontal-chatgpt.html](./parallax/parallax-storytelling-horizontal-chatgpt.html) - Horizontal storytelling parallax (ChatGPT version) (Added: 2025-11-12)
- [parallax-storytelling-horizontal-copilot.html](./parallax/parallax-storytelling-horizontal-copilot.html) - Horizontal storytelling parallax (Copilot refined version) (Added: 2025-11-12)
- [mask-scroll-demo.html](./parallax/mask-scroll-demo.html) - Parallax mask effect with sticky scroll and mix-blend-mode (Added: 2025-11-24)

### Charts and Data Visualization (chart/)
- [chart01_hbar_copilot.html](./chart/chart01_hbar_copilot.html) - Horizontal bar chart (Miyazaki films)
- [chart02.html](./chart/chart02.html) - Line plot chart (Miyazaki films)
- [chart03.html](./chart/chart03.html) - Taiwan population horizontal bar chart (D3.js) (Added: 2025-12-03)

### Scrolled Opacity & Image Effects (scrolled-opacity/)
- [scrolled-opacity01-leading.html](./scrolled-opacity/scrolled-opacity01-leading.html) - Sticky image stacking with scroll-based opacity (Refactored: 2025-12-03)
- [scrolled-opacity02-spotlight.html](./scrolled-opacity/scrolled-opacity02-spotlight.html) - Spotlight effect with map zooming and panning (Refactored: 2025-12-03)
- [scrolled-img.html](./scrolled-opacity/scrolled-img.html) - Background image panning based on scroll position (Refactored: 2025-12-03)

### Interactive Maps
- [map02_topojson_d3_copilot.html](./map02_topojson_d3_copilot.html) - Taiwan county map with D3.js and TopoJSON, scroll-triggered interactions (Added: 2025-11-18)
- [map03_leaflet.html](./map03_leaflet.html) - Leaflet-based Taiwan city map with OpenStreetMap tiles and circle markers (Added: 2025-11-18)
- [map04_leaflet_topojson.html](./map04_leaflet_topojson.html) - Leaflet + TopoJSON Taiwan county area map with polygon boundaries (Added: 2025-11-18)

### 3D Visualization
- [earth.html](./earth.html) - Interactive 3D Globe with country data (Added: 2025-12-02)
- [globe-3d.html](./globe-3d.html) - Scroll-driven 3D flight path storytelling (Added: 2025-12-02)

---

## Project Features

### Latest: Interactive Taiwan Maps (Updated: 2025-11-18)

#### map02_topojson_d3_copilot.html
**Key Features:**
- **D3.js + TopoJSON Integration**: Renders Taiwan county boundaries from `county_moi.json`
- **Scroll-Triggered Interactions**: Map highlights cities as you scroll through content sections
- **Dynamic City Info Card**: Displays population, area, and features with smooth animations
- **Geo Projection**: Uses `d3.geoMercator()` for accurate Taiwan map projection
- **Responsive Positioning**: Info card positioned dynamically below highlighted counties using `getBBox()`

**Technologies:**
- D3.js v7.8.5 for SVG manipulation and geo projections
- TopoJSON v3.0.2 for compressed topology data
- Intersection Observer API for scroll detection
- Bootstrap 5 for layout (50% fixed map + 50% scrolling content)

#### map03_leaflet.html
**Key Features:**
- **Leaflet Map Library**: Interactive web mapping with OpenStreetMap tiles
- **City Markers**: Circle markers for Taipei, Taichung, and Kaohsiung
- **Range Circles**: 15km radius circles highlighting city areas
- **Smooth Animations**: `map.flyTo()` transitions when scrolling to city sections
- **Active State Styling**: Markers enlarge and change color when active

**Technologies:**
- Leaflet 1.9.4 for interactive mapping
- OpenStreetMap tile layers
- Custom CSS for marker styling
- Intersection Observer for scroll-based activation

#### map04_leaflet_topojson.html
**Key Features:**
- **Hybrid Approach**: Combines Leaflet's interactivity with TopoJSON county boundaries
- **Polygon Area Rendering**: All Taiwan counties displayed as colored polygons
- **Clickable Counties**: Click any county to jump to its description section
- **Hover Effects**: Counties highlight on mouseover with opacity and stroke changes
- **Active County Highlighting**: Current county shows with distinct color and thicker border
- **Popup Information**: Click counties to view names and features

**Technologies:**
- Leaflet 1.9.4 map engine
- L.geoJSON() for rendering TopoJSON features
- D3.js + topojson.js for data processing
- CartoDB light basemap for clean background
- Dynamic styling with county-specific colors

**Comparison:**
- **map02 (D3.js)**: Best for custom SVG styling and precise geo projections
- **map03 (Leaflet + Markers)**: Ideal for point-based city locations with real map tiles
- **map04 (Leaflet + TopoJSON)**: Perfect for area/polygon visualizations with full map interactivity

---

### Data Visualization with Charts (Updated: 2025-12-03)

#### chart01_hbar_copilot.html
**Key Features:**
- **Horizontal Bar Chart**: Top 10 Miyazaki films by box office revenue.
- **Animated Bars**: Gradient colors and sequential animation triggered by scroll.
- **Ranked Display**: Clear ranking with badges.

#### chart03.html
**Key Features:**
- **D3.js Integration**: Uses D3.js v7 for data binding and rendering.
- **Dynamic SVG Generation**: Creates SVG elements based on population data.
- **Scroll-Triggered Animation**: Bars grow and text positions adjust when entering the viewport.
- **Responsive Design**: Adapts to container width.

---

### Scrolled Opacity & Image Effects (Added: 2025-12-03)

#### scrolled-opacity01-leading.html
**Key Features:**
- **Sticky Stacking**: Images stack on top of each other using `position: sticky`.
- **Scroll-Based Opacity**: Images fade out sequentially as the user scrolls, revealing the next image.
- **Vanilla JS**: Lightweight implementation without jQuery.

#### scrolled-opacity02-spotlight.html
**Key Features:**
- **Spotlight Effect**: A map image moves and zooms to focus on specific areas based on the active text section.
- **Coordinate Mapping**: Uses `data-x`, `data-y`, and `data-scale` attributes to define viewports.
- **Smooth Transitions**: CSS transitions ensure smooth movement between focal points.

#### scrolled-img.html
**Key Features:**
- **Background Panning**: A large background image pans (translates) based on scroll position.
- **Interpolation**: Calculates intermediate background positions between defined keyframes (sections).
- **Visual Indicators**: Debug-like overlays show the current section boundaries.

---

### Parallax H1 Section Effects (Updated: 2025-11-11)

#### 1. parallax-h1-section.html (jQuery Implementation)
**Key Features:**
- Scroll-driven parallax effect using jQuery
- Throttled scroll event handler for performance optimization
- Dynamic `translateY` transformation on content layers
- Multiple parallax sections with different background images
- Smooth transitions between sections

**Technologies:**
- jQuery 3.7.1 for scroll event handling
- Custom throttle function for performance
- CSS transforms with JavaScript control
- Responsive viewport-based calculations

#### 2. parallax-h1-section-pure-css.html (Pure CSS Implementation)
**Key Features:**
- Pure CSS parallax using `perspective` method
- No JavaScript required for parallax effect
- GPU-accelerated transformations
- `translateZ(-1px)` for background depth
- `scale(2)` compensation for perspective scaling
- Smoother performance than JS-based approach

**Technologies:**
- CSS `perspective: 1px` for depth effect
- CSS `transform-style: preserve-3d`
- 3D CSS transforms (`translateZ`)
- Pure CSS parallax scrolling

**Comparison:**
- **JS Version**: More control, customizable speed, wider browser support
- **CSS Version**: Better performance, simpler code, GPU-accelerated, modern browsers only

---

### Scrolled Video with Flying Cards (video-scrolled04.html)

**Key Features:**
- Sticky video background
- 3:6:3 Bootstrap Grid layout with flying cards
- Video starts playing when entering viewport at 50vh
- Smooth scroll-controlled video playback
- Leading and ending sections with dark background
- Responsive card layout with semi-transparent backgrounds

**Technologies:**
- HTML5 Video API
- Bootstrap 5 Grid System
- jQuery Scroll Events
- CSS Sticky Positioning
- Flexbox Centering

---

---

### Psychological Test Application (Added: 2025-11-24)

#### selecting.html
**Key Features:**
- **Complete User Flow**: Hero -> Intro -> Test -> Demographics -> Results.
- **Dynamic Questionnaire**: Generates questions from data arrays.
- **Data Processing**: Calculates score, age, and zodiac sign from user input.
- **Interactive UI**:
  - Smooth scrolling between sections.
  - Animated transition overlay displaying age and zodiac before results.
  - 5 distinct result states based on score ranges.
- **Visual Design**: Color-coded sections and responsive layout.

**Technologies:**
- Vanilla JavaScript (ES6+)
- CSS Custom Properties (Variables)
- Flexbox for layout
- `scrollIntoView` for navigation

---

### Comic Scroll Demo (Added: 2025-11-24)

#### comic_demo.html
**Key Features:**
- **Scroll-Triggered Animations**: Panels fade in and slide up as they enter the viewport.
- **Immersive Reading Experience**: Vertical layout mimicking webtoons.
- **Performance**: Uses `IntersectionObserver` for efficient scroll detection.

**Technologies:**
- `IntersectionObserver` API
- CSS Transitions (`opacity`, `transform`)

---

### Intersection Observer Demo (Added: 2025-11-24)

#### demo_intersection.html
**Key Features:**
- **Interactive Controls**: Real-time adjustment of `threshold` and `rootMargin`.
- **Visual Feedback**:
  - **Effective Root Area**: Visualizes the `rootMargin` as a dashed box overlay.
  - **Target Status**: Changes color and displays current intersection ratio.
- **Educational Tool**: Demonstrates how `IntersectionObserver` triggers based on scroll position and margin settings.

**Technologies:**
- Vanilla JavaScript `IntersectionObserver` API
- CSS Variables for theming
- Dynamic DOM manipulation for visualizers

---

### Parallax Mask Demo (Added: 2025-11-24)

#### mask-scroll-demo.html
**Key Features:**
- **Sticky Positioning**: Uses `position: sticky` to keep the visual area fixed while scrolling.
- **Scroll Mapping**: Maps vertical scroll progress to horizontal animation.
- **CSS Masking**: Utilizes `mix-blend-mode: screen` to create a see-through text effect where black text reveals the background image.
- **3-Layer Architecture**:
  1.  **Outer Track**: 300vh scrollable area.
  2.  **Middle Layer**: Sticky container with fixed background image.
  3.  **Inner Mask**: 400vw wide layer with white background and black text.

**Technologies:**
- CSS `mix-blend-mode`
- CSS `position: sticky`
- Vanilla JavaScript Scroll Event
- Bootstrap 5 for layout

---

### Cinematic Video Reveal (Added: 2025-12-02)

#### video-triggered-wp2-text-over-video-title02.html
**Key Features:**
- **Cinematic Intro Sequence**:
  - Scroll locked initially.
  - Sequential fade-in of Title, Subtitle, and Scroll Hint.
  - Animated SVG Arrow guiding user to scroll.
- **Flip-Card Video Reveal**:
  - 4 full-width (25%) transparent panels.
  - Cards flip open to reveal videos when the section touches the top of the viewport.
  - Videos play automatically upon reveal.
- **State Reset**:
  - Scrolling back to the top resets the flip cards to their closed state, ready for re-triggering.

**Technologies:**
- CSS 3D Transforms (`rotateY`, `perspective`)
- `IntersectionObserver` with `rootMargin` for precise top-border triggering.
- CSS Keyframe Animations for the arrow.
- JavaScript for sequence control and state management.

---

---

### 3D Visualization (Added: 2025-12-02)

#### earth.html
**Key Features:**
- **Interactive 3D Globe**: Built with `globe.gl`, featuring realistic textures (Blue Marble, Topology, Night Sky).
- **Country Data**: Displays country names in Traditional Chinese upon clicking.
- **Auto-Rotation**: Smoothly rotates until user interaction.
- **Visual Customization**: Highlights selected countries with custom polygon colors.

**Technologies:**
- `globe.gl` (Three.js wrapper)
- GeoJSON/TopoJSON data integration

#### globe-3d.html
**Key Features:**
- **Scroll-Driven Storytelling**: Controls the globe's camera and animation based on scroll position.
- **Flight Path Animation**: Visualizes a flight route from New York to Taiwan with intermediate stops (London, Paris, etc.).
- **Dynamic Camera Control**: Zooms out and in (parabolic altitude) while traversing the path.
- **Progress Tracking**: Updates an info panel with current location, next destination, and flight progress percentage.

**Technologies:**
- `globe.gl`
- Scroll event mapping to 3D coordinates
- Dynamic arc and point rendering

---

*Last updated: 2025-12-02*
