# Computer Vision Assignment

## Image Segmentation and Edge Detection

This project is a complete Computer Vision assignment notebook. It uses 20 local images to compare image segmentation and edge detection methods.

The project is fully local. The notebook does not download images or depend on external image links. All images are included in the `images/` folder.

## Project Contents

```text
.
├── edge detection.ipynb
├── images/
├── README.md
├── requirements.txt
└── .gitignore
```

## Assignment Tasks Covered

- Load 20 local images.
- Segment images using K-Means clustering.
- Segment images using Agglomerative clustering.
- Detect edges using Sobel filters.
- Detect edges using Prewitt filters.
- Detect edges using a manual Canny-style pipeline.
- Compare the methods using visual outputs and quantitative metrics.

## Dataset

The dataset contains 20 images stored locally in `images/`.

The images are grouped into:

- 10 images with clear objects or shapes.
- 10 images with distinct edges or boundaries.

The notebook validates that all 20 files exist before processing starts.

## Methods

### K-Means Segmentation

K-Means clusters image pixels in RGB color space. The notebook runs K-Means with:

```text
k = 2, 3, 4, 5
```

This produces 80 K-Means outputs in total: 20 images multiplied by 4 values of `k`.

### Agglomerative Segmentation

Agglomerative clustering groups pixels using color and spatial features. The notebook selects a distance threshold that gives a useful number of clusters and overlays region boundaries on the segmented images.

### Edge Detection

The notebook applies three edge detection methods to every image:

- Sobel edge detection
- Prewitt edge detection
- Canny edge detection

The Canny implementation includes Gaussian smoothing, gradient computation, non-maximum suppression, double thresholding, and hysteresis.

## Metrics

The notebook reports segmentation metrics:

- Silhouette score
- Davies-Bouldin score
- Cluster count

It also reports edge detection metrics:

- Edge density
- Mean edge strength

## How to Run

1. Open `edge detection.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.
2. Select the Python kernel.
3. Run all cells from top to bottom.

The notebook should run using only the files already included in this project.

## Expected Results

After a successful run:

- Local images loaded: 20
- K-Means outputs: 80
- Agglomerative outputs: 20
- Edge detection outputs: 60
- Segmentation table rows: 100
- Edge detection table rows: 60

## Notes

- The project is self-contained.
- No image download code is included.
- No external image URLs are required.
- The notebook output is already saved for review.
