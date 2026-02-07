# Global Supply Chain Tycoon

## Overview
Global Supply Chain Tycoon (GSCT) is a real-time business simulation game focused on Global Supply Chain Management (SCM).
As the CEO of a logistics conglomerate, you must optimize the entire process from raw material procurement to factory production and final delivery to markets, aiming to maximize profits over a 365-day period.

This is not just a game about moving goods. You must carefully calculate transport costs, inventory turnover, and most importantly, **Product Freshness**, to solve complex logistical puzzles.

## Key Features

### 1. Freshness System
Every product has a "Freshness" value.
*   **Premium (Freshness 80%+):** Freshly made or delivered goods. Sells for up to **3x** the base price.
*   **Stale (Freshness 40%-):** Aged goods. Value plummets, often leading to a **Loss** when sold below cost.
*   Freshness decays constantly during transport and storage.

### 2. Logistics & Cost Trade-offs
Choose your transport mode carefully:
*   ✈️ **Air Freight:** Ultra-fast. Maintains high freshness (Premium price) but comes with high transport costs.
*   🚢 **Sea Freight:** High volume. Low cost per trip, but goods lose freshness during the long voyage.

Additionally, **Load Factor** critically impacts your Unit Cost.
Shipping "air" (dispatching half-empty vehicles) causes the cost per unit to skyrocket, destroying your profit margins.

### 3. Inventory Strategy
*   **Pull System:** Deliver only what is needed when it is needed. Minimizing inventory keeps freshness high (Just-In-Time strategy).
*   **Frequency Control:** Use the slider on each route to adjust dispatch intervals (0.5 days to 30 days). Decide between "Frequent small batches (High Freshness)" or "Bulk shipments (Low Cost)."

## How to Play

1.  **Activate Routes:**
    *   Click on a location/route on the map and toggle the transport switch (Ship/Air) to ON.
2.  **Adjust Frequency:**
    *   Use the slider to set the dispatch interval.
    *   Monitor the "Avg. Unit Cost" to ensure you are achieving an optimal Load Factor.
3.  **Manage Time:**
    *   Once ready, hit the Play button (▶) to start the simulation.
    *   Pause (⏸) at any time to rethink your strategy.

## KPIs (Key Performance Indicators)

At the end of 365 days, you are evaluated on:

*   **Final Net Cash:** Total accumulated profit.
*   **Avg Freshness:** The average quality of goods delivered to markets globally.
*   **Missed Sales:** Total volume of sales lost due to stockouts (Supply Chain Failure).
*   **Inv. Turnover:** Inventory Turnover Rate. Indicates how efficiently you converted stock into revenue.

## Technology Stack
*   HTML5 / Canvas API
*   D3.js (Map rendering & Data visualization)
*   TopoJSON (World map data)
*   Vanilla JavaScript (Game Logic)

## License
This project is licensed under the MIT License.
