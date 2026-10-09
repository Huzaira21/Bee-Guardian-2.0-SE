# Bee Guardian 2.0

**A Smart Beehive Health Monitoring System Using Embedded Multimodal Technology**

**Course:** CSC-225 – Software Engineering (Complex Computing Problem)
**Department:** Computer Science, Namal University, Mianwali
**Submission:** Milestone 1 – Project Proposal (7th October, 2026)

---

## Project Summary

Honeybees are essential for agriculture, but monitoring hive health in
Pakistan is still mostly manual. Beekeepers must open the hive and inspect
frames one by one, which takes time, disturbs the bees, and often detects
problems like mites or a missing queen too late.

Bee Guardian 2.0 is an automatic hive monitoring system. A hive unit
(camera, microphone, temperature/humidity sensor, weight sensor and an
entrance bee-traffic sensor) collects data and uploads it to a server.
Sound, image, sensor and traffic models analyse the data, and a fusion
model combines the results into one easy-to-read health score. The
beekeeper views the score, hive history and alerts in a mobile app.

The project builds on two earlier modules: a published sound-based health
detection module and an image-based module for detecting issues such as
mites and damaged wings. These are integrated and retrained for the new
automatic hardware.

## Objectives

1. Integrate the existing sound-based and image-based modules into one
   pipeline, and build a hive unit that automatically collects data and
   sends it to a server.
2. Design a fusion model that combines sound, image, sensor and traffic
   outputs into one health score, delivered through a mobile app with alerts.
3. Evaluate the complete system on a real hive and submit the results as a
   research paper.

## System Architecture

Hive sensors → On-hive controller (Raspberry Pi) → Wi-Fi upload
(every 15–30 min) → Cloud intelligence layer (sound, image, sensor,
traffic analysis) → Fusion model → Backend server → Mobile app → Beekeeper

## Requirement Provider

| Name | Designation | Organization | Email |
|------|-------------|--------------|-------|
| Dr. Shafiq-ur-Rehman | Assistant Professor, Computer Science | Namal University, Mianwali | shafiq.rehman@namal.edu.pk |

## Tech Stack

| Layer | Tools |
|-------|-------|
| Hive hardware | Low-cost embedded camera and controller board (Raspberry Pi), microphone, temperature/humidity sensor, weight sensor, infrared entrance sensor |
| Connectivity | Wi-Fi / mobile network |
| AI – audio | Python, TensorFlow / Keras (CNN on sound spectrograms) |
| AI – vision | PyTorch, YOLO, OpenCV |
| Fusion | Weighted classifier combining all model outputs |
| Backend | Python (FastAPI), database, push-notification service |
| Mobile app | Flutter (Android) |
| Deployment | Docker, cloud server |
| Support tools | Git/GitHub, Google Colab, data-labelling tool |

## Development Methodology

Step-wise (incremental) development over a 10-month schedule. The
modules (sound integration, image integration, hive unit, backend, fusion
model, mobile app) are built and tested individually, then assembled
in steps, followed by field testing on a live hive.

## Team

| Name | Roll No | Role | Email |
|------|---------|------|-------|
| Huzaira Sultan | NUM-BSCS-2023-07 | Vision & Backend | bscs23f07@namal.edu.pk |
| Aiman Malik | NUM-BSCS-2023-26 | Audio & Hardware | bscs23f26@namal.edu.pk |
| Amara Bibi | NUM-BSCS-2023-14 | Mobile App | bscs23f14@namal.edu.pk |
| Ahmad Ali | NUM-BSCS-2024-02 | Fusion Model | bscs24f02@namal.edu.pk |

## Repository Structure

```
Bee-Guardian-2.0-SE/
├── README.md
├── Milestone-1/        # Project proposal
└── Meeting Minutes/    # Scanned handwritten meeting minutes
```

Each new milestone will be added in its own folder (Milestone-2, etc.).

## Milestone Status

| Milestone | Description | Status |
|-----------|-------------|--------|
| Milestone 1 | Project Proposal | Submitted |

## References

References are listed in the project proposal document
(`Milestone-1/`) in IEEE format, along with the AI tools usage section.

## License / Note

This repository is maintained for the CSC-225 Software Engineering course
at Namal University, Mianwali.
