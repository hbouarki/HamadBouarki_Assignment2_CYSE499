# Stage 2 Hidden Test Evaluation

## Results

The Stage 1 model achieved **86.67% accuracy** on the hidden test set.

- Accuracy: 86.67%
- Balanced Accuracy: 86.67%
- Macro F1: 0.8657
- Confusion Matrix: [[234, 66], [14, 286]]

The model correctly classified 234 out of 300 negative reviews and 286 out of 300 positive reviews.

## Public vs. Hidden Test

The public test accuracy from Stage 1 was **92.25%**, while the hidden test accuracy was **86.67%**. This is a decrease of **5.58 percentage points**.

The model performed better on positive reviews than negative reviews. One possible reason is that the original training data contained more positive reviews than negative reviews. 

## What I Would Try Next

If I had more time and computing resources, I would try using more balanced training data and testing other pretrained transformer models. I would also experiment with different methods for combining predictions from chunks of long reviews.

## Use of AI

I used ChatGPT as a support tool during Stage 2. It helped me understand the assignment requirements, organize the evaluation, troubleshoot code, and interpret the model results.

I ran the evaluation using the exact Stage 1 model checkpoint and verified the outputs myself.