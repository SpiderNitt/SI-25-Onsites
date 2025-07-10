# PhotoGrid Web App (CSS Polygon-Based Image Designer)

## Objective

Build a creative web application that allows users to upload images and arrange them into custom-designed photo grids using CSS shapes (e.g., polygons, circles, custom clip paths). Inspired by apps like PhotoGrid, the tool should support design selection, placement, and basic image editing features.

## Key Features to Implement

### 1. Image Upload & Placement

**Functionality:**  
Allow users to upload multiple images and place them inside predefined or custom-designed grid templates.

**Requirements:**
- Upload up to N images via drag-and-drop or file selector.
- Choose from pre-built polygonal layout templates (hexagonal, triangular, etc.).
- Responsive rendering using CSS `clip-path` or SVG masks.

### 2. Design Templates

**Functionality:**  
Offer users multiple creative layout styles.

**Requirements:**
- Predefined designs using CSS Polygons or Grids.
- Live preview of selected layout.
- Drag-and-drop to rearrange photos inside the grid.

### 3. Image Editing Utilities

**Functionality:**  
Provide tools to fine-tune image appearance and layout.

**Requirements:**
- Rotate, scale, and move images within cells.
- Apply filters (grayscale, sepia, brightness, etc.).
- Reset individual images to original state.

### 4. Export Options (BONUS)

**Functionality:**  
Allow users to download or share the final output.

**Requirements:**
- Export the final layout as PNG or PDF.
- Optional: Integrate third-party libraries like `html2canvas`, `jsPDF`.
