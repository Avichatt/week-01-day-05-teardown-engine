# Stress Test: Tesla FSD (Full Self-Driving)
**Product Category: Edge Robotics / Vision-Only AI**

## Layer 1 — Data Foundation
A massive **Automated Video Labeling Factory**. Tesla ingests petabytes of multi-camera video from millions of cars. They've built an "Auto-Labeler" that uses larger, slower offline models to label data for the smaller, faster online models in the car.
- **Stack**: Custom Data Lakehouse, PyTorch (for labeling models), DOJO (for compute).
- **Engineering Challenge**: Data Diversity—finding the "1-in-a-million" edge case (e.g., a horse-drawn carriage on a highway) in a sea of boring highway data.
- **Hiring Skills**: Computer Vision Data Engineer - Video processing, dataset curation, auto-labeling pipelines.
- **Honesty Check**: Bleeding Edge. Their data engine is arguably their biggest competitive advantage.

## Layer 2 — Statistics & Analysis
Focused on **Safety Critical Metrics (Disengagements)**. They track "Miles per Disengagement" (MPD) and use shadow-mode testing—running the new model in the background of customer cars to see if it *would* have made a different decision than the human driver.
- **Stack**: Custom Telemetry, Grafana, A/B Testing in "Shadow Mode".
- **Engineering Challenge**: False Positives vs. False Negatives—mathematically proving that a new model is 0.1% safer before deploying to millions of cars.
- **Hiring Skills**: ML Quality Engineer - Statistical safety analysis, shadow testing infrastructure.
- **Honesty Check**: Critical. You cannot deploy a model that controls a 2-ton vehicle without exhaustive statistical proof.

## Layer 3 — Machine Learning Models
Transitioning to **End-to-End Neural Networks**. Previously a "HydraNet" (shared backbone with many heads), now moving toward V12—where the path, object detection, and steering control are all handled by one continuous network.
- **Stack**: ResNet/RegNet, Transformers (for spatial/temporal awareness), Occupancy Networks.
- **Engineering Challenge**: Temporal Consistency—ensuring the "car" at T=0 is identified as the same "car" at T=1 while occluded by a truck.
- **Hiring Skills**: Neural Architect - Vision transformers, Occupancy networks, end-to-end learning.
- **Honesty Check**: Bleeding Edge. This is the "brain" of the car. Only a few companies in the world can do this.

## Layer 4 — LLM / Generative AI
Minimal, but evolving into **World Models**. They use generative models (like GAIA) to "predict" the next frames of a driving video, essentially allowing the car to "imagine" what might happen next (like a car pulling out from a blind corner).
- **Stack**: Diffusion Models (for world simulation), Generative Adversarial Networks (GANs).
- **Engineering Challenge**: Latency in Prediction—using generative logic to predict the future without slowing down the steering reaction time.
- **Hiring Skills**: Generative AI Researcher - Video prediction models, world simulators.
- **Honesty Check**: Minimal/Emerging. This is the "future" layer for FSD, not the current backbone.

## Layer 5 — Deployment & Infrastructure
**Edge Compute on the HW3/HW4 FSD Chips**. Everything must run locally on Tesla's custom-built silicon at sub-10ms latency. No cloud-routing allowed for steering commands.
- **Stack**: Custom C++/Rust, HW3/HW4 Silicon, Minimal Linux Kernel.
- **Engineering Challenge**: Model Quantization—squeezing a massive neural net into a low-power edge chip without losing accuracy.
- **Hiring Skills**: Embedded ML Engineer - C++, TensorRT, HW-specific optimization (FP16/INT8).
- **Honesty Check**: Advanced. Most AI products run in the cloud; this has to work in a tunnel with no Wi-Fi.

## Layer 6 — System Design & Scale
**Resilient, Fault-Tolerant Distributed Sensing**. The car must handle camera obstruction, lens flares, and sensor "hallucinations" in real-time while maintaining safety.
- **Stack**: CAN bus, Real-time Operating System (RTOS) principles.
- **Engineering Challenge**: Thermal Throttling—managing CPU heat in a car on a 40°C day while running 100% compute load.
- **Hiring Skills**: Robotics Systems Architect - Fault tolerance, real-time safety systems, heat management.
- **Honesty Check**: Differentiator. The hardware-software tight coupling is the only way to achieve this scale.

---

## ARCHITECT'S FINAL VERDICT

- **Critical Path**: **Layer 1 (Data Engine)**. The one with the most data (and the best way to label it) wins.
- **The "Bottleneck"**: **Layer 5 (On-vehicle compute)**. The car's brain is fixed; they can't just "add more GPUs" to a sold car.
- **Complexity Score**: **Bleeding Edge**. High uncertainty, massive physical-world coupling.
- **Rebuilder's Priority**: Get the **Synthetic Data Generator** right. You can't crash 1,000 cars to learn how to avoid a crash; you must be able to simulate it perfectly.
