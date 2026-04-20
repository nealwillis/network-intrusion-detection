# Network Intrusion Detection System

## Overview
A machine learning model that detects malicious network traffic using the 
DARPA KDD Cup 1999 dataset. Built to demonstrate how anomaly detection 
techniques can be applied to cybersecurity threat identification.

## The Problem
Network traffic is a constant stream of connections between computers. 
Most of it is normal. Some of it is an attack. The challenge is teaching 
a model to tell the difference automatically, at scale.

## Dataset
- Source: DARPA KDD Cup 1999 (via scikit-learn)
- 494,021 network connections
- Labels: Normal traffic vs. attack traffic

## Model
Random Forest Classifier (100 trees)
- Each tree independently evaluates a connection
- Majority vote determines the final classification
- Same ensemble approach used in production threat detection systems

## Results
- 99.98% attack detection rate
- 79,264 out of 79,276 attacks correctly identified
- Only 3 false alarms out of 19,529 normal connections

## Key Findings
The model identified three primary indicators of malicious traffic:
- Connection frequency -- attacks hammer systems at inhuman speeds
- Data volume -- unusual amounts of data transferred in either direction
- Authentication status -- most attacks occur without valid credentials

## Tools
Python, scikit-learn, pandas, NumPy, Matplotlib, Seaborn, Google Colab

## Context
This project applies the same anomaly detection techniques used in my 
prior research work to a defense-relevant problem. The goal was to 
demonstrate that ML-based threat detection is fundamentally a pattern 
recognition problem -- the same skills transfer directly.
