# ComfyUI-Text2Image-JSON
> 使用 ComfyUI 将文字（Prompt）生成图像，并导出生成结果的 JSON 元数据（包含 prompt、seed、参数与生成图片路径）的演示项目。

## 项目简介
本项目基于 **ComfyUI**（可视化 Stable Diffusion 流程构建器），实现从文本提示生成图像的完整流程，并将每次生成的关键信息导出为 JSON 文件，便于后续分析、批量处理或结果复现。适合希望把模型推理结果作结构化存储与管理的场景（例如数据标注、实验记录、自动化流水线等）。

## 功能
- 使用 ComfyUI Flow 生成高质量图像
- 自动保存生成图片（可配置保存目录和命名规则）
- 将每次生成的元数据导出为 JSON（包含 prompt、seed、模型信息、生成参数、图片路径、时间戳等）
- 支持批量生成与脚本化调用（示例命令）

## 演示截图
（在此处插入几张示例输出图或 GIF）

---

## 快速开始

### 前提
- 已安装 Python（建议 3.10+）和 Git
- 一台能运行 Stable Diffusion 的机器（有 GPU 更佳）
- 已安装并能运行 ComfyUI（请参照 ComfyUI 官方仓库的安装说明）

### 安装（示例）
```bash
# 克隆本仓库
git clone https://github.com/<your-username>/ComfyUI-Text2Image-JSON.git
cd ComfyUI-Text2Image-JSON

# 可选：创建虚拟环境
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate

# 安装依赖（本项目依赖一些用于后处理或 JSON 操作的库）
pip install -r requirements.txt
