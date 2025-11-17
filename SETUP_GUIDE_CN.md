# 仓库创建清单

## 基本信息

- **仓库名称**: `beamer-academic-template` 或 `academic-beamer-slides`
- **描述**: A clean and professional LaTeX Beamer template for academic presentations with 16:9 aspect ratio
- **主题标签**: `latex`, `beamer`, `presentation`, `academic`, `slides`, `template`, `latex-template`, `beamer-theme`
- **许可证**: MIT License

## 仓库结构

```
beamer-template-repo/
├── README.md                   # 主要文档（包含完整使用说明）
├── QUICKSTART.md              # 快速入门指南
├── CONTRIBUTING.md            # 贡献指南
├── CHANGELOG.md               # 更新日志
├── LICENSE                    # MIT许可证
├── .gitignore                 # Git忽略文件
├── slide_template.tex         # 主模板文件
├── example_presentation.tex   # 完整示例演示文稿
├── algorithm.sty             # 算法环境支持文件
└── figures/                  # 图片目录
    └── README.md             # 图片使用说明
```

## 创建步骤

### 1. 在GitHub上创建新仓库

1. 登录 GitHub
2. 点击右上角 "+" → "New repository"
3. 填写信息：
   - Repository name: `beamer-academic-template`
   - Description: `A clean and professional LaTeX Beamer template for academic presentations`
   - Public (推荐) 或 Private
   - ✅ Initialize with README (如果要在线创建，否则留空)
   - Add .gitignore: 选择 "TeX"
   - Choose a license: MIT License

### 2. 本地初始化并推送

```bash
cd /Users/wangxb/Downloads/RDES_ICML_2025_Final/beamer-template-repo

# 初始化 Git 仓库
git init

# 添加所有文件
git add .

# 首次提交
git commit -m "Initial commit: Academic Beamer presentation template v1.0"

# 连接远程仓库（替换为你的仓库地址）
git remote add origin https://github.com/YOUR_USERNAME/beamer-academic-template.git

# 推送到主分支
git branch -M main
git push -u origin main
```

### 3. 配置仓库设置

在 GitHub 仓库页面：

**About 部分**（右上角 Settings 图标）:
- Website: 可以留空或添加个人网站
- Topics: 添加标签
  - `latex`
  - `beamer`
  - `presentation`
  - `academic`
  - `slides`
  - `template`
  - `latex-template`
  - `beamer-theme`
- Description: 确认描述正确

**Settings → General**:
- ✅ Wikis (可选)
- ✅ Issues (推荐，方便用户反馈)
- ✅ Discussions (可选，用于社区讨论)

**Settings → Pages** (可选，创建项目主页):
- Source: Deploy from a branch
- Branch: main
- Folder: / (root)

## 4. 创建首个 Release

1. 在 GitHub 仓库页面，点击右侧 "Releases"
2. 点击 "Create a new release"
3. 填写信息：
   - Tag version: `v1.0.0`
   - Release title: `v1.0.0 - Initial Release`
   - Description:
     ```markdown
     ## Academic Beamer Template v1.0.0
     
     Initial release of the Academic Beamer Presentation Template.
     
     ### Features
     - Clean 16:9 aspect ratio design
     - Customizable footline
     - Support for mathematics, algorithms, and figures
     - Complete example presentation
     - Comprehensive documentation
     
     ### Files
     - `slide_template.tex` - Main template file
     - `example_presentation.tex` - Working example
     - Full documentation in README.md
     ```
4. 点击 "Publish release"

## 5. 添加 README badges (可选)

在 README.md 开头添加徽章：

```markdown
# Academic Beamer Presentation Template

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![LaTeX](https://img.shields.io/badge/Made%20with-LaTeX-1f425f.svg)](https://www.latex-project.org/)
[![GitHub release](https://img.shields.io/github/release/YOUR_USERNAME/beamer-academic-template.svg)](https://github.com/YOUR_USERNAME/beamer-academic-template/releases/)
[![GitHub stars](https://img.shields.io/github/stars/YOUR_USERNAME/beamer-academic-template.svg)](https://github.com/YOUR_USERNAME/beamer-academic-template/stargazers)
```

## 6. 后续维护

### 定期更新
- 修复用户报告的问题
- 添加新功能
- 更新 CHANGELOG.md
- 创建新的 Release

### 社区互动
- 及时回复 Issues
- 审核 Pull Requests
- 参与 Discussions

### 宣传
- 在相关社区分享（LaTeX、学术论坛等）
- 在论文中使用并注明模板来源
- 鼓励用户 Star 和 Fork

## 文件检查清单

在推送前确认：

- ✅ README.md - 完整详细的文档
- ✅ QUICKSTART.md - 快速入门指南
- ✅ CONTRIBUTING.md - 贡献指南
- ✅ CHANGELOG.md - 版本历史
- ✅ LICENSE - MIT许可证
- ✅ .gitignore - 排除辅助文件
- ✅ slide_template.tex - 主模板
- ✅ example_presentation.tex - 示例文件
- ✅ algorithm.sty - 支持文件
- ✅ figures/ - 图片目录

## 推荐的仓库描述

### 简短描述（GitHub Description）
```
A clean and professional LaTeX Beamer template for academic presentations with 16:9 aspect ratio
```

### 详细描述（README 开头）
```markdown
A modern, clean LaTeX Beamer template designed specifically for academic presentations. 
Features a professional 16:9 layout, customizable footline, and comprehensive support 
for mathematical equations, algorithms, figures, and citations.
```

## 注意事项

1. **不要提交的文件**：
   - *.aux, *.log, *.nav, *.out, *.snm, *.toc 等辅助文件
   - *.pdf 文件（可以在 Release 中提供）
   - .DS_Store 等系统文件

2. **提交信息规范**：
   - 使用清晰的提交信息
   - 格式：`类型: 简短描述`
   - 例如：`feat: Add two-column layout example`
   - 例如：`fix: Correct footline alignment issue`
   - 例如：`docs: Update installation instructions`

3. **版本号规则**（语义化版本）：
   - v1.0.0 - 初始发布
   - v1.1.0 - 添加新功能
   - v1.0.1 - 修复错误
   - v2.0.0 - 重大变更

## 完成！

完成以上步骤后，你的 Beamer 模板仓库就创建好了！🎉

记得在使用模板时，在演示文稿中添加致谢：
```latex
% Template: https://github.com/YOUR_USERNAME/beamer-academic-template
```
