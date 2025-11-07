# Athlete speed analysis using video processing and spark
## Abstract
This project leverages Big Data analytics to automate athlete speed detection using video processing. By integrating YOLOv8, DeepSORT, and Apache Spark, the system efficiently processes race videos to estimate each athlete’s real-time speed and performance metrics at scale.

## Methodology
The project integrates computer vision with Big Data analytics to estimate athlete speed in real time.

Step 1: Detection — YOLOv8 identifies athletes in each frame.

Step 2: Tracking — DeepSORT assigns a unique ID to each athlete, maintaining consistency across frames.

Step 3: Speed Estimation — Displacement of bounding boxes between consecutive frames is converted to real-world speed using video frame rate and scaling parameters.

Step 4: Spark Integration — Apache Spark performs distributed processing on extracted data, computing metrics such as average and maximum speeds for all athletes.

Step 5: Visualization — The processed video displays each athlete’s ID, real-time speed (km/h), and trajectory.

## Results / Insights
The system accurately tracked six athletes throughout the race without ID mismatches.
Average speed: 23.5 km/h  Maximum speed: 28.1 km/h
Spark enabled parallelized data analysis, reducing computational time by over 60% compared to sequential processing.
The visualization layer provided clear and interpretable feedback for coaches and analysts, enhancing decision-making in sports performance evaluation.
