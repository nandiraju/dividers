# User Guide: SVG Section Dividers Generator

Welcome to the SVG Section Dividers generator! This tool helps you create beautiful, lightweight, and responsive section dividers for your website. Rather than using static image files, this generator builds self-contained, inline-compatible CSS using SVG patterns.

You can preview the live generator here: **[nandiraju.github.io/dividers](https://nandiraju.github.io/dividers/)**

---

## <img src="https://unpkg.com/ionicons@7.1.0/dist/svg/rocket.svg" width="20" height="20" align="middle" /> Quick Start Guide

Transforming a straight section split into an elegant shape split takes only four steps:

### 1. Open the Generator
Open **[index.html](file:///Users/srikanthnandiraju/ANTIGRAVITY_WORKSPACE/SectionDividers/index.html)** in any modern web browser. The app runs entirely client-side with no external dependencies or build steps required.

### 2. Configure Your Divider
Use the interactive control panel to select and tune your divider:
- **Choose a Shape:** Pick from the list of curated organic, geometric, and wave patterns.
- **Select an Edge:** Anchor the shape to the **Top**, **Bottom**, **Left**, or **Right** of your section.
- **Adjust Dimensions:** Slide the controllers to change the height, width, and alignment.
- **Pick a Color:** Set the color of the divider to match the background of the adjacent section.

### 3. Copy the Generated CSS
Once you are happy with the visual preview, click the **Copy Code** button in the code inspector panel.

### 4. Apply to Your HTML
Paste the copied CSS into your stylesheet and add the class name to your section element. For example:

```html
<!-- Add the class name to the section you want to divide -->
<div class="svg_divider">
  <h2>Your Section Content</h2>
</div>
```

---

## <img src="https://unpkg.com/ionicons@7.1.0/dist/svg/color-palette.svg" width="20" height="20" align="middle" /> Tuning Your Dividers

To create the perfect look, you can adjust the following parameters:

### Edge & Orientation
The generator handles top, bottom, left, and right alignments by using dedicated, native SVG viewboxes. This ensures pixel-perfect vector alignment on all devices rather than relying on browser-based CSS rotations which can occasionally cause subpixel gaps.

### Scaling & Positioning
- **Long Axis (100% – 400%):** Stretches or compresses the pattern horizontally (or vertically for side dividers).
- **Short Axis (0px – 400px):** Controls how far the divider peaks or curves push into your content section.
- **Position (0% – 100%):** Shifts the alignment offset of the divider shape.

### Animation Effects
Enable **Animate** to apply smooth, non-blocking CSS translations. The shape will gently sway along its anchored edge, giving your page an active, dynamic feel.
> **Note:** Animation overrides custom axis flipping, as both utilize the CSS `transform` property.

### Responsive Behavior
Turn on the **Responsive** toggle to generate screen-size optimized media queries. This emits a base layout for mobile devices, discrete tablet (`768px`) and desktop (`1025px`) overrides, and a widescreen (`2100px`) rule that expands the shape proportionally.

---

## <img src="https://unpkg.com/ionicons@7.1.0/dist/svg/warning.svg" width="20" height="20" align="middle" /> Important Implementation Tip

The generated base CSS applies `position: relative` to your section class (e.g., `.svg_divider`) because the divider is rendered as an absolutely positioned `::before` pseudo-element. 

If your target element is already using `position: absolute` or `position: fixed` in your layouts, we recommend **wrapping the element** in a container and applying the divider class to that container instead to avoid styling conflicts.

---

## <img src="https://unpkg.com/ionicons@7.1.0/dist/svg/folder.svg" width="20" height="20" align="middle" /> Workspace Directory Map

Here is what you will find in this project directory:

| File / Folder | Description |
| :--- | :--- |
| **[index.html](file:///Users/srikanthnandiraju/ANTIGRAVITY_WORKSPACE/SectionDividers/index.html)** | The primary interactive editor and CSS generator. |
| **[divicraft.html](file:///Users/srikanthnandiraju/ANTIGRAVITY_WORKSPACE/SectionDividers/divicraft.html)** | An alternative playground interface utilizing modular JS assets. |
| **[divider_demo.html](file:///Users/srikanthnandiraju/ANTIGRAVITY_WORKSPACE/SectionDividers/divider_demo.html)** | A static guide showcasing all individual section dividers on a single scroll page. |
| **[shapes.js](file:///Users/srikanthnandiraju/ANTIGRAVITY_WORKSPACE/SectionDividers/shapes.js)** | The JavaScript data file containing the paths and viewBox definitions. |
| **[style.css](file:///Users/srikanthnandiraju/ANTIGRAVITY_WORKSPACE/SectionDividers/style.css)** | The stylesheet powering the visual layout, controls, and showcase page. |
