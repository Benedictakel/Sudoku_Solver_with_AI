# 🔢 Sudoku Solver with AI

This repository contains an **AI-based Sudoku solver** that can solve puzzles from:

✅ A given **grid input (2D array)**

✅ An **image of a Sudoku puzzle** (optional, using OpenCV for digit recognition)



## 📑 Table of Contents

* [Introduction](#introduction)
* [Objectives](#objectives)
* [Features](#features)
* [Technologies Used](#technologies-used)
* [Installation](#installation)
* [Usage](#usage)
* [Algorithm Overview](#algorithm-overview)
* [Results](#results)
* [Project Structure](#project-structure)
* [Future Work](#future-work)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)



## 📝 Introduction

Sudoku is a logic-based puzzle game where a 9x9 grid must be filled so that each row, column, and 3x3 subgrid contains all digits from 1 to 9 without repetition.

This project uses:

* **Backtracking algorithm** to efficiently solve Sudoku puzzles given as 2D arrays
* *(Optional)* **Computer Vision (OpenCV)** to extract grids from images and solve them automatically



## 🎯 Objectives

✔️ Build an efficient Sudoku solver for grid inputs using AI search techniques

✔️ Extend to solving puzzles from images with digit recognition

✔️ Practice integrating **backtracking algorithms** with computer vision



## ✨ Features

* **Grid Solver:** Solves any valid 9x9 Sudoku puzzle grid input using backtracking
* **Image Solver (Optional):** Reads puzzle from an image using OpenCV, processes it, and solves it
* **Validation:** Checks input for validity before attempting a solution
* **Visualization:** Displays the solved Sudoku in the console or on the image (for image mode)



## 🛠️ Technologies Used

* **Python 3**
* **NumPy**
* **OpenCV** (optional, for image recognition)
* **Matplotlib** (optional, for displaying results)
* **Jupyter Notebook / Python Scripts**



## ⚙️ Installation

1. **Clone the repository**

```bash
git clone https://github.com/yourusername/Sudoku_Solver_with_AI.git
cd Sudoku_Solver_with_AI
```

2. **Create and activate virtual environment (optional)**

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```


## ▶️ Usage

### 📝 Solving a Sudoku Grid

1. Run the script:

```bash
python sudoku_solver.py
```

2. Modify the `board` variable in the script with your puzzle input:

```python
board = [
  [5, 3, 0, 0, 7, 0, 0, 0, 0],
  [6, 0, 0, 1, 9, 5, 0, 0, 0],
  [0, 9, 8, 0, 0, 0, 0, 6, 0],
  [8, 0, 0, 0, 6, 0, 0, 0, 3],
  [4, 0, 0, 8, 0, 3, 0, 0, 1],
  [7, 0, 0, 0, 2, 0, 0, 0, 6],
  [0, 6, 0, 0, 0, 0, 2, 8, 0],
  [0, 0, 0, 4, 1, 9, 0, 0, 5],
  [0, 0, 0, 0, 8, 0, 0, 7, 9]
]
```

3. View the solution printed in the console.



### 🖼️ Solving a Sudoku from an Image (Optional)

1. Place your Sudoku image in the `images/` folder.

2. Run the image solver notebook or script:

```bash
python sudoku_solver_image.py
```

3. Follow prompts to process and solve the image-based puzzle.

> **Note:** Image solving requires **OpenCV** for preprocessing, digit segmentation, and recognition (via simple CNN or k-NN model).



## 🧠 Algorithm Overview

### 🔄 Backtracking

* Recursively fills empty cells with digits 1-9
* Checks constraints (row, column, 3x3 grid) for validity
* Backtracks when constraints are violated, exploring other options

### 🤖 Image Recognition (Optional)

* Uses OpenCV to:

  * Convert to grayscale and threshold
  * Detect the Sudoku grid contour
  * Warp perspective for top-down view
  * Segment cells and recognize digits using a pre-trained digit classifier
* Constructs puzzle array and solves with backtracking
* Overlays solution on original image



## 📊 Results

* Solves any valid Sudoku puzzle **instantly (milliseconds)** with backtracking
* Successfully detects and solves clear Sudoku images with proper preprocessing

> *(Screenshots coming soon)*



## 📁 Project Structure

```
Sudoku_Solver_with_AI/
 ┣ images/
 ┃ ┗ sample_sudoku.jpg
 ┣ models/
 ┃ ┗ digit_recognition_model.h5
 ┣ sudoku_solver.py
 ┣ sudoku_solver_image.py
 ┣ requirements.txt
 ┗ README.md
```



## 💡 Future Work

* Improve **digit recognition accuracy** with deep learning (e.g. CNN trained on MNIST)
* Build a **Streamlit web app** for interactive uploads and solutions
* Extend to **Killer Sudoku or Jigsaw Sudoku variants**
* Deploy as an **API service** for integration into mobile apps



## 🤝 Contributing

Contributions are welcome to add features, improve recognition, or extend algorithms!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to your branch (`git push origin feature/YourFeature`)
5. Open a pull request



## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.



## 📬 Contact

**Ugama Benedicta Kelechi**
[LinkedIn](www.linkedin.com/in/ugama-benedicta-kelechi-codergirl-103041300) | [Email](mailto:ugamakelechi501@gmail.com) | [Portfolio](#)



### ⭐️ If you find this project useful, please give it a star and share with computer vision and algorithm enthusiasts!

