# AgriPredict AI

## Overview
AgriPredict AI is an AI-powered agricultural commodity price prediction application for the Indian market. Users can upload images of pulses, vegetables, or fruits to get instant identification and current market prices in Indian Rupees (INR).

## Current Features
- **Landing Page**: Interactive cosmic-themed landing with live market prices for 22+ commodities
- **Image Upload**: Drag-and-drop interface for commodity image upload
- **AI Recognition**: OpenAI Vision API integration for accurate commodity identification
- **Price Display**: Current market prices in INR with price change indicators
- **Price Charts**: 7-day price trend visualization using Recharts
- **Commodity Details**: Seasonal info, nutritional facts, and growing regions

## Tech Stack
- **Frontend**: React, TypeScript, Tailwind CSS, Shadcn UI
- **Backend**: Express.js, Node.js
- **AI**: OpenAI GPT-5 Vision API
- **Charts**: Recharts
- **Routing**: Wouter
- **State**: TanStack Query

## Project Structure
```
client/src/
  pages/
    landing.tsx     - Main landing page with market prices
    upload.tsx      - Image upload interface
    results.tsx     - Analysis results with charts
  components/ui/    - Shadcn UI components
  lib/              - Utilities and query client
server/
  routes.ts         - API endpoints
  storage.ts        - In-memory data storage
shared/
  schema.ts         - TypeScript types and schemas
```

## API Endpoints
- `GET /api/commodities` - List all commodity prices
- `GET /api/commodities/:name` - Get specific commodity details
- `POST /api/analyze-image` - Analyze uploaded image with AI

## Environment Variables
- `OPENAI_API_KEY` - Required for image recognition

## Design Theme
Dark cosmic theme with:
- Deep purple/blue backgrounds
- Green/teal primary color (hsl 160 70% 45%)
- Glass morphism effects
- Animated particle backgrounds
- Responsive design

## Commodities Included
**Vegetables**: Tomato, Onion, Potato, Cauliflower, Cabbage, Green Peas, Brinjal, Capsicum
**Fruits**: Apple, Banana, Mango, Orange, Papaya, Grapes, Watermelon
**Pulses**: Toor Dal, Chana Dal, Moong Dal, Masoor Dal, Urad Dal, Rajma, Kabuli Chana

## Recent Changes
- December 2024: Initial MVP with all core features
  - Dark cosmic UI theme implementation
  - OpenAI Vision integration for image recognition
  - 22 commodities with Indian market prices
  - Price trend charts and commodity details
