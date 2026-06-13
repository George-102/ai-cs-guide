# Physically Based Rendering (PBRT)

## Introduction

*Physically Based Rendering: From Theory to Implementation* (PBRT) is **the authoritative text on offline rendering and path tracing**, written by Matt Pharr, Wenzel Jakob, and Greg Humphreys. The book starts from physical principles and systematically explains how to build a physically-based renderer.

PBRT's core philosophy is: **rendering should simulate the physical behavior of real light**. The book derives the rendering equation, BRDF, Monte Carlo integration, importance sampling, and other core concepts in detail, and provides complete renderer implementation code.

This book is **freely available online** and fully open-source. It's the best resource for understanding modern rendering techniques (including PBR rendering in film VFX and game engines).

## Prerequisites

- **C++ programming skills**: PBRT is implemented in C++; familiarity with modern C++ features is needed
- **Calculus and probability theory**: Monte Carlo integration, probability density functions, and other mathematical tools are core content
- **Linear algebra**: Matrix transformations, coordinate system conversions
- **Basic graphics concepts**: Recommended to first study ray tracing fundamentals before reading PBRT

## Difficulty

🌟🌟🌟🌟🌟 (Advanced)

PBRT is one of the most in-depth textbooks in graphics, with dense mathematical derivations. Best suited for advanced study after building a solid foundation.

## Estimated Study Hours

Approximately 100-150 hours (16 chapters, ~6-10 hours each)

- Reading and understanding: ~60-80 hours
- Code reading and experimentation: ~40-70 hours

## Resources

- Online (free): [pbrt.org](https://www.pbrt.org/)
- Source code: [GitHub](https://github.com/mmp/pbrt-v4)
- Book (3rd edition): Published by Elsevier

## Self-Study Tips

1. **Complete Ray Tracing in One Weekend first.** PBRT is advanced material. Build ray tracing intuition through Ray Tracing in One Weekend before diving into PBRT's mathematical derivations.

2. **Focus on understanding Monte Carlo integration.** This is the core mathematical tool of path tracing. Understand why Monte Carlo methods can solve the rendering equation, and why importance sampling accelerates convergence.

3. **Follow along with the code.** PBRT's code structure is very clear. Read the book while cross-referencing the code, understanding how each class and method maps to theoretical concepts.

4. **Don't try to read it all at once.** PBRT is extremely rich in content. Read in stages: Chapters 1-5 (foundations) first, then Chapters 6-10 (light transport), and finally Chapters 11-16 (advanced topics).

5. **Modify the renderer.** Try modifying PBRT's code to add new material models or light source types. Use code modifications to verify your understanding of the theory.
