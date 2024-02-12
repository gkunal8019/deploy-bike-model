Problem Statement:

Design a Python function that performs mean-max scaling on a given dataset. Mean-max scaling is a normalization technique that scales each feature to a range between -1 and 1 based on the mean and maximum values of the feature.

Function Signature:
```python
def mean_max_scalar(data: List[float]) -> List[float]:
    pass
```

Input:
- `data`: A list of floats representing the dataset to be scaled.

Output:
- Returns a list of floats representing the scaled dataset.

Constraints:
- The input list `data` contains at least one element.
- The elements in the input list `data` are floating-point numbers.
- The length of the input list `data` does not exceed \(10^6\).

Example:
```python
data = [1, 2, 3, 4, 5]
scaled_data = mean_max_scalar(data)
print(scaled_data)  # Output should be approximately [-1.0, -0.5, 0.0, 0.5, 1.0]
```

Explanation:
Given the input list `data = [1, 2, 3, 4, 5]`, the mean is \( \frac{1+2+3+4+5}{5} = 3 \), and the maximum value is 5. After mean-max scaling, each value is transformed as follows:

\[
\text{Scaled value} = \frac{\text{Original value} - \text{Mean}}{\text{Max} - \text{Min}} = \frac{x - 3}{5 - 1}
\]

Substituting the original values:
- For \( x = 1 \), scaled value \( \approx -1.0 \)
- For \( x = 2 \), scaled value \( \approx -0.5 \)
- For \( x = 3 \), scaled value \( \approx 0.0 \)
- For \( x = 4 \), scaled value \( \approx 0.5 \)
- For \( x = 5 \), scaled value \( \approx 1.0 \)

Thus, the output should be approximately `[-1.0, -0.5, 0.0, 0.5, 1.0]`.
