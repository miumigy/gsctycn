# AGENTS.MD - Global Supply Chain Tycoon Development Policy

This document outlines the core development principles for the Global Supply Chain Tycoon (GSCT) project, with a strong emphasis on **portability** and facilitating **future enhancements**.

## 1. Portability First: Single-File, Web-Native Distribution

The primary development goal is to maintain the project's high portability. This is achieved by:

*   **Self-contained `index.html`:** The entire application (HTML, CSS, JavaScript) resides within a single `index.html` file. This simplifies distribution, hosting, and guarantees a minimal deployment footprint.
*   **Vanilla JavaScript & Web Standards:** Strict adherence to vanilla JavaScript, HTML5, and CSS ensures maximum browser compatibility and avoids reliance on external frameworks, complex build tools, or server-side dependencies.
*   **Zero Build Step:** The project does not require a build pipeline, further simplifying development, debugging, and deployment.

## 2. Structured for Enhancement: Conceptual Modularity within a Single File

While physically a single file, the codebase is structured to allow for clear separation of concerns, enabling focused enhancements:

*   **Logical Separation of Components:**
    *   **UI/Layout:** HTML structure and CSS styling (`<style>` block) are distinct.
    *   **Map Rendering & Data Visualization:** Handled by D3.js and TopoJSON within dedicated functions.
    *   **Game Core Logic:** Encapsulated in functions like `initGameLogic`, `updateEconomy`, `updateUnits`, `dispatchUnit`.
    *   **User Interface Interactions:** Managed by specific functions for panel interactions, speed controls, and data display.
*   **Modular Function Design:** JavaScript code is organized into small, single-purpose functions to promote reusability, testability, and isolated changes.
*   **Global State Management:** The `state` object centralizes all dynamic game data, ensuring a single source of truth and predictable data flow. Modifications to game state should primarily occur through dedicated update functions.
*   **Data-Driven Configuration:** All game parameters, node data, and visual configurations are externalized into `CONFIG` and `NODES_DATA` objects. Enhancements should leverage and extend these data structures for balance adjustments, new content, or feature toggling, minimizing direct code changes.

## 3. Performance & User Experience (UX): Optimizing for Real-time Simulation

Future enhancements must consider the real-time simulation aspect and maintain a smooth user experience:

*   **Efficiency:** Prioritize efficient algorithms and rendering techniques. Avoid operations that introduce jank or excessive resource consumption, especially during the `gameLoop`.
*   **Responsive Design:** Continue to support and optimize for various screen sizes and orientations (desktop, tablet, mobile), ensuring a consistent and accessible experience across devices.
*   **Minimal UI Overhead:** User interface updates are throttled to maintain game performance, a practice that should continue.
*   **Canvas API for Dynamic Elements:** Dynamic game elements (units, nodes, particles) are rendered on a `<canvas>` element for performance, while static map elements are handled by SVG (D3.js). This hybrid approach should be maintained.

## 4. Code Standards & Maintainability

*   **Clear Naming Conventions:** Use descriptive variable and function names.
*   **Consistent Formatting:** Adhere to existing code formatting and style.
*   **Sparse, High-Value Comments:** Comments should explain *why* complex logic exists, not *what* straightforward code does.
*   **Error Handling:** Implement robust error handling, particularly for rendering and data processing, to prevent crashes and provide informative feedback.

By adhering to these principles, the Global Supply Chain Tycoon project can continue to evolve with new features and content while maintaining its core strengths of portability and maintainability.
