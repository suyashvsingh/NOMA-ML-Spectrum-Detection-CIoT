# Feature-Based Spectrum Sensing of NOMA System for Cognitive IoT Networks using Optimal Machine Learning Classifiers

This project focuses on the Rayleigh fading channels, specifically for Non-Orthogonal Multiple Access (NOMA) users. Through the use of Monte Carlo simulations, the project analyzes signal detection under varying environmental Signal-to-Noise Ratios (SNRs). Additionally, Machine Learning algorithms are applied to enhance signal detection performance.

## Libraries and Dependencies

- **numpy**: For numerical operations.
- **pandas**: Data handling and manipulation.
- **matplotlib**: Visualization and plotting.
- **scipy**: Scientific computing, used here for interpolation.
- **scikit-learn**: Machine Learning library used for training classifiers and performance evaluation.

## Constants and Parameters

- **Number of Monte Carlo iterations**: `num_iter = 10000`
- **Number of NOMA users**: `N = 2`
- **Power allocations**: `a1, a2 = 0.8, 0.2`
- **Sampled length**: `S = 4096`
- **False-alarm probability**: `Pf = 0.1`
- **Environmental SNR values**: From -25dB to 5dB.
- **Transmitter power**: `transmitter_power = 1`

## Data Generation and Signal Detection

The Monte Carlo simulation is used to:

1. Generate NOMA signals with random cyclic delays.
2. Combine signals to produce transmitted signals.
3. Add Rayleigh distributed complex normal noise.
4. Determine if NOMA signals are present using cyclic correlation.

## Machine Learning

Three ML algorithms are trained using the generated data:

- Logistic Regression (LR)
- Random Forest (RF)
- Decision Tree (DT)

Each algorithm is trained to differentiate between signals with and without the presence of NOMA signals. Their performance is then evaluated using the Receiver Operating Characteristic (ROC) curve, specifically focusing on the True Positive Rate (TPR) at a False Positive Rate (FPR) of 0.1.

## Visualization

The final step involves plotting the Probability of Detection against the Environmental SNR. This plot compares:

- Traditional signal detection method (Without ML)
- Logistic Regression (LR)
- Random Forest (RF)
- Decision Tree (DT)

## How to Run

1. Ensure you have all the necessary libraries installed.
2. Clone the repository to your local machine.
3. Run the notebook to generate the final plot comparing traditional signal detection with ML-enhanced methods under varying environmental SNRs.

## Results

Upon successful execution, a graph titled "Probability of Detection vs. Environmental SNR" will be produced. This graph provides a comparative analysis between the traditional method of signal detection and the three Machine Learning algorithms: Logistic Regression (LR), Random Forest (RF), and Decision Tree (DT). The analysis focuses on the True Positive Rate (TPR) at a Fixed False Positive Rate (FPR) of 0.1.

## Contributions

Contributions to the project are welcomed. Potential areas of contribution include:

- Optimizing the Monte Carlo simulation.
- Introducing more sophisticated machine learning algorithms.
- Enhancing visualization techniques.

---

**Note**: For a comprehensive understanding and detailed analysis, dive into the notebook.
