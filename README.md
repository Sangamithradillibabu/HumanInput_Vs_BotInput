Project Overview:
This project detects whether a user interaction pattern is human-like or bot-like using keystroke timing analysis.
It leverages statistical features extracted from key press intervals and applies a Random Forest classifier to make accurate predictions and assign a risk score.

The system is designed to:
1.Detect automated scripts and bots
2.Allow genuine human users
3.Flag suspicious behavior with a risk-based decision system

Key Idea:
1.Humans type with natural irregularity, while bots usually type with high consistency or fixed patterns.
2.This project models that difference using:
3.Statistical measures (mean, variance, skewness, entropy, etc.)
4.Machine Learning classification
5.Probability-based risk scoring

Features Extracted:

For each typing session (keystroke interval sequence), the following features are computed:

Mean
Standard deviation
Variance
Minimum
Maximum
Skewness
Kurtosis
Entropy (distribution randomness)
Rhythm (average timing variation)

Dataset

The dataset is synthetically generated to simulate realistic scenarios:


Human (label = 1)
Natural typing with variable delays

Bot (label = 0)
Very fast fixed timing
Uniform or scripted timing patterns

Dataset Size:

1800 samples total
600 human samples
1200 bot samples

Model Used

Algorithm: Random Forest Classifier

Trees: 300

Max Depth: 12

Why Random Forest?

1.Handles non-linear patterns well
2.Robust to noise
3.Works great with statistical features
