
# Sorting Visualizer

This project is a web-based Sorting Visualizer that helps users visualize the process of different sorting algorithms in action. The user can input an array of numbers, choose a sorting algorithm, and watch how the array gets sorted step-by-step, with each step being visualized as a bar chart.

## Features

- **Multiple Sorting Algorithms**: Includes Bubble Sort, Merge Sort, Quick Sort, Selection Sort, and Insertion Sort.
- **Visualization**: Displays each step of the sorting process as a dynamic bar chart.
- **Interactive**: Users can input their own array of numbers to sort and select the algorithm to use.
- **Step-by-Step Sorting**: Each sorting algorithm is visualized step-by-step, with real-time updates to help users understand how each algorithm works.

## Technologies Used

- **Frontend**:
  - HTML
  - CSS
  - JavaScript (ES6+)
- **Backend**:
  - Python
  - Flask
- **Visualization**:
  - The visualization uses a simple bar chart where each number is represented as a bar.

## Getting Started

To run this project locally, follow the instructions below.

### Prerequisites

Ensure that you have the following installed on your machine:

- Python 3.x
- pip (Python package installer)

### Installation

1. **Clone the repository**:

    ```bash
    git clone https://github.com/your-username/sorting-visualizer.git
    cd sorting-visualizer
    ```

2. **Install the required Python dependencies**:

    Create a virtual environment (optional but recommended):

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

    Install the required libraries:

    ```bash
    pip install -r requirements.txt
    ```

3. **Install frontend dependencies** (if any):

    This project does not have specific frontend dependencies, but ensure that your static files (CSS and JS) are properly set up in the `static` directory.

### Running the Project

1. **Start the Flask server**:

    Run the following command to start the Flask development server:

    ```bash
    python app.py
    ```

2. **Open the application**:

    Open your browser and go to:

    ```
    http://127.0.0.1:5000/
    ```

    This will load the Sorting Visualizer, where you can enter an array, select a sorting algorithm, and visualize the sorting process.

## Project Structure

The project has the following structure:

```
sorting-visualizer/
│
├── app.py               # Flask app to serve the frontend and handle sorting logic
├── sorting_algorithms.py  # Contains the sorting algorithms
├── static/               
│   ├── css/
│   │   └── styles.css   # Styles for the frontend
│   └── js/
│       └── script.js    # JavaScript to handle user interaction and visualization
├── templates/
│   └── index.html       # HTML template for the frontend
└── requirements.txt     # Python dependencies for the project
```

### Files Description

- **`app.py`**: The main Python file that runs the Flask web application. It serves the `index.html` file and provides an endpoint (`/sort`) that handles the sorting logic and returns the steps of the sorting process as JSON.
  
- **`sorting_algorithms.py`**: Contains the implementations of the sorting algorithms (Bubble Sort, Merge Sort, Quick Sort, Selection Sort, and Insertion Sort). Each algorithm is visualized by passing the current state of the array after each step to a callback function.
  
- **`static/css/styles.css`**: Contains styles for the frontend to make the visualizer visually appealing and responsive on different screen sizes.
  
- **`static/js/script.js`**: The main JavaScript file that handles the visualization process. It listens for user input, sends requests to the backend to perform sorting, and dynamically updates the visual representation of the array as the sorting algorithms run.
  
- **`templates/index.html`**: The main HTML file that defines the structure of the frontend. It includes an input form for the array, a dropdown to select the sorting algorithm, and a visualization area to display the array as a bar chart.

- **`requirements.txt`**: Contains the list of required Python packages, including `Flask`.

### Requirements File (`requirements.txt`)

The `requirements.txt` should look like this:

```
Flask==2.2.2
```

### Sorting Algorithms Implemented

- **Bubble Sort**: Repeatedly steps through the list, compares adjacent items, and swaps them if they are in the wrong order.
- **Merge Sort**: Divides the array into two halves, sorts them recursively, and merges the sorted halves.
- **Quick Sort**: Picks a pivot element, partitions the array around the pivot, and sorts the subarrays recursively.
- **Selection Sort**: Repeatedly selects the smallest (or largest) element from the unsorted portion and moves it to the sorted portion.
- **Insertion Sort**: Builds the sorted array one item at a time by comparing each element with the elements already in the sorted part.

## Usage

1. **Input an Array**: Enter an array of numbers separated by commas in the input field. For example, `5, 3, 8, 6, 2`.
2. **Select a Sorting Algorithm**: Choose one of the five algorithms: Bubble Sort, Merge Sort, Quick Sort, Selection Sort, or Insertion Sort.
3. **Start Sorting**: Click the "Start Sorting" button, and the array will be sorted step by step. Each step will be displayed in the form of a bar chart.

## Contributing

Contributions are welcome! If you'd like to contribute to this project, feel free to fork the repository and submit a pull request. When submitting a pull request, please ensure your code follows the existing style and includes necessary tests if applicable.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
