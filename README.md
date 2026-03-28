# SJTU Canvas 课程助手

一个 [OpenClaw](https://github.com/openclaw/openclaw) / [ClawHub](https://clawhub.com) 技能，用于管理上海交通大学 Canvas LMS 课程数据。

也适用于其他基于 Canvas LMS 的高校，修改 `base_url` 即可。

## 功能

- 📂 查看/下载/批量下载课程文件（PPT/PDF/DOCX）
- 📝 查看作业列表、DDL、提交状态
- ⏰ 同步 DDL 到 Apple 日历（macOS + iCloud → iPhone）
- 🧠 课件内容提取（PPT/PDF → Markdown），配合 AI 总结
- 📊 查看成绩、计算均分
- 💬 课程讨论区摘要
- 🚀 一键提交作业
- 📦 期末复习包生成

## 安装

### 通过 ClawHub

```bash
clawhub install sjtu-canvas
```

### 手动安装

```bash
cd ~/.openclaw/workspace/skills
git clone https://github.com/xiehaohui/sjtu-canvas.git sjtu-canvas
```

## 配置

1. 复制配置模板：

```bash
cp config.example.json config.json
```

2. 获取 Canvas API Token：
   - 登录 Canvas → 设置 → 新建访问令牌
   - 将 token 填入 `config.json`

3. 安装 Python 依赖：

```bash
pip3 install python-pptx pdfplumber requests
```

## 使用

安装配置完成后，在 OpenClaw 对话中直接说：

- "看一下最近有哪些 DDL"
- "下载传热学的课件"
- "帮我总结这个 PPT"
- "查看成绩"
- "同步 DDL 到日历"

## 兼容性

- 默认配置为 SJTU Canvas (oc.sjtu.edu.cn)
- 修改 `config.json` 中的 `base_url` 可适配任何 Canvas LMS 实例
- Apple 日历同步功能仅支持 macOS

## License

MIT
