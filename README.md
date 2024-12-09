## How to Find the Best-Fit Line using Least Squares?

<p align="center">
  <img src="https://github.com/user-attachments/assets/ae3bdc9f-0cfd-46e9-bbd1-6c4b3f62a024" width="350">
  <br><strong>Draw an Initial Line</strong>
</p>

- Starts by drawing an initial line through the data points.
- The average y-value is denoted as b, representing the y-intercept of the initial line.
- This line is random and serves as a starting point. It doesn't necessarily minimize the errors yet.

<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/756e5238-3e0d-4611-94a1-575ed7498eb6" width="350">
  <br><strong>Distance from the Line to the First Data Point</strong>
</p>

- The distance between the first data point $(x_1, y_1)$ and the line is calculated as $b - y_1$.
- This distance is called the residual, which indicates the prediction error of the line for that data point.

<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/b15ea80e-79b9-4260-9e0d-6eebeadffa9e" width="350">
  <br><strong>Summing Residuals for Two Points</strong>
</p>

- Continue by finding the residual for the next data point.
- At this stage, the total distance (sum of residuals) from the line to the first two points is calculated as $(b - y_1) + (b - y2)$.
- This shows how prediction errors from multiple points are combined to assess the overall fit of the line.

<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/a91467d4-4f99-4205-8b63-85c75d3bdac6" width="350">
  <br><strong>Adding the Third Data Point to the Sum</strong>
</p>

- The process is extended by including the third data point: $(b - y_1) + (b - y_2) + (b - y_3)$.
- The cumulative sum of residuals increases as additional points are considered.

<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/04e30f4c-c0fb-4fd3-ab47-83c0fad42342" width="350">
  <br><strong>Negative Residual Issue</strong>
</p>

- For the $4^{th}$ data point $(x_4, y_4)$, since $y_4 > b$, the residual $b - y_4$ becomes negative.
- Negative residuals reduce the total sum, which can give a false impression of how well the line fits the data.
- This problem highlights the need for a method to properly handle negative values.

<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/13ab972e-c8d0-4fa8-a7a9-81b1e7bbdbcd" width="350">
  <br><strong>Squaring the Residuals</strong>
</p>

- To address the negative residual problem, each residual is squared: $(b - y_1)^2 + (b - y_2)^2 + (b - y_3)^2 + (b - y_4)^2 + (....)^2$
- Squaring ensures that all prediction errors are positive, avoiding the cancelation effect of negatives.
- This step introduces the concept of "Sum of Squared Residuals" as a metric for evaluating fit.

<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/52f1229c-c574-4d78-a3ff-bec024428b6a" width="350">
  <br><strong>Fitting a Sloped Line</strong>
</p>

- The line is rotated to better match the data, minimizing the distances (residuals) between the points and the line.
- Residuals are recalculated for the sloped line, and the sum of squared residuals is compared to the previous line.
- The sloped line generally provides a better fit than the initial horizontal line.

<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/fdf6b145-397e-4fd0-91d9-9ac2868dddf2" width="350">
  <br><strong>Further Rotating the Line</strong>
</p>

- The line is rotated further, continuing the optimization process.
- With each adjustment, the sum of squared residuals is calculated to find the line that minimizes this value.
- The goal is to find the "sweet spot", where the line achieves the smallest sum of squared residuals and best represents the trend in the data.

<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/413c7d16-5476-4997-8bf7-74ac1a8d4180" width="350">
  <br><strong>Final Selection of the Line</strong>
</p>

- X-axis: Represents different rotations(slopes) of the line.
- Y-axis: Represents sum of squared residuals (SSR).
- Initially, as the line is rotated (from a flat horizontal line), the SSR decreases because the fit improves.
- At a specific point (marked as the red circle), the SSR reaches its lowest value. This is the "sweet spot" where the line fits the data best, achieving the least squares.
- Rotating the line further increases the SSR, as the line starts to deviate from the oprimal fit.
- The line that gives the lowest SSR is selected as the best-fit line. 

Reference: [StatQuest](https://www.youtube.com/watch?v=PaFPbb66DxQ)



