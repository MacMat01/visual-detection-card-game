[![CodeQL](https://github.com/MacMat01/cards-object-detection/actions/workflows/codeql.yml/badge.svg)](https://github.com/MacMat01/cards-object-detection/actions/workflows/codeql.yml)

# Strategic Fruits Card Detection

This project aims to detect strategic fruits cards using YOLOv8. It is implemented in Python and uses several libraries
for data processing and model training.

## Project Structure

The project has the following structure:

- `src/main/python/model_training/strategic-fruits-card-detection-dataset/`: Contains the dataset used for training the
  model.
- `environment.yml`: Contains the conda environment configuration.

## Getting Started

### Prerequisites

Ensure you have the following installed on your system:

- Python 3.12.3
- Conda package manager
- Cuda Toolkit 11.1 or higher

### Installation

1. Clone the repository:

```bash
git clone https://github.com/MacMat01/strategic-fruits-card-detection.git
```

1. Navigate to the project directory:

```bash
cd strategic-fruits-card-detection
```

2. Create a new conda environment from the `environment.yml` file:

```bash
conda env create --name <your-environment-name> -f environment.yml
```

3. Activate the conda environment:

```bash
conda activate <your-environment-name>
```

4. Install the `build` and `pip` tools:
```bash
pip install --upgrade build pip
```

5. Build a source distribution (sdist) and a binary distribution (wheel) of your package:

```bash
python -m build
```

6. Install the package from the wheel file:

```bash
pip install dist/*.whl # If it doesn't work, in my case the specific command was pip install dist/strategic_fruits_card_detection-0.1.0-py3-none-any.whl 
```

7. (OPTIONAL) If gpu isn't working for model training, install pytorch-cuda manually (remember to restart pc, it often works):

```bash
conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
```

### Running the Application

#### For Using the Main Application

To run the main application, navigate to the `src/main/python/app` directory and run the `app.py` script:

```bash
cd src/main/python/app
```

```bash
python app.py
```

#### For Creating Your Own Card Detection

Follow the instruction in the following Jupyter notebooks:

1. `Cards Extraction.ipynb`
2. `Dataset Creation.ipynb`
3. `Strategic Fruits Card Detection - YOLOv8.ipynb`

Ensure you have Jupyter installed in your environment, and start it with:

```bash
jupyter notebook
```

Navigate to the `notebooks` directory and open the respective notebook.

## License

This project is licensed under the MIT License—see the [LICENSE](LICENSE) file for details.
