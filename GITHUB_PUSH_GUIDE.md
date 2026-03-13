# GitHub 仓库推送指南

## 知识库状态

✅ 所有文档已创建完成
✅ Git仓库已初始化
✅ 文件已提交到本地仓库

## 快速推送步骤

### 方式一：使用 GitHub CLI (推荐)

```bash
# 1. 登录 GitHub
gh auth login

# 2. 创建仓库
cd /root/.openclaw/workspace/srpg-knowledge-base
gh repo create srpg-knowledge-base \
  --description "Wayen的SRPG战棋游戏设计知识库" \
  --public \
  --source=. \
  --push
```

### 方式二：手动创建并推送

```bash
# 1. 在 GitHub 网站上创建仓库
# 访问: https://github.com/new
# 填写:
#   - Repository name: srpg-knowledge-base
#   - Description: Wayen的SRPG战棋游戏设计知识库
#   - 选择 Public
#   - 不勾选 README (已有)

# 2. 添加远程仓库并推送
cd /root/.openclaw/workspace/srpg-knowledge-base
git remote add origin https://github.com/YOUR_USERNAME/srpg-knowledge-base.git
git branch -M main
git push -u origin main
```

### 方式三：使用 Token 推送

```bash
# 设置远程仓库 (使用 Personal Access Token)
git remote add origin https://YOUR_TOKEN@github.com/YOUR_USERNAME/srpg-knowledge-base.git
git branch -M main
git push -u origin main
```

## 知识库文件清单

```
srpg-knowledge-base/
├── README.md                  # 知识库导航
├── SRPG 核心机制.md          # 网格/回合制/战斗计算
├── 关卡设计方法论.md         # 三维设计框架
├── 战斗系统设计.md           # 职业/兵种/技能系统
├── 养成系统设计.md           # 转职/装备/羁绊
└── 标杆产品分析.md           # 五款标杆产品对比
```

## 预计仓库链接

推送成功后，仓库地址为：
https://github.com/YOUR_USERNAME/srpg-knowledge-base

## 可选：设置 GitHub Pages

如需在线预览，可在仓库设置中启用 GitHub Pages：
1. 进入仓库 Settings → Pages
2. Source 选择 "Deploy from a branch"
3. Branch 选择 "main"，文件夹选择 "/ (root)"
4. 访问: https://YOUR_USERNAME.github.io/srpg-knowledge-base/
