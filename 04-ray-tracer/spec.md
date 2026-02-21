# Real-Time Ray Tracer

## What do you want to build?

Build a real-time ray tracer in C++ that renders 3D scenes with realistic lighting at interactive frame rates. The renderer should support complex materials, acceleration structures, and output to a window or image file.

The implementation must include:
- Ray-scene intersection with BVH (bounding volume hierarchy) acceleration
- Materials: diffuse (Lambertian), metallic, dielectric (glass), emissive
- Lighting: area lights, environment maps (HDR)
- Camera: perspective projection with depth of field and motion blur
- Geometry: spheres, triangles, triangle meshes (OBJ file loading)
- Anti-aliasing via multi-sample per pixel
- Multi-threaded rendering with work-stealing task scheduler
- PNG/PPM image output
- Interactive preview window (SDL2 or similar) with progressive refinement
- Scene description file format (JSON or custom)

## How do you consider the project is success?

1. Cornell Box scene renders correctly with proper global illumination (soft shadows, color bleeding)
2. BVH provides >100x speedup over brute-force on a scene with 10K+ triangles
3. Glass and metallic materials produce physically plausible reflections and refractions
4. Multi-threaded rendering achieves >4x speedup on an 8-core machine vs single-threaded
5. A 1000-triangle mesh scene renders at >10 FPS at 800x600 in the interactive preview (progressive)
6. Reference image output matches expected results for at least 5 test scenes
7. OBJ mesh loading handles standard models (Stanford Bunny, Utah Teapot)
8. Test suite with at least 20 tests covering intersections, materials, BVH correctness, and image output
