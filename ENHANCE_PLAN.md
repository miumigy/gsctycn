# Global Supply Chain Tycoon (GSCT) Enhancement Roadmap

This document outlines the proposed features and functional expansions to improve the "SCM Learning Value" and "Gameplay Experience" of GSCT.

---

## 1. Complexity: Multi-Product & BOM (Bill of Materials)
Evolve from simple single-product logistics to the reality of manufacturing, where finished goods are assembled from multiple parts.

- **BOM System:**
  - Example: Product A = Raw Material X(2) + Component Y(1).
  - Add complexity by requiring players to coordinate the arrival of multiple components at a factory (Kitting/Synchronization).
- **Lead Time Stacking:**
  - Since different parts have different procurement lead times, simulate the critical SCM challenge where "a single missing screw stops the entire assembly line."
- **Learning Objectives:** Synchronization, Shortage Risk Management, Component Inventory Optimization.

## 2. Expansion: Supply Chain Network Investment
Enable players to expand their global footprint through strategic capital expenditure, moving beyond managing a pre-set map.

- **Node Development Investment:**
  - **Raw Material Sites:** Improve extraction efficiency and secure rare materials.
  - **Factories:** Add production lines, implement automation (reduce processing costs), and improve quality control.
  - **Markets:** Stimulate demand through advertising and develop local distribution networks.
- **New Hub Discovery:**
  - Spend cash to build new nodes (facilities) in new countries, requiring players to redesign their optimal logistics network.
- **Learning Objectives:** ROI (Return on Investment) analysis, Vertical Integration vs. Horizontal Specialization, Global Network Design.

## 3. Sustainability: CO2 Emissions & Green Investment
Incorporate "Green Transformation (GX)," a top-priority theme in modern SCM, into the core gameplay.

- **Carbon Footprint Visualization:**
  - Calculate CO2 emissions based on transport modes (Air = High, Sea = Low) and factory operations.
- **Carbon Tax & Environmental Regulations:**
  - Implement taxes based on emission levels or penalties for exceeding certain thresholds.
- **Green Investment:**
  - Upgrade to "Electric Cargo Ships" or "Renewable Energy Factories" to reduce long-term tax burdens and improve brand value.
- **Learning Objectives:** Trade-offs between environmental impact and cost, ESG management, Sustainable Supply Chain.

## 4. Risk Management: Supply Chain Disruptions
Test resilience against uncertainty (VUCA) through dynamic in-game events.

- **Random Events:**
  - "Canal blockages," "Port strikes," or "Extreme weather conditions" in specific regions.
- **Emergency Response Mode:**
  - Allow players to set up "Emergency Air Freights" or "Alternative Routes" during crises to minimize stockouts.
- **Learning Objectives:** Resilience, BCP (Business Continuity Planning), Strategic Safety Stock placement.

## 5. Strategic Missions: Emergency Orders & Contracts
Provide short-term business opportunities in addition to steady-state sales.

- **Spot Contracts:**
  - Time-limited missions such as "Deliver 100 units with 90%+ freshness to Germany within 10 days."
  - High rewards for success; heavy penalties for failure.
- **Learning Objectives:** Agility, Prioritization under pressure.

## 6. Advanced Analytics: Financial & Operational Visibility
Enhance BI (Business Intelligence) features to support data-driven decision-making.

- **Cost-to-Serve Analysis:**
  - Breakdown of "Manufacturing Cost," "Transport Cost," "Inventory Holding Cost," and "Wastage Loss" per unit.
- **Sensitivity Analysis Graphs:**
  - Simulate how total costs change when adjusting parameters like shipping frequency.
- **Learning Objectives:** Total Cost of Ownership (TCO), Data-Driven Management.

## 7. Game Flow: Customizable Duration & Intermediate Results
Enhance the game progression by allowing players to set the duration and review their performance periodically.

- **Game Duration Setting:**
  - Select the game duration (e.g., 1 year, 3 years, 5 years) on the start screen.
- **Year-by-Year Progression:**
  - The game pauses at the end of each year to display intermediate performance reports (financials, KPIs).
- **In-Game Year Display:**
  - Real-time display of the current progress (e.g., "Year 2 of 5") on the main game screen.
- **Learning Objectives:** Long-term strategic planning, performance review cycles, and target management.

## 8. Development Strategy: Single-File Maintainability
As the project grows within a single HTML file, we will adopt a "Virtual Module" strategy to ensure LLMs can maintain and evolve the code without introducing regressions.

- **Boundary Comments:** Use standardized delimiters (e.g., `// --- MODULE: [NAME] ---`) to separate Data, State, Engine, UI, and Rendering logic.
- **Functional Isolation:** Encapsulate features into self-contained functions or object literals (e.g., `UIManager`, `EventSystem`) to minimize global scope pollution and side effects.
- **State Centralization:** Maintain a single `state` object for all dynamic data, ensuring that any module can predict the application's status.
- **UI Templating:** Move complex UI generation into dedicated "Render Functions" that use template literals, separating HTML structure from business logic.

## 9. System Integration: Unified Event Framework
Merge "Market Spikes" and "Crisis Events" into a single, extensible event engine.

- **Event Schema:** Define a common structure for all disruptions and opportunities (id, type, target_node/route, multipliers, duration, visuals).
- **Dynamic Multipliers:** Use the event system to modify node properties (demand, production rate) and route properties (travel time, cost) dynamically.
- **Visual Feedback:** Implement a unified notification and particle system to signal both positive (gold/green) and negative (red/warning) events.

## 10. Maritime Logistics: Nautical Route Optimization
Improve routing logic to ensure ships follow realistic sea lanes, avoiding land traversal (Great Circle artifacts).

- **Sea Lane Graph:** Define a network of "Maritime Waypoints" (Straits, Capes, Canal Entrances) that ships must navigate between landlocked or coastal regions.
- **Coastline Alignment:** Implement "Port Entry" points for each node to ensure ships arrive at the coastline before "docking," preventing visual overlap with land.
- **Pathfinding:** Use a simplified A* or waypoint-chaining logic to select the best sequence of sea lanes based on the origin and destination.

---

## Proposed Implementation Phases

1.  **Phase 1: Foundation & Reliability (Code Health & Core Logic)**
    *   **Code Splitting:** Refactor existing code into the "Virtual Module" structure for better LLM maintainability.
    *   **Nautical Routing:** Implement the Maritime Waypoint system to prevent land-crossing and ensure realistic sea lanes.
    *   **Unified Event Framework:** Merge spikes and crisis logic into a single extensible engine.
    *   **Game Flow:** Basic duration settings and yearly progress tracking.

2.  **Phase 2: Visibility & Analytics (Business Intelligence)**
    *   **Financial Visibility:** Advanced Cost-to-Serve analysis (TCO awareness).
    *   **Sensitivity Analysis:** Visual graphs showing the impact of transport frequency and mode changes.

3.  **Phase 3: Strategic Growth (Network Expansion)**
    *   **Development Investment:** Enable ROI-driven upgrades for factories, mines, and markets.
    *   **Hub Discovery:** Spend capital to unlock and design new supply chain nodes.

4.  **Phase 4: Operational Complexity (Multi-Product & BOM)**
    *   **BOM System:** Introduce assembly logic where finished goods require multiple raw materials.
    *   **Lead Time Stacking:** Simulate synchronization challenges in complex manufacturing.

5.  **Phase 5: Sustainability & Brand (Green Transformation)**
    *   **GX Investment:** CO2 emissions tracking and green upgrades (Electric ships, etc.).
    *   **ESG Management:** Impact of environmental regulations on long-term profitability.
