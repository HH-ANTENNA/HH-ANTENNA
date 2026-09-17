<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&duration=3000&pause=1000&color=20C20E&center=true&vCenter=true&width=560&height=45&lines=Hi+there,+I'm+HH-ANTENNA;Computer+Vision+%7C+Deep+Learning;Embedded+AI+%7C+Edge+Deployment" alt="Typing SVG" />

<br/>

**Electronic & Information Engineering @ Shenzhen University**
GPA 3.85 / 4.50 · 2024 – 2028

🎯 **Seeking Internship:** Computer Vision Algorithm / Embedded AI

<a href="https://github.com/HH-ANTENNA">
  <img src="https://img.shields.io/badge/GitHub-Profile-black?style=flat-square&logo=github" />
</a>
<img src="https://img.shields.io/badge/PyTorch-Framework-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/OpenCV-4.8+-5C3EE8?style=flat-square&logo=opencv&logoColor=white" />
<img src="https://img.shields.io/badge/Embedded_AI-MaixCAM-20C20E?style=flat-square" />

</div>

<br />

[中文文档](README_CN.md)

---

### 🏆 Project Spotlight: All-terrain Cooperative Vehicle — Edge AI Perception System

> **Solved the pain point:** Arduino UNO has almost no compute — offloaded the entire vision pipeline to an edge NPU and cut inter-board traffic down to 3 discrete commands.

**🥉 Provincial Third Prize · 2026.08** · **[All-terrain-Cooperative-Vehicle](https://github.com/HH-ANTENNA/All-terrain-Cooperative-Vehicle/tree/main)**

| Layer | Detail |
| :--- | :--- |
| 📷 **Perception** | MaixCAM-Pro · 3-class classifier (triangular prism / cylinder / cube) · ~2.22M params, on-device NPU |
| 🔗 **Communication** | UART with level shifting · edge-compute decoupling, only `0 / 1 / 2` downstream |
| 🧠 **Main Control** | Arduino UNO · state machine + PD line-following + robotic arm |
| 🎯 **Actuation** | Software PWM motor drive · 3-channel tracking · ultrasonic ranging · servo gripper |

**Engineering highlights**

* ⚡ **Edge-compute decoupling** — vision fully offloaded to MaixCAM-Pro; after confidence filtering only 3 discrete commands are sent downstream, minimizing bandwidth and MCU load.
* 🔁 **Sliding-window majority voting** — 10~15 consecutive frames, class mode as the decision; temporal smoothing against vibration and lighting noise.
* 🛡️ **Application-layer redundancy** — each decision repeated 10~20 times to survive occasional UART packet loss; the state machine never stalls.
* 🎚️ **Confidence fallback** — 0.78 rejection threshold; low-confidence results default to triangular prism to guarantee stable output.
* 🧭 **System-level trade-off** — abandoned vision-based localization (resource contention + distortion) for ultrasonic stop-point calibration: engineering delivery over theoretical perfection.

**Stack:** `MaixCAM-Pro` `MaixHub` `PyTorch` `UART` `Arduino UNO` `State Machine`

---

### 🔁 Paper Reproduction: ResiComp — Loss-Resilient Image Compression

> **Solved the pain point:** Reproduce a TCSVT 2026 method from scratch and benchmark its structural robustness against post-hoc redundancy (LDPC).

**TCSVT 2026 · arXiv 2502.10812** · [Official Repo](https://github.com/wsxtyrdd/ResiComp) · [Paper](https://arxiv.org/abs/2502.10812)

* 📚 **Training setup:** Trained the MVTM dual-functional model from scratch on ImageNet val, validated on DIV2K — no official weights loaded, to verify reproducibility.
* 📡 **Evaluation protocol:** 6 real network traces (EP1~EP6) × 3 context modes (ISC / MDC / LC), rate-distortion curves + fine-grained progressive decoding (10%→90% token loss).
* 🎯 **Baseline:** Implemented an LDPC forward-error-correction baseline to compare structural robustness vs. post-hoc redundancy under identical packet-loss rates.
* 📈 **Status:** Training done, experiments in progress — deviation analysis vs. reported PSNR / BD-rate to follow.

**Stack:** `Neural Image Compression` `MVTM` `Swin Transformer` `ImageNet` `DIV2K` `LDPC`

---

### 🌟 Project Spotlight: Handwritten-Digit-Recognition-YOLOv8

> **Solved the pain point:** An out-of-the-box end-to-end handwritten digit recognition tool — no manual MNIST download, real-time drawing interaction, multi-digit continuous recognition, zero deployment hassle.

**[Handwritten-Digit-Recognition-YOLOv8](https://github.com/HH-ANTENNA/Handwritten-Digit-Recognition-YOLOv8)**

* 🚀 **Engineering:** YOLOv8-cls + Otsu adaptive thresholding + vertical projection digit segmentation + Tkinter GUI. One-click training, real-time recognition, confidence visualization.
* 💡 **Value:** Fully packaged CV pipeline — ideal as an entry-level project & interview portfolio piece. GPU/CPU auto-adaptation, zero data prep cost.
* 🛠️ **Stack:** Python 3.8+, PyTorch / Ultralytics YOLOv8, Pillow, NumPy, Tkinter.

---

### 🌟 Project Spotlight: dl-learning-journey

> **Solved the pain point:** Systematic learning of deep learning — from PyTorch basics to CNN / object detection practice, precipitating notes and code.

**[dl-learning-journey](https://github.com/HH-ANTENNA/dl-learning-journey)**

* 🛠 **Engineering:** Organized PyTorch introductory tutorials, model implementations and project cases into a complete computer-vision learning path.
* ⚡ **Value:** Laid a solid foundation for subsequent research / internships, and can be directly used as a technical portfolio.
* 🔧 **Stack:** Python 3.8+, PyTorch 2.0+, OpenCV 4.8+, NumPy.

---

### 📚 Tooling: Claude Paper Assistant

> **Solved the pain point:** The full "read a paper → present a paper" loop is manual and slow.

**[claude-paper-assistant](https://github.com/HH-ANTENNA/claude-paper-assistant)**

* 🤖 Claude Code skill package: auto deep-read PDF → structured Word study notes → academic-style slides with figures cropped straight from the PDF.
* 🛠️ **Stack:** Claude Code, python-pptx, PyMuPDF.

---

### 🛠 Tech Stack

| Core | Frameworks & Tools |
| :--- | :--- |
| ![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&logo=python&logoColor=white) | ![PyTorch](https://img.shields.io/badge/PyTorch-Framework-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![OpenCV](https://img.shields.io/badge/OpenCV-4.8+-5C3EE8?style=flat-square&logo=opencv&logoColor=white) |
| ![Git](https://img.shields.io/badge/Git-VCS-F05032?style=flat-square&logo=git&logoColor=white) | ![VS Code](https://img.shields.io/badge/VS_Code-IDE-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-Data-013243?style=flat-square&logo=numpy&logoColor=white) |
| ![C](https://img.shields.io/badge/C-Programming-00599C?style=flat-square&logo=c&logoColor=white) | ![Arduino](https://img.shields.io/badge/Arduino-Embedded-00979D?style=flat-square&logo=arduino&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-Basics-FCC624?style=flat-square&logo=linux&logoColor=black) |

**Domains:** Image Classification · Object Detection · Self-Supervised Learning (MAE) · Neural Image Compression · Edge AI Deployment

---

### 🔭 About Me

- 🎓 **Background:** Undergraduate in Electronic & Information Engineering @ Shenzhen University. Focused on **Computer Vision, Deep Learning and Embedded AI**.
- 🔬 **Research:** Undergraduate research assistant — SDR-HDR video enhancement (dataset construction · literature survey · code reproduction). Reproduced MAE (CVPR 2022) for a group literature talk.
- 🌱 **Learning:** CNN / object detection, PyTorch model training, edge NPU deployment.
- 💼 **Goal:** Seeking internship in **Computer Vision / AI Application** (available 6 months+).
- 💬 **Motto:** "以眼观世界，以码识万物。(See the world with eyes, understand all things with code.)"
