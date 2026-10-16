# Image Segmentation and Boundary Detection

Conceptual treatment of region segmentation, edge detection, boundary formation and geometric contours.

**Status: documentation / starter notebooks only.** The original notebooks for this subject contain headings but no executable cells; the processing pipeline below explains the topic rather than demonstrating finished code.

## What this covers

- Global/local thresholding
- Edge-strength maps and threshold selection
- Edge connectivity and boundary tracing
- Region masks and closed contours

## Processing pipeline

~~~mermaid
flowchart LR
    A[Input image] --> B[Threshold / region segmentation]
    A --> C[Gradient edge detection]
    B --> D[Candidate region masks]
    C --> E[Edge linking]
    D --> F[Boundaries and regions]
    E --> F
~~~

## Technical explanation

Image gradients approximate **∇I = (∂I/∂x, ∂I/∂y)**; the magnitude **||∇I||** measures local intensity change and is useful for edge detection.

## Contents

- `notebooks/image-segmentation.ipynb` — from `week09_segmentation/lab09_segmentation.ipynb`
- `notebooks/edge-and-boundary-detection.ipynb` — from `week10_edge_linking_boundary/lab10_edge_linking_boundary.ipynb`

## Getting started

Use Python 3.10+ in a virtual environment:

~~~bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
~~~

On Windows, activate with `.venv\Scripts\activate` instead. Install `jupyterlab` if it is not installed already. Open a notebook under `notebooks/`. Dataset/model paths in the original examples may need updating.

## Important limitations

This subject has not yet been implemented in the source notebook. The diagram is a conceptual study guide, not a verified program.

Input assets, lecture handouts, PDFs, trained models, cached results and third-party datasets have intentionally not been republished. Notebook code and explanatory cells are retained, while saved cell outputs are removed. No performance claims or additional experiments have been invented.

## Provenance

Adapted from the publicly available [ComputerVision source collection](https://github.com/dbxdrgsl/ComputerVision). Source-to-destination file mappings appear above. Each repository is organized by technical subject rather than course numbering.
