# Voice Recognition for Mental Health

## Overview
This project demonstrates a voice recognition system using the Arduino Nano 33 BLE Sense, designed to identify keywords related to absolutist language, relevant in the context of mental health diagnostics. Keywords include "all", "only", "must", "none", "never", and periods of silence. The system aims to provide a tool for monitoring language markers potentially indicative of mental health states, rather than diagnosing conditions directly.

### Author
- Pranit Sehgal - *Arizona State University* - [1225456193]

## Project Link
- [Edge Impulse Studio Project](https://studio.edgeimpulse.com/public/309235/latest)
- Dataset ( self collected data, if you need access to it contact me on pvsehgal@asu.edu )

### Data Collection
- **Sources**: Personal voice recordings and student contributions.
- **Method**: Utilized the Harvard open speech recording tool.
- **Storage**: Stored in 'audio' folder with subfolders for each keyword, in .wav format.
- **Augmentation**: Combined with the Simple Speech Command dataset for a comprehensive training set.

### Dataset Details
- **Keywords**: 6 (including silence).
- **Total Samples**: 2531 (2025 for training, 506 for testing).
- **Format**: .wav files.
- **Split**: 80% training, 20% testing.


### Design
- **Tool**: Edge Impulse software.
- **Architecture**: Sequential 1D CNNs, including an "Audio (MFCC) processing block".

### Training
- **Cycles**: 100.
- **Learning Rate**: 0.005.
- **Parameters**: Pooling layer (8 neurons, 3 kernel size), Dropout Rate: 0.25, Flattening.

## Results

- **Accuracy**: 96.8%
- **Loss**: 0.19
- **Inference Time**: 3ms
- **Memory Usage**: Peak RAM: 3.8k, Flash: 31.6k

## Demo
https://drive.google.com/file/d/1bSiBapBsx0R0te8azuRlGFuSWncwjrBX/view?usp=sharing

### Achievements
Successfully developed a high-accuracy voice recognition system that showcases potential for monitoring mental health markers through speech.

### Challenges & Future Directions
Enhancing the model's sensitivity to similar sounding words and silence. Future iterations could explore sophisticated audio processing techniques and neural network architectures.

## Installation

1. Clone the repository to your local machine.
2. Ensure you have the necessary tools and libraries installed for Arduino development and Edge Impulse projects.
3. Follow the setup instructions on Edge Impulse's documentation for deploying to Arduino Nano 33 BLE Sense.

## Usage
Deploy the system to continuously monitor for specified keywords in speech, potentially indicating mental health states. Ideal for integrating into wearable technologies for mental health monitoring.

## Contributing
Contributions to improve the system, address challenges, or extend functionality are welcome. Please submit pull requests or open issues to discuss proposed changes.

## Acknowledgments
- Contributions from students and the use of the Harvard open speech recording tool were invaluable.
- Edge Impulse for providing a platform for developing and training the machine learning model.

## Contact
For any queries or further information, please reach out to Pranit Sehgal at pranitsehgal@gmail.com.

