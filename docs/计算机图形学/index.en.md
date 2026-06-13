# Computer Graphics

## What Is Computer Graphics

Computer graphics studies **how to generate, process, and display visual content using computers**. From UI rendering on your phone screen, to virtual worlds in 3D games, to visual effects in movies, to AI image generation — all of these rely on computer graphics knowledge.

The core problem of graphics: how to convert a 3D scene (models, materials, lighting, camera) into a 2D image (pixels). This process is called **rendering**. Rendering falls into two categories: real-time rendering (games, interactive applications, requiring 30-120 frames per second) and offline rendering (film VFX, pursuing extreme realism, where a single frame can take hours to render).

## Why Study Computer Graphics

**Core of game development.** You're building games with Godot 4. Understanding graphics helps you use the rendering pipeline, shaders, and lighting systems more effectively to create better visuals.

**Foundation for AI image generation.** The underlying principles of generative AI models (Stable Diffusion, DALL-E, Sora) — diffusion models, NeRF, 3D Gaussian Splatting — are all built on graphics.

**Intersection of multimodal AI.** Computer vision (helping AI understand images) and computer graphics (helping AI generate images) are two sides of the same coin.

**Train mathematical application skills.** Graphics is the most intuitive application of linear algebra, geometry, and calculus. Studying graphics helps you truly understand the practical meaning of matrix transformations, vector spaces, and probability distributions.

**Frontier research directions.** Neural Radiance Fields (NeRF), 3D Gaussian Splatting, real-time path tracing — these are the hottest research areas at the intersection of graphics and AI.

## Core Knowledge Modules

### Mathematical Foundations

- **Linear algebra**: Matrix transformations (translation, rotation, scaling), homogeneous coordinates, quaternions
- **Vector operations**: Dot product (lighting calculations), cross product (normals), vector projection
- **Geometry**: Parametric equations, Bezier curves, B-splines

### The Rasterization Pipeline

- **Vertex processing**: Model transform → View transform → Projection transform → Viewport transform
- **Triangle rasterization**: Converting 3D triangles to 2D pixels
- **Depth buffer (Z-Buffer)**: Resolving occlusion relationships
- **Texture mapping**: Applying 2D images to 3D model surfaces
- **Anti-aliasing**: MSAA, FXAA

### Lighting and Shading

- **Phong lighting model**: Ambient + diffuse + specular
- **Blinn-Phong model**: An improvement on Phong
- **PBR (Physically Based Rendering)**: Microfacet model, BRDF, energy conservation
- **Shadows**: Shadow Mapping, Ray Traced Shadows
- **Global illumination**: Ray tracing, radiosity, photon mapping

### Ray Tracing

- **Ray generation**: Cast rays from the camera through each pixel
- **Ray-object intersection**: Spheres, triangles, AABB
- **Recursive ray tracing**: Reflection, refraction, soft shadows
- **Acceleration structures**: BVH (Bounding Volume Hierarchy), KD-Tree
- **Path tracing**: Monte Carlo methods for solving the rendering equation

### Shader Programming

- **Vertex shader**: Processes position and attributes of each vertex
- **Fragment shader**: Computes the final color of each pixel
- **Compute shader**: General-purpose GPU computation
- **GLSL / HLSL**: Shader programming languages

### Advanced Topics

- **Geometry processing**: Mesh simplification, subdivision surfaces, parameterization
- **Animation**: Skeletal animation, skinning, keyframe interpolation, physics simulation
- **Volume rendering**: Clouds, smoke, fire
- **Neural rendering**: NeRF, 3D Gaussian Splatting

## How to Learn

**Start with OpenGL/WebGL.** Write a simple triangle rendering program and understand each stage of the graphics pipeline. Recommended: [LearnOpenGL](https://learnopengl.com/) — excellent tutorial quality, available in Chinese.

**Practice with Godot.** You're already using Godot 4. Try writing custom shaders and understanding Godot's rendering pipeline. Combining graphics theory with game engine practice produces the best learning results.

**Do Ray Tracing in One Weekend.** This tutorial series implements a ray tracer in a few hundred lines of C++. You can finish it in three days, and the sense of accomplishment is incredible. It's the best hands-on project for getting started with graphics.

**Don't skip the math.** The math in graphics (linear algebra, geometry) is the foundation for understanding everything. Recommended supplement: 3Blue1Brown's *Essence of Linear Algebra* series.

## Recommended Resources

### Systematic Courses

- [Berkeley CS184](./Berkeley-CS184.md) — Berkeley's graphics course with complete project assignments covering modeling, animation, and rendering
- [Stanford CS148](https://cs148.stanford.edu/) — Stanford's introductory graphics course
- [MIT 6.837](https://ocw.mit.edu/courses/6-837-computer-graphics-fall-2012/) — MIT's computer graphics course

### Hands-on Tutorials (Highly Recommended)

- [LearnOpenGL](./LearnOpenGL.md) — The best OpenGL tutorial, available in Chinese, build a rendering pipeline from scratch
- [Ray Tracing in One Weekend](./Ray-Tracing-in-One-Weekend.md) — Build a ray tracer in three days, free online, best starting project
- [The Book of Shaders](https://thebookofshaders.com/) — Interactive shader programming tutorial
- [WebGL Fundamentals](https://webglfundamentals.org/) — WebGL tutorial that runs directly in the browser

### Textbooks

- [PBRT](./PBRT.md) — The authoritative text on offline rendering and path tracing, free online
- *Computer Graphics: Principles and Practice* (Foley, van Dam et al.) — Classic graphics textbook, comprehensive coverage
- *Real-Time Rendering* (Tomas Akenine-Möller et al.) — The bible of real-time rendering, required reading

### Frontier Directions

- [NeRF: Neural Radiance Fields](https://www.matthewtancik.com/nerf) — The original NeRF paper
- [3D Gaussian Splatting](https://repo-sam.inria.fr/fungraph/3d-gaussian-splatting/) — 3D Gaussian Splatting, a breakthrough in real-time neural rendering
- [Two Minute Papers (YouTube)](https://www.youtube.com/c/K%C3%A1rolyZsolnai) — Accessible explanations of cutting-edge graphics and AI research
