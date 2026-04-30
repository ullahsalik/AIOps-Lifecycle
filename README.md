---
# AIOps-Lifecycle

### Experiment: MLflow Instrumentation for Reproducible AIOps Model Training

**What**
This experiment focuses on transforming an anomaly detection training workflow into a reproducible and trackable ML pipeline by instrumenting `train.py` with MLflow. The setup enables systematic logging of parameters, metrics, and artifacts, along with model packaging for consistent execution across environments.

**Why**
In AIOps use cases such as anomaly detection and incident prediction, reproducibility and traceability are critical for debugging, governance, and continuous improvement. This experiment addresses the limitations of ad-hoc experimentation by introducing structured experiment tracking and artifact management, ensuring that model performance and behavior can be reliably audited and compared.

**How**

* Integrated MLflow Tracking API into `train.py` to log hyperparameters, anomaly detection metrics, and model artifacts
* Configured MinIO as an S3-compatible backend for scalable artifact storage
* Created `MLproject` and `conda.yaml` to standardize runtime environments and enable reproducible runs via MLflow CLI
* Executed multiple experiment runs with varying configurations and tracked them through the MLflow UI
* Registered the trained model in the MLflow Model Registry for versioning and downstream deployment

**Result**
The experiment established a fully traceable training workflow where all runs are versioned and reproducible, with the final model successfully registered in MLflow and achieving strong anomaly detection performance (~94% accuracy).

---

If you want, I can tailor this further to match your exact repo structure or make it more “GitHub-polished” (badges, architecture diagram section, etc.).
