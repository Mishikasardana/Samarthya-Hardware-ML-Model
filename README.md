# Samarthya-Hardware-ML-Model
# Women's Safety Device - Sequential Machine Learning Model

## Overview

This project presents a **Sequential Machine Learning Model** designed for a women's safety device. The system employs a multi-stage threat detection approach, processing sensor data sequentially to identify and escalate potential threats. This CSV-driven version allows for training and evaluation using historical sensor data.

The sequential nature of the model ensures efficient processing by only engaging more complex stages when initial stages indicate a potential concern, thus optimizing resource usage and reaction time.

## System Stages

The threat detection system operates through four distinct stages:

1.  **Stage 1: Proximity Analysis**
    * **Sensor:** Proximity Sensor
    * **Purpose:** Detects the distance of objects or individuals from the user. An unusually close proximity can be an initial indicator of a potential threat.
    * **Model:** RandomForestClassifier

2.  **Stage 2: Motion Analysis**
    * **Sensor:** Accelerometer, Gyroscope
    * **Purpose:** Analyzes the user's movement patterns, including sudden changes in acceleration, rotation, or overall motion intensity. Abnormal motion could suggest struggling or unusual activity.
    * **Model:** GradientBoostingClassifier

3.  **Stage 3: Stress Detection**
    * **Sensor:** Galvanic Skin Response (GSR)
    * **Purpose:** Measures changes in skin conductivity, which can indicate physiological stress or anxiety. Elevated stress levels, when combined with other indicators, can signal distress.
    * **Model:** Support Vector Machine (SVC)

4.  **Stage 4: Voice Analysis**
    * **Sensor:** Microphone
    * **Purpose:** Analyzes audio features such as amplitude, frequency, and vocal stress patterns to identify shouts, screams, or distressed speech. This is typically the final stage for confirming high-severity threats.
    * **Model:** Multi-layer Perceptron (MLPClassifier)

---

## Features

* **Multi-Stage Threat Detection:** A cascaded system that processes sensor data through sequential stages.
* **Optimized Resource Usage:** Earlier stages can trigger early termination for "normal" scenarios, reducing computational load for safe situations.
* **Diverse ML Models:** Each stage utilizes a machine learning model optimized for its specific sensor data type.
* **Data-Driven Thresholds:** Thresholds for threat levels are learned from the training data.
* **Comprehensive Evaluation:** Provides detailed metrics including accuracy, precision, recall, F1-score, and insights into processing efficiency (average stages processed, stage usage).
* **Visualizations:** Includes plots for data distribution, processing efficiency, and confusion matrices to aid in understanding model performance.
* **CSV Integration:** Easily load and process sensor data from a standard CSV file.

---

## Setup and Installation

To run this project, you'll need Python and the following libraries.

### Prerequisites

* Python 3.x

### Installation
1.  **Install the required Python libraries:**
    ```bash
    pip install numpy pandas scikit-learn matplotlib seaborn
    ```

---

## Usage
1. **I have made my dataset you have to prepare of your own i am uploading sample dataset name test.csv.**
