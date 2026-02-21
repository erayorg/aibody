# aibody 🧍‍♂️🤖

<p align="center">
  <img src="https://github.com/fluidicon.png" alt="aibody" width="200">
</p>

<p align="center">
  <strong>开源 AI 身体感知与数字孪生框架</strong><br>
  <strong>Open-Source AI Body Perception & Digital Twin Framework</strong>
</p>

<p align="center">
  <a href="https://github.com/erayorg/aibody/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License">
  </a>
  <a href="https://python.org">
    <img src="https://img.shields.io/badge/Python-3.8+-green.svg" alt="Python">
  </a>
  <a href="https://pytorch.org">
    <img src="https://img.shields.io/badge/PyTorch-1.10+-red.svg" alt="PyTorch">
  </a>
  <a href="https://github.com/erayorg/aibody/stargazers">
    <img src="https://img.shields.io/github/stars/erayorg/aibody?style=social" alt="Stars">
  </a>
</p>

---

## 🌍 语言 / Languages
- [English](./README.md)
- [中文](#中文版本)

---

## 中文版本

### 📖 项目简介

**aibody** 是一个面向未来的开源 AI 身体感知框架，旨在将计算机视觉技术与人体科学深度融合。无论是构建智能健身应用、开发医疗康复系统，还是创造沉浸式 VR 体验，aibody 都能为你提供强大的身体数据感知能力。

我们相信，每个人的身体都值得被数字化理解。通过 aibody，你可以轻松构建属于自己的**数字孪生身体**。

### ✨ 核心特性

| 功能模块 | 描述 | 状态 |
|---------|------|------|
| **姿态估计引擎** | 支持 2D/3D 实时关键点检测，精度达 95%+ | ✅ 可用 |
| **动作识别系统** | 自定义动作分类，支持异常姿态预警 | ✅ 可用 |
| **生理数据融合** | 整合可穿戴设备数据（心率、血氧等） | 🚧 开发中 |
| **数字孪生生成** | 构建个性化虚拟身体模型 | 🚧 开发中 |
| **云端同步服务** | 实时数据上云与多端同步 | 📅 规划中 |

### 🚀 快速开始

#### 环境要求
- Python 3.8+
- CUDA 11.0+ (推荐，用于 GPU 加速)
- Webcam 或视频文件

#### 安装

```bash
# 克隆仓库
git clone https://github.com/erayorg/aibody.git
cd aibody

# 创建虚拟环境
python -m venv venv
source venv/bin/activate  # Linux/Mac
# 或 venv\Scripts\activate  # Windows

# 安装依赖
pip install -r requirements.txt

# 下载预训练模型
python scripts/download_models.py
```

运行示例

```bash
# 启动实时姿态检测
python examples/pose_estimation.py --source 0  # 0 为默认摄像头

# 运行 Web 界面
python -m aibody.web.app
# 访问 http://localhost:8000
```

📁 项目结构

```
aibody/
├── aibody/                 # 核心库
│   ├── core/               # 姿态估计核心
│   ├── models/             # 预训练模型
│   ├── fusion/             # 多模态数据融合
│   └── digital_twin/       # 数字孪生模块
├── examples/               # 示例代码
├── web/                    # Web 服务与前端
├── docs/                   # 文档
├── tests/                  # 测试用例
└── scripts/                # 工具脚本
```

🛠️ 技术架构

```
┌─────────────────────────────────────┐
│           应用层 (Applications)        │
│  ┌─────────┐ ┌─────────┐ ┌────────┐ │
│  │ 健身APP │ │ 医疗系统 │ │ VR游戏 │ │
│  └────┬────┘ └────┬────┘ └───┬────┘ │
└───────┼───────────┼──────────┼───────┘
        │           │          │
┌───────┴───────────┴──────────┴───────┐
│         API 层 (FastAPI)              │
└─────────────────┬───────────────────┘
                  │
┌─────────────────┴───────────────────┐
│         核心引擎层 (Core Engine)       │
│  ┌──────────┐ ┌──────────┐ ┌────────┐ │
│  │ 姿态估计 │ │ 动作识别 │ │ 数据融合│ │
│  │ (MediaPipe│ │ (LSTM)  │ │ (Kalman)│ │
│  │ /YOLOv8) │ │         │ │ Filter)│ │
│  └──────────┘ └──────────┘ └────────┘ │
└───────────────────────────────────────┘
                  │
┌─────────────────┴───────────────────┐
│         数据层 (Data Layer)            │
│  ┌──────────┐ ┌──────────┐ ┌────────┐ │
│  │ 视频流   │ │ 传感器   │ │ 云端   │ │
│  │ (OpenCV) │ │ (BLE)   │ │ (AWS)  │ │
│  └──────────┘ └──────────┘ └────────┘ │
└───────────────────────────────────────┘
```

🤝 贡献指南

我们欢迎各种形式的贡献！

特别需要：
- 🐛 Bug 报告与修复
- 📖 文档翻译与改进
- 🧠 新模型集成（姿态估计、动作识别）
- 🎨 UI/UX 设计
- 🌍 多语言支持

📜 许可证

本项目采用 [MIT 许可证](LICENSE) 开源。

🙏 致谢

- [MediaPipe](https://mediapipe.dev) 提供强大的姿态估计基础
- [PyTorch](https://pytorch.org) 深度学习框架
- 所有贡献者与社区支持者
