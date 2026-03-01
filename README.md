AgriPredict-AI  — AI-Powered Agricultural Commodity Identification & Price Insight Platform

AgriPredict-AI is an AI-driven agricultural intelligence platform designed to help farmers, traders, consumers, and market participants identify vegetables, fruits, pulses, spices, and nuts through image recognition and access real-time Indian market prices.
The system also provides weekly price trends, commodity metadata, and a responsive dark-cosmic UI for a smooth user experience.
<br>
Features
1. AI-Based Commodity Identification

Upload an image of a vegetable, fruit, pulse, nut, or spice.

Gemini 2.5 Flash model identifies the commodity with high accuracy.

Confidence-based fallback system to avoid misclassification.

2. Real-Time Market Price Retrieval

Fetches live Indian market prices (INR) through external APIs.

Displays minimum, maximum, and modal prices.

Auto-updates based on the user's selected commodity.

3. 7-Day Price Trend Visualization

Interactive line charts built using Chart.js.

Shows price fluctuations for informed market decisions.

4. Commodity Details Panel

Nutritional information

Seasonal availability

Major growing regions

Usage details

5. Price Comparison Dashboard

Displays 15–20 commonly traded commodities.

Helps users compare market prices at a glance.

6. Dark Cosmic Responsive UI

Built using React, TailwindCSS, and DaisyUI.

Smooth animations, gradients, and responsive layout.

7. Robust Backend & Database

Node.js + Express for core APIs

MongoDB Atlas for user sessions, price data, and logs

TanStack Query for caching & optimized network calls

Vite for blazing-fast development

Tech Stack
Frontend

React

TypeScript

Vite

Tailwind CSS

DaisyUI

TanStack Query

Chart.js

Backend

Node.js

Express.js

MongoDB Atlas

Axios

Gemini API (Gemini 2.5 Flash model)

AI

Gemini Vision API for commodity identification

Confidence & fallback prediction pipeline
