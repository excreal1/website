+++
title = 'Example Questions'
date = 2024-06-03T04:15:50Z
draft = false
+++

1. **Question:** A manufacturer claims that the mean lifespan of their product is 5000 hours. A sample of 50 products yielded a mean lifespan of 4900 hours with a standard deviation of 200 hours. At a significance level of 0.05, can we reject the manufacturer's claim?

   **Solution:** 
   
   - Null Hypothesis (H0): μ = 5000
   - Alternative Hypothesis (H1): μ ≠ 5000
   - Standard error of the mean (SEM) = σ / √n = 200 / √50 ≈ 28.28
   - Z-score = (4900 - 5000) / 28.28 ≈ -3.54
   - The critical Z-value for a significance level of 0.05 (two-tailed) is approximately ±1.96.
   - Since -3.54 < -1.96, we reject the null hypothesis. There is sufficient evidence to conclude that the mean lifespan is not 5000 hours.

2. **Question:** In a survey, 150 people were asked about their preference between two brands. 80 people preferred Brand A. Can we conclude that Brand A is preferred by more than 50% of the population at a significance level of 0.01?

   **Solution:**
   - Null Hypothesis (H0): p = 0.50
   - Alternative Hypothesis (H1): p > 0.50
   - Sample proportion (p̂) = 80/150 ≈ 0.533
   - Standard error of the proportion (SE) = √(p(1-p)/n) ≈ √((0.50 * 0.50)/150) ≈ 0.055
   - Z-score = (0.533 - 0.50) / 0.055 ≈ 0.6
   - The critical Z-value for a significance level of 0.01 (one-tailed) is approximately 2.33.
   - Since 0.6 < 2.33, we fail to reject the null hypothesis. There is not enough evidence to conclude that Brand A is preferred by more than 50% of the population.

3. **Question:** A researcher wants to know if there is a relationship between hours spent studying and exam scores. They collect data from 50 students and find a correlation coefficient of 0.70. At a significance level of 0.05, is there a significant correlation between study hours and exam scores?

   **Solution:**
   - Null Hypothesis (H0): ρ = 0 (No correlation)
   - Alternative Hypothesis (H1): ρ ≠ 0 (Correlation exists)
   - Degrees of freedom (df) = n - 2 = 50 - 2 = 48
   - Critical value for a two-tailed test with df = 48 and α = 0.05 is approximately ±0.291.
   - Since 0.70 > 0.291, we reject the null hypothesis. There is sufficient evidence to conclude that there is a significant positive correlation between study hours and exam scores.

4. **Question:** A company wants to test if there is a difference in mean productivity between two departments. In Department A, the mean productivity of 30 employees is 55 units per hour with a standard deviation of 5, while in Department B, the mean productivity of 25 employees is 60 units per hour with a standard deviation of 6. Can we conclude that there is a significant difference in mean productivity between the two departments at a significance level of 0.05?

   **Solution:**
   - Null Hypothesis (H0): μA - μB = 0
   - Alternative Hypothesis (H1): μA - μB ≠ 0
   - Pooled standard deviation (Sp) = √(((n1-1)*s1^2 + (n2-1)*s2^2) / (n1 + n2 - 2)) ≈ √(((29*5^2) + (24*6^2)) / (30 + 25 - 2)) ≈ 5.35
   - T-score = ((55 - 60) - 0) / (5.35 * √(1/30 + 1/25)) ≈ -3.32
   - The critical t-value for a two-tailed test with df = 53 and α = 0.05 is approximately ±2.004.
   - Since -3.32 < -2.004, we reject the null hypothesis. There is sufficient evidence to conclude that there is a significant difference in mean productivity between the two departments.

5. **Question:** A biologist wants to know if there is a difference in the average height between two species of plants. She collects data from 20 plants of each species. The mean height of species A is 25 cm with a standard deviation of 3 cm, while the mean height of species B is 22 cm with a standard deviation of 2.5 cm. Is there a significant difference in average height between the two species at a significance level of 0.01?

   **Solution:**
   - Null Hypothesis (H0): μA - μB = 0
   - Alternative Hypothesis (H1): μA - μB ≠ 0
   - Pooled standard deviation (Sp) = √(((n1-1)*s1^2 + (n2-1)*s2^2) / (n1 + n2 - 2)) ≈ √(((19*3^2) + (19*2.5^2)) / (20 + 20 - 2)) ≈ 2.75
   - T-score = ((25 - 22) - 0) / (2.75 * √(1/20 + 1/20)) ≈ 7.27
   - The critical t-value for a two-tailed test with df = 38 and α = 0.01 is approximately ±2.704.
   - Since 7.27 > 2.704, we reject the null hypothesis. There is sufficient evidence to conclude that there is a significant difference in average height between the two species.

6. **Question:** A car manufacturer claims that their cars have an average fuel efficiency of 30 miles per gallon (mpg). A random sample of 25 cars yields a mean fuel efficiency of 28 mpg with a standard deviation of 5 mpg. Test the manufacturer's claim at a significance level of 0.05.

   **Solution:**
   - Null Hypothesis (H0): μ = 30
   - Alternative Hypothesis (H1): μ ≠ 30
   - Standard error of the mean (SEM) = σ / √n = 5 / √25 = 1
   - Z-score = (28 - 30) / 1 = -2
   - The critical Z-value for a significance level of 0.05 (two-tailed) is approximately ±1.96.
   - Since -2 < -1



## Explaination

**Question:** A manufacturer claims that the mean lifespan of their product is 5000 hours. A sample of 50 products yielded a mean lifespan of 4900 hours with a standard deviation of 200 hours. At a significance level of 0.05, can we reject the manufacturer's claim?

**Solution:** 
- **Null Hypothesis (H0):** The manufacturer's claim is true; the mean lifespan of their product is 5000 hours (\(μ = 5000\)).
- **Alternative Hypothesis (H1):** The manufacturer's claim is not true; the mean lifespan of their product is not 5000 hours (\(μ ≠ 5000\)).
- Standard error of the mean (SEM): 
  - \(SEM = \frac{σ}{\sqrt{n}} = \frac{200}{\sqrt{50}} \approx 28.28\)
- Z-score: 
  - \(Z = \frac{\bar{X} - μ}{SEM} = \frac{4900 - 5000}{28.28} \approx -3.54\)
- Critical Z-value: 
  - For a significance level of 0.05 (two-tailed), critical Z-value is approximately ±1.96.
- Conclusion: 
  - Since -3.54 is less than -1.96 (in absolute value), we reject the null hypothesis. There is sufficient evidence to conclude that the mean lifespan is not 5000 hours, as claimed by the manufacturer.
