# Image Processing Pipeline

## What do you want to build?

Build an image processing pipeline in Rust that provides a CLI and library for applying filters, resizing, watermarking, and batch processing images. The tool should support common formats (JPEG, PNG, WebP), implement several filters from scratch (blur, sharpen, grayscale, edge detection), and process images in parallel for performance. Include both a command-line interface and a programmatic API.

The implementation must include:
- Image loading and saving for JPEG, PNG, and WebP formats
- Filters implemented from scratch: Gaussian blur, box blur, sharpen, grayscale, edge detection (Sobel), brightness/contrast adjustment
- Resize with multiple algorithms: nearest neighbor, bilinear, bicubic
- Watermarking: overlay text or image with alpha blending and positioning
- Batch processing: apply operations to all images in a directory with parallel execution
- CLI with intuitive syntax: `imgproc --input foo.jpg --blur 5 --resize 800x600 --output bar.jpg`
- Pipeline chaining: apply multiple operations in sequence efficiently
- Progress reporting for batch operations

## How do you consider the project is success?

1. Correctly loads and saves JPEG, PNG, and WebP images without quality loss (lossless operations)
2. Filters produce visually correct results — blur smooths, sharpen enhances edges, edge detection highlights boundaries
3. Resize operations maintain aspect ratio when only one dimension specified and produce high-quality output
4. Watermarking correctly applies text and image overlays with configurable opacity and position
5. Batch processing handles 100+ images in parallel with proper thread pooling and error handling
6. CLI supports pipeline syntax: `--blur 5 --resize 800x600 --watermark logo.png --output-dir ./processed`
7. Test suite with at least 15 tests covering each filter, resize algorithms, watermarking, and batch processing
8. Benchmarks show processing 1000 images (1920x1080 → 800x600 with blur) in under 30 seconds on modern hardware
