# Size-and-color-identification-of-microplastics-through-the-implementation-of-YOLOv8

This project includes two notebooks, **Model Generator** and **Testing**, which enable training and evaluating a YOLOv8 model for microplastic detection, classifying them by color and size. These notebooks have been run in Google Colab.

## Notebook Structure

### 1. Model Generator

The **Model Generator** notebook focuses on setting up and training the YOLOv8 model. The steps include:

- **System Check**: Verifies the availability of GPU in the environment to ensure efficient training.
- **Dependency Installation**: Installs YOLOv8 and other necessary libraries, such as `torch` and `ultralytics`.
- **Dataset Configuration**: Loads annotation files and defines microplastic categories, including color and size.
- **Model Training**: Trains the YOLOv8 model using the prepared dataset, adjusting hyperparameters to maximize accuracy.
- **Model Saving**: Once trained, the model is saved in a file named `best.pt` for later evaluation.

### 2. Testing

The **Testing** notebook performs the evaluation of the trained model. The steps include:

- **YOLOv8 Installation**: Reinstalls YOLOv8 to ensure the testing environment matches the training setup.
- **Model Loading**: Loads the previously trained model from `best.pt` for evaluation.
- **Model Evaluation**: Uses test images to detect microplastics, obtaining metrics such as precision and recall.
- **Results Generation**: Results include the classification of microplastics by color and size, saved in a CSV file with details like the number of detected microplastics, their image locations, and categories.

## Requirements

- Python 3.10 or higher
- CUDA-compatible GPU (optional but recommended)
- Packages: `ultralytics`, `torch`, `opencv-python`, `numpy`, and other libraries installed automatically in the notebook.

## Execution

1. **Setup**: Run the **Model Generator** notebook in Google Colab to train the model. Be sure to adjust the configuration based on the available datasets.
2. **Testing**: Then, run the **Testing** notebook to test the model on new images and obtain performance metrics.

## Results

Detection and classification results are saved in a CSV file in the working directory. This file includes:

- **Number of detected microplastics by color**
- **Detection location** (latitude, longitude, country, description)
