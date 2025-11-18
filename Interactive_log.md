# Interactive Development Session Log

**Session Date**: 2025-11-18 ~ 2025-11-19  
**Project**: Data Visualization & Interactive Maps with Taiwan Geographic Data

---

## Session 1: Data Visualization - Miyazaki Films Charts

### User Prompts
```
根據這個範例在 chart01 的地方繪製宮崎駿動畫的前10名票房的 horizontal bar
https://codepen.io/jirlong/pen/qBXQyLP

for #chart02, generate a line plot, while x-axis for year, and y-axis for sale

remember to update README.md
```

### Files Created
- **data01_hbar_copilot.html**

### Implementation Details
- **Chart 01 - Horizontal Bar Chart**:
  - Top 10 Miyazaki films by box office revenue
  - Animated bars with gradient colors (blue-green)
  - Sequential animation triggered by Intersection Observer
  - Ranked display with position badges
  
- **Chart 02 - Line Plot**:
  - SVG-based line chart with animated drawing effect
  - X-axis: Year (1986-2013)
  - Y-axis: Box office sales (億日圓)
  - Interactive data points with hover tooltips
  - Grid lines and axis labels

- **Layout**: Two-column sticky layout with Bootstrap 5

### Documentation Updated
- **README.md**: Added Data Visualization section with feature descriptions

---

## Session 2: Taiwan Map - D3.js + TopoJSON Implementation

### User Prompts
```
我希望 #chart01 是個 taiwan 縣市等級的 area map，
左側包含地圖的 <div> 會 sticky-top，
然後右側的 section 捲動到該縣市時，相對應的地圖會改變顏色，並浮現基本資料。

可否模仿 webScroll/d3/d3_areamap/d3_areamap_3.html 來重新繪製 map02.html

#cityInfoCard 可否出現在該縣市下方？
```

### Files Created/Modified
- **map02.html** → **map02_topojson_d3_copilot.html**

### Implementation Details
- Used D3.js v7.8.5 for SVG rendering
- TopoJSON v3.0.2 for county boundary data
- `d3.geoMercator()` projection for Taiwan map
- Scroll-triggered county highlighting with Intersection Observer
- Dynamic city info card positioned below counties using `getBBox()`

### Issues Resolved
- **Map not rendering**: Copied `county_moi.json` from webScroll directory to web114 directory
- **Info card positioning**: Changed to `position: absolute` with dynamic left/top based on `getBBox()`

---

## Session 3: Taiwan Map - Leaflet with City Markers

### User Prompt
```
可否用 leaflet 等套件，仿照 map02 的互動模式，建立一個 map03.html 的新的應用
```

### Files Created
- **map03_leaflet.html**

### Implementation Details
- Leaflet 1.9.4 with OpenStreetMap tiles
- Circle markers for Taipei, Taichung, and Kaohsiung
- 15km radius circles highlighting city areas
- `map.flyTo()` animations when scrolling to city sections
- Active state styling with marker enlargement

---

## Session 4: Taiwan Map - Leaflet + TopoJSON Area Map

### User Prompt
```
可以建立一個 map04.html，仿照 map03_leaflet.html 的互動模式，
但改為呈現 area map（縣市區域地圖）嗎？
```

### Files Created
- **map04.html** → **map04_leaflet_topojson.html**

### User Prompt
```
可以建立一個 map04.html，仿照 map03_leaflet.html 的互動模式，
但改為呈現 area map（縣市區域地圖）嗎？
```

### Action Taken
- **Created**: `map04.html` (later renamed to `map04_leaflet_topojson.html`)
- **Implementation**:
  - Combined Leaflet map engine with TopoJSON county boundary data
  - Used `L.geoJSON()` to render Taiwan county polygons
  - Implemented D3.js + topojson.js for data processing
  - Added CartoDB light basemap for clean background
  - Set up hover effects and click interactions for counties
  - Created scroll-triggered highlighting system with Intersection Observer

---

## 2. Documentation Update

### User Prompt
```
update README.md
```

### Action Taken
- **Modified**: `README.md`
- **Changes**:
  - Added new "Interactive Maps" section
  - Documented three map implementations (map02, map03, map04)
  - Included feature comparison table
  - Listed technologies used for each map variant

---

## 3. Map Service Consultation

### User Prompt
```
還有其他常用的地圖服務嗎？
```

### Action Taken
- **Response**: Provided comprehensive overview of map services
- **Categories Covered**:
  - Commercial Services: Google Maps, Mapbox, HERE Maps
  - Open Source Libraries: OpenLayers, MapLibre GL JS
  - 3D Visualization: Cesium, Deck.gl
  - China Services: Baidu Maps, Amap
  - Taiwan Government: NLSC WMTS services
- **Recommendations**: Based on use case (free/commercial, simple/complex, 2D/3D)

---

## 4. Layout Optimization

### User Prompt
```
目前 map04 只用了左側一小塊區域來呈現地圖，
我希望整個左側的 <div> 都用來呈現地圖。
至於 InfoCard 可以呈現在地圖下方，或浮動在該縣市上方即可。
```

### Action Taken
- **Modified**: `map04_leaflet_topojson.html`
- **CSS Changes**:
  - Removed map title element
  - Changed `#map` to `width: 100%; height: 100%`
  - Changed `#map-container` to fill left 50% with `height: 100vh`
  - Modified `.city-info` to `position: absolute; bottom: 20px; left: 50%`
  - Added transform for centering: `transform: translateX(-50%)`
  - Enhanced shadow effects for floating card appearance

---

## 5. Highlight Functionality Debugging (Part 1)

### User Prompt
```
現在地圖是滿版的了，但是卻無法 highlight（高亮顯示）各個縣市。
```

### Action Taken
- **Modified**: `map04_leaflet_topojson.html`
- **JavaScript Changes**:
  - Added dynamic TopoJSON object name detection: `Object.keys(data.objects)[0]`
  - Added console.log statements for debugging
  - Implemented delayed initialization with `setTimeout(() => { highlightCity('台北市'); }, 500)`
  - Added error handling with `.catch()` for TopoJSON loading

---

## 6. Highlight Functionality Debugging (Part 2)

### User Prompt
```
現在可以 highlight 了，但除了第一個縣市（台北市）無法 highlight。
```

### Action Taken
- **Modified**: `map04_leaflet_topojson.html`
- **Intersection Observer Adjustments**:
  - Reduced `threshold` from `0.5` to `0.3`
  - Added `rootMargin: '0px 0px -30% 0px'` to improve first section detection
  - Added console.log for section intersection tracking

---

## 7. Highlight Functionality Debugging (Part 3)

### User Prompt
```
仍然無法 highlight 台北市。
```

### Action Taken
- **Modified**: `map04_leaflet_topojson.html`
- **Enhanced Debugging**:
  - Added comprehensive console.log in `highlightCity()` function
  - Logged available layers with `Object.keys(countyLayers)`
  - Logged first section city name
  - Added conditional checks for layer and city data existence

---

## 8. Critical Bug Fix - Character Encoding Issue

### User Prompt
```
Available layers: Array(22)
map04_leaflet_topojson.html:415 No layer found for: 台北市
map04_leaflet_topojson.html:354 First section city: 台北市
map04_leaflet_topojson.html:379 highlightCity called with: 台北市
map04_leaflet_topojson.html:380 Available layers: Array(22)
map04_leaflet_topojson.html:415 No layer found for: 台北市
```

### Action Taken
- **Modified**: `map04_leaflet_topojson.html`
- **Root Cause**: Character mismatch between HTML and TopoJSON data
  - HTML used: `台北市` (simplified character)
  - TopoJSON had: `臺北市` (traditional character)
- **Changes Made**:
  1. Updated `cityData` keys: `'台北市'` → `'臺北市'`
  2. Updated HTML attribute: `data-city="台北市"` → `data-city="臺北市"`
  3. Updated initialization call: `highlightCity('台北市')` → `highlightCity('臺北市')`
- **Result**: ✅ All three cities now highlight correctly

---

## 9. Banner, Footer & Scroll Snap Implementation

### User Prompt
```
在整個地圖視覺化的前方加一個 100vh、bg-primary 的 <div> 作為 banner，
後方加一個 100vh、bg-dark 的 <div> 作為 footer。

希望捲動三個縣市時可以有 slide 效果，
也就是向上/向下滾動時會自動滑動到下一個縣市（scroll snap 效果）。
```

### Action Taken
- **Modified**: `map04_leaflet_topojson.html`

#### HTML Structure Changes:
- **Added Banner Section**:
  ```html
  <div id="banner-section" class="banner-section bg-primary">
    - Large title: "台灣縣市探索"
    - Subtitle with description
    - Animated scroll hint with bounce effect
  ```

- **Added Footer Section**:
  ```html
  <div id="footer-section" class="footer-section bg-dark">
    - Closing message
    - Copyright information
  ```

#### CSS Changes:
- **Banner Styling**:
  - `min-height: 100vh`
  - Flexbox centering
  - `@keyframes bounce` animation for scroll hint
  - `scroll-snap-align: start`

- **Footer Styling**:
  - `min-height: 100vh`
  - Dark background with light text
  - `scroll-snap-align: start`

- **Scroll Snap Implementation**:
  - Added to `#content-container`: `scroll-snap-type: y mandatory`
  - Added to all sections: `scroll-snap-align: start`

#### JavaScript Changes:
- Added null check in Intersection Observer: `if (cityName) { ... }`
- Added scroll event listener for smooth snap behavior
- Implemented debouncing with `scrollTimeout`

---

## Final File Structure

```
web114/
├── map04_leaflet_topojson.html    # Main interactive map file
├── county_moi.json                # TopoJSON county boundary data
├── README.md                      # Updated with map documentation
└── Interactive_log.md             # This file
```

---

## Technologies Used

| Technology | Version | Purpose |
|------------|---------|---------|
| Leaflet | 1.9.4 | Interactive map engine |
| TopoJSON | 3.0.2 | Compressed topology data |
| D3.js | 7.8.5 | TopoJSON data processing |
| Bootstrap | 5.3.2 | Layout & styling |
| CartoDB Basemap | - | Light background tiles |
| Intersection Observer API | Native | Scroll detection |
| CSS Scroll Snap | Native | Page-by-page scrolling |

---

## Key Features Implemented

1. ✅ Taiwan county boundary visualization with colored polygons
2. ✅ Scroll-triggered county highlighting
3. ✅ Hover effects on counties (opacity & border changes)
4. ✅ Click-to-navigate functionality
5. ✅ Floating info card with city statistics
6. ✅ Dynamic map flyTo animation
7. ✅ 100vh banner section with animated scroll hint
8. ✅ 100vh footer section
9. ✅ CSS Scroll Snap for smooth page transitions
10. ✅ Responsive design for mobile devices

---

## Issues Resolved

### Issue #1: Map Not Rendering
- **Cause**: Incorrect TopoJSON object name
- **Solution**: Dynamic object name detection

### Issue #2: First Section Not Highlighting
- **Cause**: Intersection Observer threshold too high
- **Solution**: Reduced threshold and added rootMargin

### Issue #3: Taiwan City Not Highlighting
- **Cause**: Character encoding mismatch (台 vs 臺)
- **Solution**: Unified all references to use traditional character (臺)

---

## Performance Considerations

- Used CSS Scroll Snap (hardware-accelerated) instead of JavaScript scroll hijacking
- Intersection Observer (efficient) instead of scroll event listeners for section detection
- Debounced scroll events to prevent excessive function calls
- Leaflet's efficient tile loading and caching system

---

*Session completed: 2025-11-19*
