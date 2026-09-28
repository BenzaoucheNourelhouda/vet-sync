# VET-SYNC: Multimodal Dairy Cattle Health Monitoring

*Master's thesis project. Code and data are not yet public.*

## Intro
Sensor-based monitoring can tell you that a cow's behavior has changed, but
not why. Vision-based diagnosis can identify visible disease, but only if
someone already knows which animal to look at. VET-SYNC connects the two: a
sensor anomaly on a specific cow triggers analysis of the matching camera
footage, then produces an explained, reviewable report for a veterinarian.

## Technologies
Python · Deep learning (segmentation and CNN classification) · Explainable AI
(Grad-CAM) · LLM-based report generation · Web dashboard with live alerts

## Features
- Continuous anomaly detection based on each cow's own normal behavior
- Automatic retrieval of the camera footage matching the alert
- Body-region segmentation to focus the analysis on the relevant area
- Disease classification with a confidence score
- Visual explanations showing what the model focused on
- Automated veterinary report with suggested management, for vet review
- Dashboard with live notifications

## Process
1. **Detect:** sensor data flags an abnormal state for an individual cow.
2. **Link:** the alert is matched to the corresponding visual evidence by cow
   identity and time.
3. **Localize:** segmentation isolates the relevant body region.
4. **Classify:** disease-specific models estimate the likely condition.
5. **Explain:** heatmaps show the evidence behind the prediction.
6. **Report:** a structured report is generated for veterinary confirmation.

## What I learned
- Matching data from different sources by animal and time is as important as
  the models themselves.
- Evaluating monitoring data chronologically, not randomly, avoids overly
  optimistic results.
- Comparing each animal to its own baseline is more meaningful than using
  fixed thresholds.
- Explainability makes the outputs easier for non-ML users to trust.

## What could be improved
- Validation on more farms, animals, and disease cases
- Broader disease coverage
- Stronger end-to-end evaluation of the full pipeline
- Testing in real farm conditions with veterinary feedback

## Contact
[LinkedIn]((https://www.linkedin.com/in/nour-el-houda-benzaouche-48401a371/)) · nour339be@gmail.com
