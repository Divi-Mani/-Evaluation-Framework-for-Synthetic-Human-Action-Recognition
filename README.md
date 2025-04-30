# Evaluation Framework for Synthetic Human Action Recognition

This project provides a framework to evaluate the **quality of synthetic human action videos** using two industry-standard metrics: **FID-VID** and **FVD**. It includes an easy-to-use interface for uploading real and synthetic videos, computing scores and visualizing the results.

---

## Features

- Upload real and synthetic videos directly via a UI
- Compute **FID-VID** and **FVD** metrics for quantitative evaluation
- Generate visualization plots to compare and interpret results
- Gradio-based user interface for interaction

---

## Project Structure

```
synthetic-action-eval/
│
├── README.md                  
├── Documentation.pdf          
├── main.py                    
├── requirements.txt           
├── Real_Videos.zip            
├── Synthetic_Videos.zip      
└── fid-metrics/              
```
---

## Prerequisites

- Python 3.7 or higher  
- Internet connection (for downloading models if needed)

---

## Setup Instructions

### 1. Clone the `fid-metrics` Repository

This project relies on [`fid-metrics`](https://github.com/npurson/fid-metrics) for computing **FID-VID** and **FVD** scores.

```bash
git clone https://github.com/npurson/fid-metrics.git
cd fid-metrics
export PYTHONPATH=$(pwd):$PYTHONPATH  # Windows: set PYTHONPATH=%cd%;%PYTHONPATH%
```

### 2. Install Dependencies

Go back to the root folder (`synthetic-action-eval/`) and install the requirements:

```bash
pip install -r requirements.txt
```

---

## How to Run

### 1. Prepare Videos

- Place your videos in the same directory or unzip the provided `Real_Videos.zip` and `Synthetic_Videos.zip` archives.

### 2. Launch the Application

```bash
python main.py
```

### 3. Use the Gradio Interface

- Select a metric (**FID-VID** or **FVD**)
- Upload a real video and a synthetic video
- View the computed results and scatter plot visualization

---

## Output

- **Metric Results**  
  - Numeric scores for **FID-VID** and **FVD** (lower is better)

- **Visualization**  
  - A scatter plot showing comparative metric values for the uploaded videos

---

## Demo

Watch the demo video to see the framework in action:  
[📺 YouTube Demo](https://youtu.be/z1J4cyMaayU?si=pidEtYN5ifa1QxN8)

---

## Notes

- The model may take a few seconds during the first run (model weights downloading or video processing).
- Metric accuracy depends on resolution, frame count, and preprocessing steps.
- Ensure the videos are in supported formats (e.g., `.mp4`, `.avi`).

---
