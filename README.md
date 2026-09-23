# AI Image Classifier

An AI-powered image classification web application built with **Python, Streamlit, TensorFlow, and MobileNetV2**.

The application allows users to upload an image and uses the pre-trained **MobileNetV2** model with ImageNet weights to identify what is present in the image.

## Features

* Upload JPG and PNG images
* Uses a pre-trained MobileNetV2 deep learning model
* Displays the top 3 predictions
* Shows the confidence score for each prediction
* Simple and user-friendly Streamlit interface
* No OpenAI API key required

## Technologies Used

* **Python**
* **Streamlit** – Web application interface
* **TensorFlow / Keras** – Deep learning framework
* **MobileNetV2** – Pre-trained image classification model
* **OpenCV** – Image resizing and processing
* **NumPy** – Numerical operations
* **Pillow (PIL)** – Image handling

## How It Works

1. The user uploads an image.
2. The image is converted into a NumPy array.
3. The image is resized to **224 × 224 pixels**, which is the input size expected by MobileNetV2.
4. The image is preprocessed using MobileNetV2's preprocessing function.
5. The processed image is passed to the pre-trained MobileNetV2 model.
6. The model predicts the most likely objects/classes in the image.
7. The application displays the **top 3 predictions** with their confidence scores.

## Project Structure

```text
AI image classifier/
│
├── src/
│   └── ai_image_classifier/
│       ├── __init__.py
│       └── main.py
│
├── .gitignore
├── pyproject.toml
├── uv.lock
└── README.md
```

## Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
```

### 2. Open the project folder

```bash
cd "AI image classifier"
```

### 3. Install the required dependencies

If you are using `uv`:

```bash
uv sync
```

## Running the Application

If `main.py` is inside:

```text
src/ai_image_classifier/main.py
```

run:

```bash
uv run streamlit run src/ai_image_classifier/main.py
```

Streamlit will start the application and provide a local URL in the terminal.

Open that URL in your browser.

## Example

Upload an image such as a dog, cat, car, or other recognizable object.

The application may produce results such as:

```text
Predictions

Labrador retriever: 92.45%
Golden retriever: 4.21%
German shepherd: 1.83%
```

The exact predictions and confidence scores depend on the uploaded image.

## Model

This project uses **MobileNetV2** with weights trained on the **ImageNet** dataset.

MobileNetV2 is a lightweight convolutional neural network designed for image classification and other computer vision tasks.

The model is loaded using:

```python
MobileNetV2(weights="imagenet")
```

## Important Note

This project **does not use the OpenAI API**, so an `OPENAI_API_KEY` is not required.

The MobileNetV2 model is downloaded automatically when it is first loaded if the required model weights are not already available locally.

## Future Improvements

Possible improvements include:

* Support for more image formats
* Displaying the uploaded image with better UI
* Adding a prediction history
* Adding more detailed class information
* Improving the user interface
* Supporting custom-trained image classification models
* Deploying the application online

## Author

**Arshad Syed**

This project was created as a practical project to learn and demonstrate image classification using deep learning and Streamlit.
