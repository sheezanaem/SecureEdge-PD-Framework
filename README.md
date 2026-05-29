# SecureEdge-PD: An Attention-Augmented Multi-Modal Edge-Cloud Framework for Continuous Parkinson's Disease Monitoring and UPDRS Assessment

SecureEdge-PD is a distributed, five-layer IoT-Edge-Cloud architecture designed for continuous, remote monitoring of Parkinson's Disease (PD) motor and vocal symptoms. The framework enables real-time automated Unified Parkinson's Disease Rating Scale (UPDRS) scoring while maintaining strict data privacy and optimized computational efficiency.

---

## Key Features & 5-Layer Architecture

The framework manages high-throughput telemetry streams across five specialized infrastructure layers:

1. **Perceptual Sensing Layer:** Continuous data acquisition via wrist-worn smartwatches (100 Hz bilateral 6-axis IMU signals tracking gait/tremor dynamics) and smartphone microphones (acoustic phonation data).
2. **Edge Filtering & Processing Layer:** Real-time localized signal conditioning executing a **4th-order Butterworth filter** directly on the patient's smartphone to mitigate high-frequency artifacts and motion noise.
3. **Network Transport Layer:** Secure, low-latency transmission protocols ensuring encrypted data synchronization.
4. **Cloud Analytics Infrastructure:** A HIPAA-eligible AWS cloud backend managing feature extraction, deep learning inference, and sequential data persistence.
5. **Application Interface:** Interactive clinician dashboards for monitoring continuous intra-day fluctuations and remote clinical decision support.

---

## Core Methodology & Deep Learning Optimization

* **Multi-Modal Data Fusion:** Independent dual-branch processing pipelines that synthesize irregular temporal movement patterns and spectral vocal features.
* **Attention-Augmented Modeling:** Specialized temporal attention layers to lock onto transient behavioral anomalies and contextual dependencies across modalities.
* **Parameter-Efficient Convolution (DSConv):** Replaces dense traditional convolutions with **Depthwise Separable Convolutions (DSConv)**, drastically reducing parameter overhead and allowing high-fidelity processing on standard configurations.
* **Explainable AI (XAI) Validation:** Integrates interpretive diagnostic structures (such as feature attribution and segment tracking) to maintain biological alignment with neurological indicators, fostering expert clinical reliance.

---

## Project Structure

```text
SecureEdge-PD-Framework/
├── notebooks/
│   └── cloud-article-final.ipynb    # End-to-end data processing, DSConv modeling, and evaluation
├── .gitignore                       # Standard Python exclusions (e.g., checkpoints, cache)
└── README.md                        # Comprehensive system documentation
