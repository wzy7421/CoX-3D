CoX-3D – 社交媒体驱动的可解释三维共创系统

CoX-3D 是一个研究型原型系统，融合了 社交媒体需求建模 与 可解释人工智能（XAI），支持从文本、图像和用户评论快速生成三维设计方案。它既能作为 生成式设计实验平台，也能提供直观的 Web 界面，帮助用户在生成—迭代—优化中实现高效共创。

✨ 核心功能

多模态输入: 支持文本提示 + 图像上传 + 社交媒体数据。

三种生成模式: 文本→图像、图像→图像、图文融合。

拓扑优化: 自动网格简化与结构优化，兼顾精度与可制造性。

可解释反馈: Grad-CAM 热力图 + 自动化指标。

一键导出: 输出 .obj/.fbx 模型与设计报告。

🚀 技术栈

前端: React + TailwindCSS

后端: FastAPI (Python) / Node.js

模型: 扩散模型 + YOLOv5s + Grad-CAM

数据源: 微博 API / 用户上传

🔧 快速部署
# 克隆仓库
git clone https://github.com/your-repo/cox-3d.git
cd cox-3d

# 安装依赖
pip install -r requirements.txt

# 设置环境变量
export OPENROUTER_API_KEY=your_key

# 启动服务
uvicorn main:app --reload


访问 http://localhost:8000 打开 Web UI。

📦 API 示例
curl -X POST https://my-cox3d-server.dev/generate/multimodal \
-H "Content-Type: application/json" \
-H "Authorization: Bearer YOUR_API_KEY" \
-d '{
  "prompt": "生成一款具有流线型外观和金属质感的吹风机",
  "images": ["BASE64_IMAGE_DATA"]
}'

🎯 使用场景

研究者：验证“社交数据—生成设计—可解释优化”的闭环。

设计师：缩短建模时间，提升透明度与设计质量。

学生/创作者：低门槛从灵感到原型，支持快速迭代。
