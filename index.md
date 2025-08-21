---
editor_options:
  markdown: null
---
# Outlier Detection via DBSCAN

## Contents

-   What Exactly Does DBSCAN Do for Outlier Detection?
-   What's The Secret?
-   What Other Topics Should I Cover In My work?
-   Why Does All This Matter?
-   In Summary:

**By:** Javier E. De Moya Figueroa and M.Sc. Carlos M. De Oro
Aguado & Dr. Jorge I. Vélez, PhD\
**Posted on:** July 14, 2025

![](/home/jdemoya/Downloads/Statistician_03_Funny.png){width=50%}

*Fig 1. Statistician "searching for outliers" in datasets. Source:(AI-generated)*

Imagine you have a massive dataset full of customer transactions, sensor
readings, or medical measurements. And now imagine you want to
automatically discover which data points are unusual or suspicious,
without manually checking each one. Sounds useful? That's exactly what a
technique with a fancy name does: **Density-Based Spatial Clustering of
Applications with Noise**, or **DBSCAN** for short.

This blog summarizes and adapts part of the research developed by student
Javier E. De Moya Figueroa with advisors Carlos M. De Oro Aguado and
Jorge I. Vélez as part of the Master's in Applied Statistics. The work
is titled **"Outlier Detection via DBSCAN"**. We wrote it
with the aim of explaining what DBSCAN is and why it's so useful today
for finding anomalies in data in a simple way. And don't worry: we'll
explain it here without technical jargon.

## What Exactly Does DBSCAN Do for Outlier Detection?

![](/home/jdemoya/Downloads/DBSCAN_01_clustering.png){width=50%}

*Fig 2. Representation of DBSCAN's outlier detection objective. Source:(AI-generated)*

Think of DBSCAN as an automatic anomaly detector. You give it a bunch
of data points, and it replies with something like:

-   "These points form normal clusters and belong to the main pattern."
-   "This point is isolated and doesn't have enough neighbors - it's an
    outlier!"
-   "This group of points is too sparse to be considered normal
    behavior."

And all that without telling it in advance what normal or abnormal
should look like! The magic is that it **discovers the outliers by
itself**, simply by analyzing the density patterns in the data.

## What's The Secret?

![](/home/jdemoya/Downloads/DBSCAN_01_points.png){width=50%}

*Fig 3. Representation of core points, border points, and noise points in DBSCAN. Source: (AI-generated)*

Even though it may sound like sorcery, DBSCAN is based on
well-thought-out mathematical ideas. But don't worry: with a bit of
intuition, it's understandable. In this work, we explain step-by-step
how it all works. Here are some of the key ideas:

### 1. How do data points behave in space?

Some points cluster together densely, and that gives us clues. For
example, if customer purchases cluster around certain amounts and times,
isolated transactions far from these patterns might be fraudulent.

### 2. How are outliers identified?

We use a density-based method that classifies each point as: - **Core
point**: Has many neighbors within a specified radius - **Border
point**: Has fewer neighbors but is near a dense region\
- **Noise point**: Has very few neighbors and is isolated - **these are
our outliers!**

### 3. How is this model optimized?

We use parameter optimization techniques to find the best values for the
neighborhood radius (ε) and minimum points (MinPts). It's like
fine-tuning a telescope to see anomalies more clearly while avoiding
false alarms.

## What Other Topics Should I Cover In My work?

Besides explaining how DBSCAN works for outlier detection, I also
discuss:

-   How to represent data in a way that machines can understand density
    patterns.
-   How to prepare datasets so the model can work effectively with
    different types of variables.
-   A comprehensive comparison with 18 other outlier detection methods
    including classical (Z-Score, Grubbs), robust (BACON), and machine
    learning approaches.
-   A real-world evaluation using simulated data to test performance
    under controlled conditions (okay, this part is a bit more
    technical, but it shows the power and limitations of this tool!).

## Why Does All This Matter?

We're surrounded by data that can hide important anomalies. Techniques
like DBSCAN allow us to:

-   **Detect fraud** in financial transactions automatically.
-   **Identify equipment failures** before they cause major problems.
-   **Find unusual patterns** in medical data that might indicate rare
    conditions.
-   **Quality control** in manufacturing processes.
-   **Cybersecurity** by spotting unusual network behavior.

Better understand what's hidden in our data... without having to examine
everything manually!

## In Summary:

This work is a practical and accessible guide on how to uncover hidden
outliers in large amounts of data using DBSCAN in a clear and useful
way. Even though there's math behind it, the goal is simple: to help
people (and machines) better identify the unusual and potentially
important anomalies in the information around us.

**Key findings from our research:** - DBSCAN shows high specificity
(95%) but lower recall (58%) compared to specialized outlier detection
methods - Classical methods like Hotelling's T² and Mahalanobis distance
significantly outperform DBSCAN in F1-Score - DBSCAN adopts a
conservative approach, prioritizing minimal false positives over
exhaustive detection - The percentage of outliers in the data is the
most influential factor affecting performance - While DBSCAN wasn't
designed specifically for outlier detection, it remains a viable
alternative to traditional statistical methods

## Affiliations

**Javier E. De Moya Figueroa:** Master's in Applied Statistics,
Universidad del Norte, Colombia.

**Carlos M. De Oro Aguado, MSc:** Tutor, Universidad del Norte,
Colombia.

**Dr. Jorge I. Vélez, PhD:** Tutor, Universidad del Norte, Colombia.
