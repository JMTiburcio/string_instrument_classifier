# String Instrument Classifier

A machine learning project that classifies string instruments using computer vision and deep learning techniques. This project uses FastAI and ResNet18 to train a model that can identify different types of string instruments from images.

## 🎵 Supported Instruments

The classifier can identify the following string instruments:
- Violin
- Cello
- Acoustic Guitar
- Electric Guitar
- Piano
- Ukulele

## 🚀 Features

- **Automated Data Collection**: Uses DuckDuckGo search to automatically collect training images
- **Data Validation**: Automatically verifies and cleans downloaded images
- **Data Augmentation**: Implements random resizing, cropping, and other transformations to improve model robustness
- **Interactive Cleaning**: Provides a GUI tool for manually reviewing and cleaning misclassified images
- **Model Training**: Fine-tunes a ResNet18 model using transfer learning
- **Performance Analysis**: Includes confusion matrix and loss analysis tools

## 📋 Requirements

- Python 3.9+
- FastAI 2.0+
- PyTorch
- Additional dependencies listed in `requirements.txt`

## 🛠️ Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd string_instrument_classifier
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## 📖 Usage

1. **Run the Jupyter Notebook**:
   - The notebook will automatically download training images for each instrument type
   - Clean and validate the downloaded images
   - Train the model using transfer learning
   - Provide tools for model evaluation and data cleaning

## 📁 Project Structure

```
string_instrument_classifier/
├── main.ipynb              # Main Jupyter notebook with the complete pipeline
├── requirements.txt        # Python dependencies
├── images/                 # Sample images for testing
│   ├── piano.jpg
│   └── violin.jpg
├── string_instruments/     # Training data organized by instrument type
│   ├── acoustic guitar/
│   ├── cello/
│   ├── electric guitar/
│   ├── piano/
│   ├── ukulele/
│   └── violin/
└── venv/                   # Virtual environment
```

## 🔧 Technical Details

- **Model Architecture**: ResNet18 with transfer learning
- **Image Processing**: 224x224 pixel input with data augmentation
- **Training Strategy**: Fine-tuning with 4-5 epochs
- **Data Split**: 80% training, 20% validation
- **Image Sources**: DuckDuckGo image search API

## 🎯 Model Performance

The model achieves high accuracy in classifying string instruments. Performance metrics and confusion matrices are generated automatically during training and can be visualized using the built-in tools.

## 🧹 Data Cleaning

The project includes an interactive data cleaning tool (`ImageClassifierCleaner`) that allows you to:
- Review model predictions
- Delete misclassified images
- Reassign images to correct categories
- Improve model performance through data quality

## 🔍 Troubleshooting

- **Apple Silicon Compatibility**: The notebook includes MPS fallback settings for Apple Silicon Macs
- **Image Download Issues**: If image downloads fail, the verification step will automatically remove corrupted files
