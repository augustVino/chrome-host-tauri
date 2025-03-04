# Chrome Host Manager

一个基于 Tauri + Rust 开发的 Chrome 浏览器多环境管理工具，支持快速切换不同环境的 hosts 配置和代理设置。

## 技术栈

### 前端
- React - 用户界面开发框架
- TypeScript - 类型安全的 JavaScript 超集
- Less - CSS 预处理器
- Vite - 现代前端构建工具

### 后端
- Tauri - 跨平台桌面应用开发框架
- Rust - 系统级编程语言

## 核心功能

### Chrome 环境管理
- 支持创建和管理多个 Chrome 浏览器环境
- 每个环境独立的用户数据目录
- 自动管理 Chrome 进程的启动和关闭
- 环境状态实时同步

### Hosts 配置管理
- 可视化编辑 hosts 配置
- 多环境 hosts 配置独立存储
- JSON 格式保存配置信息
- 支持快速切换不同环境

### 代理服务
- 内置代理服务器
- 支持环境级别的代理配置
- 代理服务器自动启停
- 代理日志实时查看

### 系统托盘
- 系统托盘常驻
- 快速切换环境
- 实时显示环境状态

## 架构设计

项目采用领域驱动设计（DDD）架构，清晰地划分了不同的职责层次：

### 领域层 (Domain)
- 定义核心业务模型（HostEntry、ProxyServer、ChromeInstance）
- 实现领域服务（ChromeService、HostService、ProxyService）
- 定义仓储接口

### 应用层 (Application)
- 编排领域服务
- 处理业务流程
- 事务管理

### 基础设施层 (Infrastructure)
- 文件存储实现
- 日志管理
- 系统托盘实现
- 常量定义

### 接口层 (Interfaces)
- Tauri 命令定义
- 事件处理
- 前端交互

## 项目特点

1. 跨平台支持
   - 支持 Windows、macOS 和 Linux
   - 针对不同操作系统优化

2. 高性能
   - Rust 实现核心功能
   - 异步处理代理服务
   - 高效的文件操作

3. 用户友好
   - 现代化 UI 设计
   - 简洁的操作流程
   - 实时状态反馈

4. 可扩展性
   - 模块化设计
   - 清晰的领域边界
   - 易于添加新功能

## 开发环境要求

- Node.js
- Rust 工具链
- Tauri CLI
- pnpm 包管理器
