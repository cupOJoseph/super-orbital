#orbital

HTML based visualization of the geometry of Orbital, a new n-dimensional AMM design from the team over at Paradigm

Orbital AMM Paper

Authors: Dave White, Dan Robinson, Ciamac Moallemi (Paradigm)
Topic: Concentrated liquidity for n-dimensional stablecoin pools
Innovation: Capital efficiency through geometric constraints
Key Concepts
Hypersphere geometry: n-dimensional trading surfaces
Virtual reserves: Free liquidity from mathematical constraints
Tick consolidation: Efficient multi-tick trading
Polar decomposition: Separating balance vs. imbalance components
Built with Three.js • No installation required • Open source visualization

https://www.paradigm.xyz/2025/06/orbital


Orbital AMM 3D Visualization
An interactive 3D visualization of the Orbital AMM mathematical model for multi-asset stablecoin trading with concentrated liquidity.

Quick Start

Open https://1elbaz.github.io/orbital/ directly OR
Download the HTML file
Open in any modern web browser (Chrome, Firefox, Safari, Edge)
Interact with the 3D model using mouse and controls
No installation required! Just open the HTML file directly in your browser.

What You'll See

Core Elements
🟢 Green Wireframe Sphere: The AMM constant surface ||r⃗ - x⃗||² = r²
🔴 Colored Planes: Tick boundaries x⃗ · v⃗ = k for concentrated liquidity zones
🟡 Yellow Dot: Equal price point where all assets trade at $1.00
⚪ White Dot: Mathematical sphere center at (r, r, r)

Mathematical Relationships
AMM Constant: ||r⃗ - x⃗||² = r² (defines all valid reserve states)
Tick Boundaries: x⃗ · v⃗ = k (creates capital efficiency zones)
Equal Price Point: q = r(1 - 1/√n) (optimal balanced state)

Controls

Interactive Sliders
Sphere Radius (r): Adjust the AMM pool size (50-150)
Tick Count: Change number of concentration zones (3-12)
Animation Speed: Control rotation speed (0-2x)
Mouse Controls
Click + Drag: Rotate the 3D view
Scroll Wheel: Zoom in/out
Reset View: Button to return to default position
Action Buttons
Toggle Animation: Start/stop automatic rotation
Reset View: Return to default camera position

Key Insights

Capital Efficiency Zones:
Inner boundaries (red): High efficiency, low risk (covers small depegs)
Outer boundaries (blue): Low efficiency, high risk (covers extreme depegs)
Distance from center: Determines risk/reward profile
Geometric Constraints
All trading happens on the sphere surface
Tick boundaries slice the sphere into manageable liquidity zones
Equal price point represents perfect $1.00 parity for all assets

Real-World Applications

Multi-stablecoin pools: USDC, USDT, DAI, FRAX, LUSD
Concentrated liquidity: LPs can choose their risk tolerance
Capital efficiency: Up to 150x improvement over traditional AMMs

Technical Details

Requirements
Modern web browser with WebGL support
Internet connection (for Three.js library download)
No additional software needed
Dependencies
Three.js r128: 3D graphics library (loaded from CDN)
Pure HTML/CSS/JavaScript: No build process required
Browser Compatibility: Chrome 80+, Firefox 70+, Safari 12+, Edge 80+

Understanding the Math

AMM Constant (Sphere Equation)
||r⃗ - x⃗||² = r²
(r - x₁)² + (r - x₂)² + (r - x₃)² = r²
Replaces x × y = k for n-dimensional trading
Ensures consistent pricing across all asset pairs
Creates bounded reserve space (0 ≤ xᵢ ≤ r)

Tick Boundaries (Plane Equations)
x⃗ · v⃗ = k
(x₁ + x₂ + x₃)/√3 = k
Creates concentration zones for capital efficiency
k_min = r(√n - 1): Closest to equal price point
k_max = r(n-1)/√n: Covers extreme scenarios

Capital Efficiency Formula
efficiency = x_base / (x_base - x_min(k))
x_base: Traditional capital requirement
x_min(k): Virtual reserves from geometric constraints
Result: 15x to 150x efficiency gains