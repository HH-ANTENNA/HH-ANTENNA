<div align="center">

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&duration=3000&pause=1000&color=20C20E&center=true&vCenter=true&width=560&height=45&lines=Hi+there,+I'm+HH-ANTENNA;Computer+Vision+%7C+Deep+Learning;Embedded+AI+%7C+Edge+Deployment" alt="Typing SVG" />

<br/>

**深圳大学 · 电子信息工程 · 本科在读**
GPA 3.66 / 4.50 · 2024 – 2028

🎯 **求职意向：** 计算机视觉算法 / 嵌入式 AI 实习

<a href="https://github.com/HH-ANTENNA">
  <img src="https://img.shields.io/badge/GitHub-Profile-black?style=flat-square&logo=github" />
</a>
<img src="https://img.shields.io/badge/PyTorch-Framework-EE4C2C?style=flat-square&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/OpenCV-4.8+-5C3EE8?style=flat-square&logo=opencv&logoColor=white" />
<img src="https://img.shields.io/badge/Embedded_AI-MaixCAM-20C20E?style=flat-square" />

</div>

<br />

[English](README.md)

---

### 🏆 项目精选：全地形协同机器人 — 端侧边缘 AI 感知系统

> **解决了什么：** Arduino UNO 几乎无算力 —— 将视觉任务完全下沉到边缘 NPU，板间通信压缩到 3 个离散指令。

**🥉 省级三等奖 · 2026.08** · **[All-terrain-Cooperative-Vehicle](https://github.com/HH-ANTENNA/All-terrain-Cooperative-Vehicle/tree/main)**

| 层级 | 说明 |
| :--- | :--- |
| 📷 **视觉感知** | MaixCAM-Pro · 三分类模型（三角柱 / 圆柱 / 正方体）· 约 222w 参数量，端侧 NPU 推理 |
| 🔗 **通信层** | UART 串口（带电平转换）· 边缘算力解耦，仅向下位机传 `0 / 1 / 2` |
| 🧠 **主控** | Arduino UNO · 状态机调度 + PD 循迹 + 机械臂 |
| 🎯 **执行** | 软件 PWM 电机驱动 · 三路循迹 · 超声波测距 · 舵机抓取 |

**工程亮点**

* ⚡ **边缘算力解耦** —— 视觉任务完全下沉至 MaixCAM-Pro；置信度过滤后仅向下位机发送 3 个离散指令，大幅降低通信带宽与主控负载。
* 🔁 **多帧滑动窗口多数表决** —— 连续收集 10~15 帧，取类别众数作为决策；针对赛场震动与光线波动做时序平滑去噪。
* 🛡️ **应用层冗余通信** —— 单次决策连续重复发送 10~20 次，应对串口偶发丢包，确保下位机状态机永不卡死。
* 🎚️ **置信度兜底** —— 0.78 拒识阈值；低置信度结果默认归类为三角柱，保证比赛全流程稳定输出。
* 🧭 **系统级方案取舍** —— 放弃视觉定位盒子（资源竞争 + 视觉畸变），改用超声波标定停车点：工程落地优先于理论完美。

**技术栈：** `MaixCAM-Pro` `MaixHub` `PyTorch` `UART` `Arduino UNO` `状态机`

---

### 🔁 论文复现：ResiComp — 损失鲁棒图像压缩

> **解决了什么：** 从零复现 TCSVT 2026 方法，并将其结构内生鲁棒性与事后冗余方案（LDPC）做横向对比。

**TCSVT 2026 · arXiv 2502.10812** · [官方仓库](https://github.com/wsxtyrdd/ResiComp) · [论文](https://arxiv.org/abs/2502.10812)

* 📚 **训练配置：** 从零重训练 MVTM 双功能模型（训练集 ImageNet 验证集 / 验证集 DIV2K），不加载官方权重，验证论文方法的可复现性。
* 📡 **评估协议：** 6 种真实网络 Trace（EP1~EP6）× 3 种上下文模式（ISC / MDC / LC），率失真曲线 + 细粒度渐进解码（10%→90% token 丢失）。
* 🎯 **基线对比：** 额外实现 LDPC 前向纠错基线，在相同丢包率下对比结构内生鲁棒性与事后冗余方案的性能差异。
* 📈 **状态：** 训练完成，实验收集中 —— 复现 PSNR / BD-rate 与论文报告值的偏差分析待补充。

**技术栈：** `神经图像压缩` `MVTM` `Swin Transformer` `ImageNet` `DIV2K` `LDPC`

---

### 🌟 项目精选：Handwritten-Digit-Recognition-YOLOv8

> **解决了什么：** 开箱即用的端到端手写数字识别方案，无需手动准备 MNIST 数据集，支持实时手写交互与多数字连续识别。

**[Handwritten-Digit-Recognition-YOLOv8](https://github.com/HH-ANTENNA/Handwritten-Digit-Recognition-YOLOv8)**

* 🚀 **工程：** 基于 YOLOv8-cls 构建，集成 Otsu 自适应阈值、竖直投影多数字分割与 Tkinter 可视化 GUI，一键训练、实时识别、置信度可视化。
* 💡 **价值：** 封装完整工程化流程，可直接作为 CV 入门项目与面试作品集，GPU/CPU 自适应，零额外数据准备成本。
* 🛠️ **技术栈：** Python 3.8+, PyTorch / Ultralytics YOLOv8, Pillow, NumPy, Tkinter。

---

### 🌟 项目精选：dl-learning-journey

> **解决了什么：** 系统化学习深度学习，从 PyTorch 基础到 CNN / 目标检测实战，沉淀学习笔记与项目代码。

**[dl-learning-journey](https://github.com/HH-ANTENNA/dl-learning-journey)**

* 🛠 **工程：** 梳理 PyTorch 入门教程、模型实现与项目案例，形成完整的计算机视觉学习路径。
* ⚡ **价值：** 为后续科研 / 实习打下扎实基础，可直接用作技术作品集展示。
* 🔧 **技术栈：** Python 3.8+, PyTorch 2.0+, OpenCV 4.8+, NumPy。

---

### 📚 工具链：Claude Paper Assistant

> **解决了什么：** 「读论文 → 讲论文」全流程手工操作，耗时且重复。

**[claude-paper-assistant](https://github.com/HH-ANTENNA/claude-paper-assistant)**

* 🤖 Claude Code 技能包：自动精读 PDF → 生成结构化 Word 学习笔记 → 从 PDF 截取原图生成学术风格汇报 PPT。
* 🛠️ **技术栈：** Claude Code, python-pptx, PyMuPDF。

---

### 🛠 技术栈

| 核心 | 框架与工具 |
| :--- | :--- |
| ![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat-square&logo=python&logoColor=white) | ![PyTorch](https://img.shields.io/badge/PyTorch-Framework-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![OpenCV](https://img.shields.io/badge/OpenCV-4.8+-5C3EE8?style=flat-square&logo=opencv&logoColor=white) |
| ![Git](https://img.shields.io/badge/Git-VCS-F05032?style=flat-square&logo=git&logoColor=white) | ![VS Code](https://img.shields.io/badge/VS_Code-IDE-007ACC?style=flat-square&logo=visual-studio-code&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-Data-013243?style=flat-square&logo=numpy&logoColor=white) |
| ![C](https://img.shields.io/badge/C-Programming-00599C?style=flat-square&logo=c&logoColor=white) | ![Arduino](https://img.shields.io/badge/Arduino-Embedded-00979D?style=flat-square&logo=arduino&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-Basics-FCC624?style=flat-square&logo=linux&logoColor=black) |

**方向：** 图像分类 · 目标检测 · 自监督学习（MAE）· 神经图像压缩 · 边缘 AI 部署

---

### 🔭 关于我

- 🎓 **背景：** 深圳大学 电子信息工程 本科在读，专注 **计算机视觉、深度学习与嵌入式 AI**。
- 🔬 **科研：** 导师课题组本科科研助理 —— SDR-HDR 视频增强（数据集构建 · 文献调研 · 代码复现）；完成 MAE（CVPR 2022）文献汇报。
- 🌱 **学习中：** CNN / 目标检测、PyTorch 模型训练、边缘 NPU 部署。
- 💼 **目标：** 寻找 **计算机视觉 / AI 应用** 方向实习（可实习 6 个月以上）。
- 💬 **座右铭：** "以眼观世界，以码识万物。"
