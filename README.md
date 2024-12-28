# RVO Risk Calculator (Logistic Regression)

This project provides a web-based **Retinal Vein Occlusion (RVO)** risk calculator based on logistic regression. The calculator estimates the probability of RVO based on user input and determines whether the risk is high or low using a specified cutoff value.

## Features
- Simple and user-friendly interface.
- Calculates RVO risk probability based on:
  - Age (years)
  - Hypertension status (1: Yes, 0: No)
  - Diabetes Mellitus status (1: Yes, 0: No)
  - Diastolic Blood Pressure (mmHg)
  - Triglyceride Level (mg/dL)
  - White Blood Cell Count (10^3 cells/μL)
  - Smoking status (1: Yes, 0: No)
- Displays probability in percentage (%)
- Highlights whether the risk is **high** or **low** based on the cutoff value of **0.0061** (0.61%).

## Getting Started

### Prerequisites
You only need a modern web browser to use this project. No additional installations are required.

### Installation
1. Download or clone the repository:
   ```bash
   git clone https://github.com/your-username/rvo-risk-calculator.git
   ```
2. Open the `index.html` file in a web browser to start the calculator.

### Usage
1. Enter the required variables into the input fields:
   - Age (years)
   - Hypertension (1 for Yes, 0 for No)
   - Diabetes Mellitus (1 for Yes, 0 for No)
   - Diastolic Blood Pressure (mmHg)
   - Triglyceride Level (mg/dL)
   - White Blood Cell Count (10^3 cells/μL)
   - Smoking status (1 for Yes, 0 for No)
2. Click the **Calculate Risk** button.
3. The calculator will display the probability of RVO in percentage (%) and indicate whether the risk is **high** or **low**.

## Technical Details
The logistic regression formula used in this project:

\[
\text{Logit}(P) = -11.512 + (0.055 \cdot \text{age}) + (1.023 \cdot \text{HTN}) - (0.756 \cdot \text{DM}) + (0.031 \cdot \text{HE\_dbp}) - (0.003 \cdot \text{HE\_TG}) + (0.091 \cdot \text{HE\_WBC}) + (0.348 \cdot \text{Smoking})
\]

Where:
- **P** is the probability of RVO.
- The logit is transformed into probability using:
  \[P = \frac{1}{1 + e^{-\text{Logit}(P)}}\]

The cutoff value is **0.0061** (0.61%), above which the result is classified as **high risk**.

## File Structure
- `index.html`: Main file for the RVO risk calculator.
- `README.md`: Documentation for the project.

## License
This project is licensed under the MIT License.

## Acknowledgments
This project uses logistic regression coefficients to predict the risk of RVO. The cutoff value and coefficients were derived from a specific logistic regression analysis.

## Contact
For questions or feedback, please reach out to **Dr. Tae Keun Yoo** or open an issue in the repository.
