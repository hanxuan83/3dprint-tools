# 🖨️ 3D打印工具导航网站 - 部署指南

恭喜你，蟑螂恶霸！你的 3D打印工具导航网站已经准备好了！

---

## 📦 网站文件说明

你已经拥有了以下文件：

```
3dprint-tools/
├── index.html      ← 这就是你的完整网站（无需其他文件）
└── README.md       ← 这个说明文档
```

**特点：**
- ✅ 单个 HTML 文件，包含所有代码（HTML+CSS+JavaScript）
- ✅ 无需服务器，无需数据库
- ✅ 完全免费托管
- ✅ 自动适配手机和电脑

---

## 🚀 方案一：GitHub Pages 部署（推荐）

### 第 1 步：注册 GitHub 账号

1. 访问 https://github.com
2. 点击 "Sign up" 注册账号
3. 记住你的用户名（比如：`qinhaiyang`）

### 第 2 步：创建仓库

1. 登录 GitHub 后，点击右上角的 **+** → **New repository**
2. Repository name 填写：`3dprint-tools`
3. 勾选 **Public**（公开）
4. 点击 **Create repository**

### 第 3 步：上传网站文件

**方法 A：网页直接上传（最简单）**

1. 在新创建的仓库页面，点击 **uploading an existing file**
2. 把 `index.html` 文件拖到上传区域
3. 在下方输入 Commit message：`Initial commit`
4. 点击绿色按钮 **Commit changes**

**方法 B：使用 Git 命令（如果你会 Git）**

```bash
cd 3dprint-tools
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/你的用户名/3dprint-tools.git
git push -u origin main
```

### 第 4 步：开启 Pages 服务

1. 在仓库页面，点击 **Settings**（设置）
2. 左侧菜单找到并点击 **Pages**
3. 在 **Build and deployment** 部分：
   - Source: 选择 **Deploy from a branch**
   - Branch: 选择 **main**，文件夹选择 **/(root)**
4. 点击 **Save**

### 第 5 步：等待部署完成

- 等待约 1-2 分钟
- 刷新 Pages 设置页面，你会看到顶部出现一个链接
- 格式类似：`https://你的用户名.github.io/3dprint-tools/`

**🎉 恭喜！你的网站已经上线了！**

---

## 🌐 方案二：Vercel 部署（备选）

如果 GitHub Pages 访问慢，可以用 Vercel：

### 步骤：

1. 访问 https://vercel.com
2. 用 GitHub 账号登录
3. 点击 **Add New Project**
4. 选择你的 `3dprint-tools` 仓库
5. 点击 **Deploy**
6. 获得域名：`https://3dprint-tools.vercel.app`

---

## 🔗 自定义域名（可选）

如果你想用自己的域名（如 `www.3dprinttools.cn`）：

### 购买域名：
- 阿里云：https://wanwang.aliyun.com/domain
- 腾讯云：https://cloud.tencent.com/product/domain
- 价格：约 60 元/年

### 绑定到 GitHub Pages：

1. 在仓库 Settings → Pages → Custom domain
2. 输入你的域名，点击 Save
3. 按照提示配置 DNS 解析

---

## 📱 网站功能预览

### 1. 实时搜索
- 在搜索框输入关键词，立即过滤工具
- 支持搜索名称和网址

### 2. 智能分类
网站自动将工具分为 5 类：
- 🎨 设计与建模
- 🖼️ 图像处理
- 📷 扫描与重建
- 🔧 工具与实用
- 📚 资源与教程

### 3. 响应式设计
- 电脑：多列网格布局
- 手机：单列卡片布局
- 平板：自适应两列布局

### 4. 快捷操作
- **访问网站**：直接打开工具
- **复制链接**：一键复制到剪贴板

---

## ✏️ 如何添加新工具？

如果以后要添加新的工具网站：

### 方法 1：直接编辑 HTML（推荐）

1. 用记事本或 VS Code 打开 `index.html`
2. 找到这行代码（大约在第 176 行）：
   ```javascript
   const toolsData = [{"folder":"...
   ```
3. 在数组末尾添加新工具，格式如下：
   ```javascript
   {"name":"工具名称","url":"https://工具网址.com"},
   ```
4. 保存文件，重新上传到 GitHub

### 方法 2：告诉我帮你改

直接在对话框跟我说：
> "帮我添加一个新工具：XXX，网址是 https://xxx.com"

我会生成更新后的代码给你。

---

## 🛠️ 常见问题解答

### Q1: 网站打不开怎么办？
- 检查 GitHub Pages 是否已正确开启
- 确认上传的是 `index.html`（不是 `Index.html` 或其他大小写）
- 清除浏览器缓存后重试

### Q2: 修改后多久能更新？
- GitHub Pages 通常 1-2 分钟自动更新
- 如果没更新，强制刷新浏览器（Ctrl+F5）

### Q3: 可以离线使用吗？
- 可以！直接双击 `index.html` 就能在本地浏览器打开
- 但工具链接需要联网才能访问

### Q4: 数据会丢失吗？
- 不会！GitHub 会自动保存所有历史版本
- 随时可以回滚到之前的版本

### Q5: 有人访问我的网站吗？
- GitHub 仓库页面可以看到 Star 和 Fork 数量
- 如需详细统计，可以集成 Google Analytics

---

## 📊 下一步建议

网站上线后，你可以：

1. **分享给朋友**：把链接发给其他 3D打印爱好者
2. **收集反馈**：根据使用情况优化分类和功能
3. **定期更新**：发现好工具就加进来
4. **美化界面**：如果需要更炫酷的设计，随时找我

---

## 🎯 快速开始清单

- [ ] 注册 GitHub 账号
- [ ] 创建名为 `3dprint-tools` 的仓库
- [ ] 上传 `index.html` 文件
- [ ] 在 Settings → Pages 开启服务
- [ ] 等待 1-2 分钟获取访问链接
- [ ] 测试网站功能（搜索、复制链接等）
- [ ] 分享给朋友 🎉

---

## 💡 技术支持

如果在部署过程中遇到任何问题：

1. 截图错误信息
2. 告诉我你卡在哪一步
3. 我会立刻帮你解决！

---

**祝你使用愉快！** 🖨️✨

*Made with ❤️ for 3D Printing Community*
