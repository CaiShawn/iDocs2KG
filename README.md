# iDocs2KG：文档知识图谱构建系统

将各种文档（PDF、Word、Excel、PPT等）自动转换为结构化的知识图谱，便于知识管理、智能检索与可视化分析。

## 快速开始

### 环境准备
- Python 3.8+
- Node.js 14+
- Neo4j 图数据库（或兼容的图数据库）

### 启动步骤

1. **启动后端**
   ```bash
   cd backend
   pip install -r requirements.txt
   python app.py
   ```

2. **启动前端**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

3. **访问系统**
   - 前端界面：`http://localhost:3000`
   - API 文档：`http://localhost:8000/docs`

## 主要功能

- **文档上传与解析**：支持 PDF、Word、Excel、PPT 等多种格式
- **智能抽取**：自动识别文档中的实体（如人名、组织、术语）和关系
- **图谱构建**：将抽取的知识存入图数据库，构建可查询的知识图谱
- **可视化与检索**：前端界面直观展示图谱，支持交互式查询和探索

## 项目结构

```
iDocs2KG/
├── backend/          # 后端服务（Python + FastAPI/Flask）
├── frontend/         # 前端界面（React/Vue）
├── uploads/          # 用户上传的文件
├── results/          # 处理结果与生成的数据
└── venv/             # Python 虚拟环境
```

## 技术栈

- **后端**：Python、FastAPI/Flask、spaCy/NLTK（NLP）、Neo4j、向量数据库
- **前端**：React/Vue、D3.js/Vis.js（图谱可视化）、Ant Design/Element UI
- **文档解析**：PyPDF2、python-docx、openpyxl 等

## 如何使用？

1. **上传文档**：在前端页面上传一个或多个文档
2. **配置选项**（可选）：调整实体识别、关系提取等设置
3. **开始处理**：系统自动解析内容并构建知识图谱
4. **查看图谱**：在前端界面中交互式查看图谱，可通过节点/关系进行检索
5. **导出结果**：支持导出图谱数据或查询结果

## 部署

### 简单部署（开发）
```bash
# 分别启动后端和前端服务
cd backend && python app.py
cd frontend && npm run dev
```

### Docker 部署（生产）
```bash
docker-compose up -d
```

## 测试

运行测试用例：
```bash
pytest
```

## 贡献

欢迎提交 Issue 或 Pull Request。请先 Fork 项目，并在功能分支上进行开发。

## 许可证

待补充（可选用 MIT、Apache 2.0 等开源协议）

## 联系

如有问题或建议，请通过项目仓库的 Issue 页面联系维护者。

---

**让文档变成知识，让知识连接起来。**
