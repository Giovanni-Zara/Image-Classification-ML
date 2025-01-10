# Image Classification for Autonomous Driving Simulation 🚗💻

This repository contains the implementation and analysis of a machine learning project focused on controlling a car in a 2D simulation environment. The task was framed as a supervised multi-class image classification problem, where the model predicts control actions from visual input.

## Project Overview

### Objective
To develop a machine learning model capable of mapping images from the simulation environment to one of five control actions:
1. Turn Right
2. Turn Left
3. Accelerate
4. Brake
5. Maintain Current Trajectory

### Key Features
- **Dataset:** Composed of 96x96 RGB images labeled with the respective actions. Data was collected from a reinforcement learning-trained policy.
- **Preprocessing:** Normalization and efficient data loading with TensorFlow's `tf.data` API.
- **Models:** Multiple convolutional neural network (CNN) architectures were explored, optimized through hyperparameter tuning.
- **Loss Functions:** Comparative analysis of categorical crossentropy and focal loss, with special attention to dataset imbalance.

## Methodology
1. **Data Preparation:**
   - Images organized by class into training, validation, and test sets.
   - Normalization to scale pixel values to `[0, 1]`.

2. **Model Architectures:**
   - Baseline and advanced CNN models, with varying complexity.
   - Evaluation of different strategies.

3. **Performance Metrics:**
   - F1 Score (Macro-Averaged) was chosen to evaluate performance on imbalanced data.
   - Confusion matrices analyzed to understand prediction patterns.

4. **Experimentation:**
   - Different loss functions (categorical crossentropy, weighted focal loss) were tested.
   - Hyperparameter tuning for optimal model configurations.

## Results
- **Best Performing Model:** A CNN trained with categorical crossentropy, achieving the most reliable predictions for smooth driving behavior.
- **Challenges Addressed:** Dataset imbalance and its effect on model performance and driving behavior.
- **Insights:** Improved label prediction does not always correlate with better driving behavior.

## Simulation
The project includes a video showcasing the model in action within the simulation environment. This video demonstrates the car's ability to navigate the circuit using predictions from the trained model.

<div><video controls src="https://github.com/user-attachments/assets/b7b586ef-fed0-48c6-ac2d-6d26136daa0e" muted="false" ></video> Simulation of my best CNN4 model, with categorical crossentropy.
environment. </div>





## Acknowledgments
This project was completed as part of the Artificial Intelligence and Robotics course at Sapienza University of Rome.
