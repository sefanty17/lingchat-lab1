# 2026 实验一 · 软件工具的使用

软件工程课内实验一提交仓库。

- **姓名**：蔡智豪
- **学号**：302024315025
- **班级**：软工4班
- **任课教师**：董天阳
- **学院**：计算机科学与技术学院
- **提交日期**：2026-10-08

## 一、项目背景与目标

本仓库是《实验一：软件工具的使用》的提交物，目标有三个：

1. **跑通一个真实开源工程**：选用 [LingChat](https://github.com/SlimeBoyOwO/LingChat) 作为示例项目
   （课程允许自行寻找示例代码）。它是一个基于 Tauri 2 的桌面 AI Galgame 引擎，
   Rust 后端 + Vue 3 前端，技术栈跨度大，适合用来练习"克隆 → 装依赖 → 编译 → 运行"的完整流程。
2. **练习 Git 版本控制**：从初始化仓库、分阶段提交到推送远程，理解 `commit / push / pull`。
3. **体验 AI 辅助编程**：使用 DeepSeek Harness 完成"描述需求 → AI 生成代码 → 本地运行验证 → 微调"。

## 二、目录结构

```
.
├── README.md              本文件：项目说明
├── hello_ai.py            最小程序（AI 生成，输出 "Hello, AI 编程！"）
├── docs/
│   └── AI使用记录.md       AI 辅助编程的过程记录（提示词 / 生成结果 / 校验）
└── 实验报告.md             实验报告正文
```

## 三、运行方式

### 3.1 最小程序（无第三方依赖）

需要 Python 3.8+。

```bash
python hello_ai.py
```

预期输出：

```
Hello, AI 编程！
```

### 3.2 示例项目 LingChat

需要 Node.js 20+、pnpm、Rust 工具链（含 Tauri 2 的系统依赖）。

```bash
git clone https://github.com/SlimeBoyOwO/LingChat.git
cd LingChat
pnpm install          # 安装前端依赖
pnpm tauri dev        # 开发模式运行完整桌面应用
pnpm tauri build      # 打包安装程序（产物在 src-tauri/target/release/bundle/）
```

## 四、开源社区与协作说明

- 上游仓库：<https://github.com/SlimeBoyOwO/LingChat>（SlimeBoyOwO/LingChat）
- 本仓库（本次实验提交）：见提交时填写的 GitHub 地址
- 许可证：上游采用 GPL-3.0，本仓库引用其代码仅用于课程实验，未作商业用途
- 协作方式：Issue 提问题/需求，Pull Request 提交改动；本次实验以 fork + 本地分支的方式练习该流程

## 五、实验环境

| 项 | 值 |
| --- | --- |
| 操作系统 | Windows 10/11 x64 |
| 版本控制 | Git 2.54.0.windows.1 |
| 前端 | Node.js + pnpm，Vue 3.5 + Vite + Tailwind CSS 4 |
| 后端 | Rust + Cargo workspace，Tauri 2 |
| AI 编程工具 | DeepSeek Harness |
| 示例项目版本 | LingChat v0.5.2 |
