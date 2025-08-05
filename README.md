# Uni-App AI 开发规则集合

这是一个为uni-app生态系统开发优化的AI编程助手规则集合，支持Cursor、VSCode等IDE，帮助AI生成更准确、规范的uni-app代码。

## 🎯 项目概述

本项目包含两套完整的uni-app开发规则集，针对不同的开发场景进行了专门优化：

### 📁 项目结构

```
uni-app-ai-rules/
├── uniadmin/          # uni-admin后台管理系统规则集
│   ├── mcp.json       # MCP服务配置
│   ├── README.md      # 详细说明文档
│   └── rules/         # 规则文件目录
│       ├── uni-admin-best-practices.mdc   # 核心最佳实践(自动应用)
│       ├── api.mdc                        # API使用规范
│       ├── vue.mdc                        # Vue3组件开发
│       ├── typescript.mdc                 # TypeScript规范
│       ├── scss.mdc                       # SCSS样式规则
│       ├── conditional-compilation.mdc    # 条件编译
│       ├── project-structure.mdc          # 项目结构规范
│       ├── uni-ui-components.mdc          # uni-ui组件库
│       ├── unicloud.mdc                   # uniCloud云开发
│       └── uni-modules.mdc                # uni_modules模块
└── uniapp/            # 标准uni-app应用规则集  
    ├── mcp.json       # MCP服务配置
    ├── README.md      # 详细说明文档
    └── rules/         # 规则文件目录
        ├── uni-app-best-practices.mdc     # 核心最佳实践(自动应用)
        ├── api.mdc                        # API使用规范
        ├── vue.mdc                        # Vue3组件开发
        ├── typescript.mdc                 # TypeScript规范
        ├── scss.mdc                       # SCSS样式规则
        ├── project-structure.mdc          # 项目结构规范
        ├── uni-ui-components.mdc          # uni-ui组件库
        └── unicloud-development.mdc       # uniCloud安全开发
```

## 🚀 快速开始

### 1. 选择合适的规则集

- **开发uni-admin后台管理系统** → 使用 `uniadmin/` 规则集
- **开发标准uni-app应用** → 使用 `uniapp/` 规则集

### 2. 复制到项目目录

将对应的规则目录复制到你的项目根目录：

```bash
# 对于uni-admin项目
cp -r uniadmin/ your-project/.cursor/

# 对于标准uni-app项目  
cp -r uniapp/ your-project/.cursor/
```

### 3. 配置IDE

**Cursor用户**：规则会自动生效

**VSCode用户**：需要手动配置MCP，将`mcp.json`内容添加到VSCode设置中

## ✨ 主要特性

### 🎨 SCSS开发优化
- 强制使用SCSS预处理器，禁用CSS/Less
- 优先使用uni.scss预定义变量和类
- 减少手写样式，提高代码复用性
- 保持主题一致性

### 🔒 uniCloud安全开发
- **uni-admin**: 推荐云对象开发模式，支持完整的云数据库操作
- **uni-app**: 强制安全模式，仅通过admin云对象操作数据库
- 数据访问权限集中管理
- 前后端职责清晰分离

### 📱 跨平台兼容
- Vue3 + TypeScript + 组合式API
- 条件编译规则，确保多平台兼容性
- uni-ui组件库最佳实践
- 响应式设计规范

### 🔧 智能组件检测
- MCP服务自动检测项目中的easycom组件
- AI生成代码时智能使用可用组件
- 减少重复开发，提高代码质量

## 📖 详细文档

- [uni-admin规则集文档](uniadmin/README.md) - 后台管理系统开发规范
- [uni-app规则集文档](uniapp/README.md) - 标准应用开发规范

## 🛠 技术栈支持

- **Vue 3**: 组合式API、`<script setup>`语法
- **TypeScript**: 严格类型检查、完整类型定义
- **uni-app**: 跨平台API、条件编译支持
- **uniCloud**: 云对象、云函数、云数据库
- **uni-ui**: 丰富的组件生态
- **SCSS**: 预处理器 + uni.scss变量系统
- **状态管理**: Pinia支持
- **开发工具**: HBuilderX、CLI工具链

## 🤝 贡献指南

欢迎提交Issue和Pull Request来改进规则集：

1. Fork本项目
2. 创建功能分支 (`git checkout -b feature/new-rule`)
3. 提交更改 (`git commit -am 'Add some rule'`)
4. 推送到分支 (`git push origin feature/new-rule`)
5. 创建Pull Request

## 📄 许可证

本项目采用MIT许可证 - 查看[LICENSE](LICENSE)文件了解详情

---

> 💡 **提示**: 不同类型的uni-app项目请选择对应的规则集，这样能获得最佳的AI编程体验！
