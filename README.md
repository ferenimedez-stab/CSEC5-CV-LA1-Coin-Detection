# Laboratory Activity 1: Coin Detection

This repository is in fulfilment of the course requirements for **CSEC 5 -
Computer Vision**.

It contains my implementation and results for **Laboratory Activity 1 (LA1)**,
which focuses on processing images of Philippine coins using convolution,
spatial filtering, and edge-detection techniques.

## Objective

The objective of this activity is to process a combined image of selected
Philippine coins and produce a clean edge-detected result in which the coins
can be clearly identified. The selected coins have a combined value of
**₱21.10**.

## Selected Coins

The coin combination used in the activity is:

- One ₱20.00 coin
- Two ₱0.50 coins
- One ₱0.10 coin

```text
₱20.00 + ₱0.50 + ₱0.50 + ₱0.10 = ₱21.10
```

## Methodology

The notebook applies the following image-processing pipeline:

1. Select, load, and combine the coin images.
2. Convert the image to grayscale.
3. Reduce noise using a median filter and Gaussian smoothing.
4. Apply a sharpening convolution kernel to enhance coin boundaries.
5. Compare Canny, Laplacian, and Sobel edge-detection methods.
6. Select Canny edge detection as the most effective method for this image.
7. Clean the binary edge image by removing small connected components and
   other artifacts.
8. Display the processed image and final result.

The sharpening operation uses the following 3 × 3 kernel:

```text
[[ 0, -1,  0],
 [-1,  5, -1],
 [ 0, -1,  0]]
```

## Results

Canny edge detection produced the cleanest and most well-defined coin
boundaries among the tested methods. The Laplacian and Sobel results contained
more background noise and less distinct coin edges.

The generated outputs are available in the `results/` directory:

- `Original Combined Coin Images.png` - the combined input image
- `Final Output.png` - the cleaned edge-detected result

## Technologies

- Python
- Jupyter Notebook
- NumPy
- OpenCV
- Matplotlib
- Pillow

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── data/
│   └── README.md
├── notebooks/
│   └── ENIMEDEZ - Coin_Detection_Lab1.ipynb
└── results/
    ├── Final Output.png
    └── Original Combined Coin Images.png
```

## How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/ferenimedez-stab CSEC5-CV-LA1-Coin-Detection.git
   cd CSEC5-CV-LA1-Coin-Detection
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook:

   ```bash
   jupyter notebook "notebooks/ENIMEDEZ - Coin_Detection_Lab1.ipynb"
   ```

4. Run the notebook cells from top to bottom.

The original coin images are not included in this public repository. They were
provided by the instructors, and their original sources and redistribution
permissions are unknown. The notebook can be run only in the original
instructor-provided environment, or after the required images have been
obtained through an authorized course source and placed in the expected local
data directory.

## Data and Attribution

The coin images were provided by the instructors for this educational
activity. They are intentionally excluded from this repository because their
original sources and licenses could not be verified. See
[`data/README.md`](data/README.md) for details.