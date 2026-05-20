# Claude Code 自我介绍

## 基本信息

- **名称**: Claude Code (Anthropic 官方 CLI 工具)
- **运行环境**: VSCode 原生扩展环境
- **当前模型**: deepseek-v4-pro
- **平台**: Windows 10 Enterprise (PowerShell 5.1)
- **会话日期**: 2026-05-19

## 模型家族

Claude 模型系列最新版本：
- **Opus 4.7** (`claude-opus-4-7`) — 最强推理能力，适合复杂任务
- **Sonnet 4.6** (`claude-sonnet-4-6`) — 平衡性能与速度
- **Haiku 4.5** (`claude-haiku-4-5-20251001`) — 最快响应，适合简单任务

支持通过 Agent 工具使用不同模型进行子任务处理。

## 核心功能

### 文件操作
- 读取、编辑、创建任意类型的文件
- 基于 glob 模式匹配和正则表达式的文件搜索（Grep）
- 精确的字符串替换编辑，支持单次/全部替换
- Jupyter Notebook (.ipynb) 的单元格级编辑

### 代码分析与探索
- 多文件代码搜索与符号定位
- 上下文感知的代码审查
- 架构分析与实现方案设计（Plan 模式）
- 专门的代码探索 Agent 可进行大规模代码库研究

### 终端操作
- 通过 PowerShell 执行系统命令
- 支持后台任务运行
- Git 操作（提交、分支管理、查看日志等）
- 包管理（npm、pip 等）

### Web 能力
- Web 搜索获取最新信息
- Web 页面内容抓取与分析

### 任务管理
- Todo 列表跟踪复杂多步骤任务
- 后台并行任务执行
- 定时任务调度（CronCreate / ScheduleWakeup）
- 循环任务（/loop 命令）

### 智能协作
- **Plan 模式**: 先设计方案，经用户确认后再实施
- **Agent 子代理**: 委托复杂任务给专门的工作代理
  - `claude-code-guide`: Claude Code 使用帮助
  - `Explore`: 快速只读代码搜索
  - `Plan`: 软件架构设计
  - `general-purpose`: 通用多步骤任务
  - `statusline-setup`: 状态栏配置
- **Skill 技能系统**: 领域专用的自动化工作流
  - `simplify`: 代码审查与重构
  - `review`: PR 审查
  - `security-review`: 安全审查
  - `init`: 项目初始化与 CLAUDE.md 文档生成
  - `claude-api`: Claude API / Anthropic SDK 应用开发
  - 等等...

### 安全特性
- 沙盒化命令执行
- 权限分级管理（allow/ask/deny）
- 危险操作需用户确认

### 持久化
- 记忆系统：跨会话保存用户偏好、项目信息、反馈等
- 设置文件：项目级和用户级配置
- 定时任务可持久化到磁盘

## 限制说明

- 无网络访问时无法使用 Web 搜索/抓取
- 仅支持读取，不能直接操作 GUI
- 命令执行基于 PowerShell 5.1 语法
- 文件路径需使用绝对路径