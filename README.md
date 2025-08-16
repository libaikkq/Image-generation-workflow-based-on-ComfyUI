# ComfyUI-Text2Image-JSON

## 项目简介
本项目基于 **ComfyUI**（可视化 Stable Diffusion 流程构建器），实现从文本提示生成图像的完整流程，并将每次生成的关键信息导出为 JSON 文件，便于后续分析、批量处理或结果复现。适合希望把模型推理结果作结构化存储与管理的场景）。

## 功能
- 使用 ComfyUI Flow 生成高质量图像
- 自动保存生成图片（可配置保存目录和命名规则）
- 将每次生成的元数据导出为 JSON（包含 prompt、seed、模型信息、生成参数、图片路径、时间戳等）
- 支持批量生成与脚本化调用（示例命令）

## 演示截图
-这些眼睛生成的比较正常，后续有些可能是参数调整有问题，显示模糊抽象
<img width="1024" height="1024" alt="ComfyUI_00050_" src="https://github.com/user-attachments/assets/e375d423-fb4d-46bb-afcf-ebb1cfbc0039" />
<img width="1024" height="1024" alt="ComfyUI_00075_" src="https://github.com/user-attachments/assets/8c34cd98-fbae-4a5e-929b-264eec30538d" />
<img width="1024" height="1024" alt="ComfyUI_00096_" src="https://github.com/user-attachments/assets/35294c32-c28a-48e1-890a-a186c6b25526" />
<img width="1024" height="1024" alt="ComfyUI_00053_" src="https://github.com/user-attachments/assets/cccf7ae9-cd5c-4dfa-afd3-3f042299a434" />
<img width="1024" height="1024" alt="2loras_test__00011_" src="https://github.com/user-attachments/assets/290b47db-b744-4480-bc37-c90b4145e769" />

-这部分减少了步数，显示效果类似于了油画
<img width="1024" height="1024" alt="ComfyUI_00358_" src="https://github.com/user-attachments/assets/f557e051-9fb2-4656-bcda-5d056fb51807" />
<img width="1024" height="1024" alt="ComfyUI_00343_" src="https://github.com/user-attachments/assets/260f1a9a-044d-4c74-9404-7739f7f5979e" />
<img width="1024" height="1024" alt="ComfyUI_00355_" src="https://github.com/user-attachments/assets/bce0bb81-7ca8-4c37-9606-a8456ee9efb4" />
<img width="1024" height="1024" alt="ComfyUI_00346_" src="https://github.com/user-attachments/assets/6c5f2685-e183-46cc-a656-583f214aafc8" />
<img width="1024" height="1024" alt="ComfyUI_00353_" src="https://github.com/user-attachments/assets/53d085db-fe6f-41ba-889d-0512128d695d" />
<img width="1024" height="1024" alt="ComfyUI_00354_" src="https://github.com/user-attachments/assets/8738491c-3126-4d8f-b909-fe080ef357cc" />
<img width="1024" height="1024" alt="ComfyUI_00331_" src="https://github.com/user-attachments/assets/cf8e66d7-3774-4fe1-86a3-9f9cf256c889" />
<img width="1024" height="1024" alt="ComfyUI_00330_" src="https://github.com/user-attachments/assets/14e06618-fa8a-4a6e-b0f8-61935ffb1954" />


## 快速开始

### 前提
- 已安装 Python（建议 3.10+）和 Git
- 一台能运行 Stable Diffusion 的机器（有 GPU 更佳）
- 已安装并能运行 ComfyUI（请参照 ComfyUI 官方仓库的安装说明）

### 提示词
```bash
#正向提示词
Zynthr4, 1girl, solo, short hair, messy hair, pretty, thin, earrings, jewelry, dark theme, bangs, realistic flowing colors, full body image, black tattoo, full arm tattoo, wearing frilly black velvet, arrogant expression, strong black light and shadows, evening gown, shadows, studio
#反向提示词
compression artifacts, bad artwork, worst quality, low quality, plastic, imperfect eyes, fake, bad limbs, conjoined, featureless, bad features, incorrect objects, watermark, logo, blurry eyes, blurry irises, bad hands, imperfect hands, half-closed eyes, squinting, close-up, twins, two girls, long neck, naked body

