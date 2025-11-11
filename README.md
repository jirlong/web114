# Web114 Project Log

## HTML Files Index

### Root Directory

- [bootstrap_template.html](./bootstrap_template.html) - Bootstrap template
- [bt_template.html](./bt_template.html) - Bootstrap + jQuery starting template (Updated: 2025-11-05)
- [parallax-h1-section.html](./parallax-h1-section.html) - Parallax H1 section with jQuery scroll effects
- [parallax-h1-section-pure-css.html](./parallax-h1-section-pure-css.html) - Pure CSS parallax using perspective method (Created: 2025-11-11)
- [parallax-pure-css.html](./parallax-pure-css.html) - Pure CSS parallax demo

### Basic HTML (basic-html/)

- [index.html](./basic-html/index.html) - Basic HTML structure demo
- [style.css](./basic-html/style.css) - Styles for basic HTML demo


### Bootstrap (bt/)

- [bt.html](./bt/bt.html) - Bootstrap demo
- [bt2.html](./bt/bt2.html) - Bootstrap demo 2
- [bg-fixed.html](./bt/bg-fixed.html) - Background fixed demo

### jQuery (jquery/)

- [jquery_basic.html](./jquery/jquery_basic.html) - jQuery basics
- [jquery1008.html](./jquery/jquery1008.html) - jQuery demo (Oct 8)
- [practice-sticky-top.html](./jquery/practice-sticky-top.html) - Sticky top practice

### Prompting Examples (prompting/)

- [jquery01_detect_top.html](./prompting/jquery01_detect_top.html) - Detect top position
- [jquery02_detect_top_smooth_transition.html](./prompting/jquery02_detect_top_smooth_transition.html) - Detect top with smooth transition
- [jquery03_detect_top_html_first.html](./prompting/jquery03_detect_top_html_first.html) - Detect top (HTML first approach)
- [keyframe_as.html](./prompting/keyframe_as.html) - Keyframe animation demo


### Horizontal Scrolling (horizontal/)
- [horizontal_nice.html](./horizontal/horizontal_nice.html) - Horizontal nice layout
- [horizontal_section.html](./horizontal/horizontal_section.html) - Horizontal section layout


### Video Projects (video-scroll/)

#### Scrolled Video Series
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


---

## Project Features

### Latest: Parallax H1 Section Effects (Updated: 2025-11-11)

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

*Last updated: 2025-11-11*
