# Antigravity Particle Physics

A high-performance, interactive particle engine inspired by organic fluid dynamics. 

## Overview

This project is a standalone WebGL implementation using Three.js and custom GLSL shaders to render an interactive, instanced particle system. It is designed to be lightweight, running entirely on the client side with zero build step dependencies.

### Features

*   **Instanced Rendering**: Renders thousands of particles smoothly using `THREE.InstancedMesh`.
*   **Custom GLSL Shaders**: Uses tailored vertex and fragment shaders to handle organic sinusoidal drift and gradient color shifting based on proximity.
*   **Interactive Simulation**: The particle field reacts to mouse position with drag dynamics and a physical repulsion radius, mimicking fluid displacement.
*   **Zero Dependencies**: Written in pure HTML, CSS, and modern JavaScript using ES Modules. No bundlers or frameworks are required.

## Demonstration

<video width="100%" autoplay loop muted playsinline>
  <source src="Particles.mp4" type="video/mp4">
  <p>Your browser does not support the video tag. You can download the video <a href="Particles.mp4">here</a>.</p>
</video>

## Usage

Since the project uses ES Modules to import Three.js, it must be served over HTTP/HTTPS rather than opened directly via the file protocol (`file://`).

1. Navigate to the project directory.
2. Start a local development server. For example, using Python:
   ```bash
   python -m http.server 8080
   ```
   Or using Node.js:
   ```bash
   npx serve .
   ```
3. Open a web browser and navigate to `http://localhost:8080`.

## Architecture

*   `index.html`: Contains the core logic, shader definitions, and instanced mesh generation.
*   `style.css`: Minimal styling to ensure the canvas fills the viewport seamlessly.
*   **Three.js**: Imported via a remote CDN using import maps for immediate execution in the browser.
