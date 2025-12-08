# AgriPredict AI - Design Guidelines

## Design Approach
**Aesthetic Direction**: Dark Cosmic Theme with Modern Agricultural Elements
The interface will embody a sophisticated "cosmic agriculture" aesthetic - merging deep space-inspired backgrounds with clean, data-driven agricultural interfaces. Think: sleek dashboard meets night sky observatory, where commodity data feels both scientific and approachable.

**Core Design Principles**:
- Immersive depth through layered cosmic backgrounds
- High contrast for critical data visibility (prices, graphs)
- Smooth, purposeful animations that feel celestial
- Modern card-based layouts with glass morphism effects

## Typography System

**Font Stack**:
- Primary: 'Inter' - Clean, modern, excellent for data display
- Accent: 'Space Grotesk' - Geometric, futuristic for headlines and callouts

**Hierarchy**:
- Hero Headlines: 3xl to 5xl, font-bold, tracking-tight
- Section Headers: 2xl to 3xl, font-semibold
- Body Text: base to lg, font-normal, leading-relaxed
- Data/Prices: xl to 3xl, font-bold, tabular-nums
- Labels: sm to base, font-medium, uppercase tracking-wide

## Layout System

**Spacing Primitives**: Use Tailwind units of 2, 4, 6, 8, 12, 16, 20, 24
- Component padding: p-6 to p-8
- Section spacing: py-16 to py-24
- Card spacing: p-6 internal, gap-6 between
- Form elements: space-y-4 to space-y-6

**Grid Structure**:
- Landing page: Full-width sections with max-w-7xl containers
- Price cards: grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4
- Upload interface: Centered layout with max-w-4xl
- Results view: Two-column lg:grid-cols-3 (2 col content + 1 col sidebar)

## Component Library

### Navigation
- Fixed top navbar with glass morphism effect (backdrop-blur-md)
- Logo left, navigation center, CTA button right
- Mobile: Hamburger menu with slide-in drawer

### Landing Page Components

**Hero Section** (80vh):
- Full-width cosmic gradient background with subtle particle animation
- Centered content: Headline, subheadline, dual CTAs ("Upload Image" primary, "View Prices" secondary)
- Floating element: Live ticker showing 3-4 commodity prices scrolling horizontally
- Include hero image: Abstract/artistic representation of Indian agriculture meeting technology (farmers with digital overlay, or produce with data visualization elements)

**Live Market Prices Section**:
- Grid of 12-15 commodity cards (4 columns on desktop)
- Each card: Icon/image, commodity name, current price in large bold INR, small percentage change indicator with up/down arrow
- Subtle hover elevation effect
- Filter tabs above: "All", "Vegetables", "Fruits", "Pulses"

**Features Section**:
- Three-column grid highlighting: "AI Recognition", "Price Trends", "Commodity Insights"
- Each feature: Icon, title, 2-line description
- Glass morphism cards with border glow effect

**How It Works**:
- Horizontal timeline/stepper showing: Upload → Identify → Analyze → Results
- Each step with icon and brief text

### Upload Interface
- Large drag-and-drop zone (min-h-96) with dashed border
- Central icon (cloud upload) with "Drag image here or click to browse"
- Accepted formats note below
- After upload: Image preview with 80% width, "Analyze" button prominent below
- Loading state: Spinner with cosmic animation, "Identifying commodity..." text

### Results Display

**Layout**: Three-panel grid
1. **Left Panel (2 columns)**: 
   - Identified commodity with confidence score
   - Current market price (very large, bold INR display)
   - Price change indicators (day, week)
   
2. **Center Panel**:
   - Interactive line chart showing 7-day price history
   - Y-axis: Price in INR, X-axis: Dates
   - Gradient fill under line, glowing line stroke
   
3. **Right Sidebar**:
   - Commodity details card: Season, growing regions, nutritional highlights
   - "Ask for more details" expandable section

### Cards & Containers
- Consistent border-radius: rounded-xl for large cards, rounded-lg for smaller elements
- Glass morphism: backdrop-blur-md with semi-transparent backgrounds
- Subtle border glow using box-shadow with cosmic theme accents
- Elevation: Use shadow-xl for primary cards, shadow-lg for secondary

### Forms & Inputs
- Minimal, borderless inputs with bottom border on focus
- Labels: Small, uppercase, tracking-wide above inputs
- File upload: Large click target with visual feedback
- Buttons: 
  - Primary: Solid with glow effect on hover, px-8 py-3, rounded-lg
  - Secondary: Outline with backdrop blur, same padding
  - Disabled state: Reduced opacity, no hover effects

### Data Visualization
- Charts: Use Chart.js or Recharts
- Line charts for price trends with smooth curves
- Gradient fills from dark to accent
- Interactive tooltips on hover showing exact values
- Grid lines: Subtle, semi-transparent

### Icons
Use Heroicons exclusively via CDN
- Outline style for general UI
- Solid style for emphasis (upload success, price indicators)
- Size: h-5 w-5 for inline, h-8 w-8 for features, h-12 w-12 for empty states

## Images

**Hero Image**: 
- Position: Background overlay with 40% opacity, or side-by-side split (image right, content left)
- Content: Modern Indian agriculture scene - possibly farmer with smartphone in field, or overhead shot of fresh produce at market with digital price overlays
- Treatment: Subtle cosmic gradient overlay blending into background

**Commodity Icons/Images**:
- Small thumbnail images of actual produce in price cards (64x64px, rounded-full)
- High-quality, well-lit product photography
- Consistent styling: Same background treatment across all

**Upload Preview**:
- User-uploaded image displayed at actual size (max 600px width) with rounded corners
- Subtle shadow and border treatment

## Animations (Minimal)
- Page transitions: Fade + slight slide (200ms)
- Card hovers: Lift effect with shadow increase (150ms ease-out)
- Button interactions: Scale 0.98 on active
- Chart rendering: Stagger animation on load (400ms)
- Cosmic background: Subtle parallax scroll or slow particle drift
- Loading states: Spinner with rotation, no complex animations

## Accessibility
- Minimum contrast ratio 4.5:1 for all text on cosmic backgrounds
- Focus states: 2px outline with offset
- Alt text for all commodity images
- Keyboard navigation for upload and form interactions
- ARIA labels for chart data points
- Screen reader announcements for price updates