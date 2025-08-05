# Uni-App Vue3 TypeScript 开发规则

这个目录包含了适用于uni-app + Vue3 + TypeScript开发的Cursor规则集。

## 规则文件说明

### 核心规则 (alwaysApply: true)
- **uni-app-best-practices.mdc**: 最佳实践规则，包含代码风格、项目结构等核心指导

### 技术规则 (按需应用)
- **api.mdc**: uni-app API使用规范，生命周期、TypeScript类型等
- **vue.mdc**: Vue3组件开发规则，组合式API、scoped等
- **typescript.mdc**: TypeScript配置和开发规范
- **scss.mdc**: SCSS样式规则，优先使用uni.scss预定义样式，减少手写代码
- **conditional-compilation.mdc**: 条件编译规则，跨平台兼容性
- **project-structure.mdc**: 项目结构和命名规范
- **uni-ui-components.mdc**: uni-ui组件库使用指南，easycom配置等

## 主要变化

从uni-app x适配到uni-app + Vue3 + TypeScript：

### 删除的文件
- `ucss.mdc` - uni-app x特有的CSS子集规则
- `uts.mdc` - uni-app x特有的UTS语言规则

### 新增的文件
- `typescript.mdc` - TypeScript开发规范
- `scss.mdc` - SCSS开发规范，强制使用uni.scss预定义样式
- `project-structure.mdc` - 项目结构规范
- `uni-ui-components.mdc` - uni-ui组件库使用指南

### 修改的文件
- `api.mdc` - 从UTS API改为uni-app标准API
- `uvue.mdc` → `vue.mdc` - 从uvue组件改为标准Vue组件
- `uni-app-x-best-practices.mdc` → `uni-app-best-practices.mdc` - 适配标准uni-app

### MCP配置
- `mcp.json` - 更新为使用context7工具查询uni-app文档

## 使用方法

1. 将此目录复制到项目的`.cursor/rules/`目录下
2. 确保项目配置了TypeScript和Vue3
3. 安装必要的依赖：`@dcloudio/types`
4. 配置`tsconfig.json`继承`@vue/tsconfig/tsconfig.json`

## 技术栈特性

- **Vue 3**: 组合式API、`<script setup>`语法
- **TypeScript**: 严格类型检查、类型定义
- **uni-app**: 跨平台API、条件编译
- **SCSS**: 强制使用SCSS，优先使用uni.scss预定义样式
- **响应式设计**: rpx单位、flex布局
- **状态管理**: 支持pinia
- **工具链**: HBuilderX或CLI项目

## 🎨 SCSS 开发重点

### 强制要求
1. **只使用SCSS**: 项目中禁用CSS和Less，统一使用SCSS预处理器
2. **优先使用uni.scss**: 充分利用框架预定义的颜色、尺寸、间距变量
3. **减少手写样式**: 优先使用预定义CSS类，如`.uni-flex`、`.uni-center`等
4. **主题一致性**: 通过uni.scss变量定制主题，保持项目整体风格统一

### 核心原则
- `$uni-color-primary` > `#007aff` (使用变量而非硬编码)
- `.uni-flex .uni-center` > 手写flex样式 (使用预定义类)
- `$uni-spacing-row-base` > `10px` (使用间距变量)
- `@import '@/uni.scss'` > 重复定义 (导入全局变量)

## 📋 最终规则文件列表
```
uniapp/rules/
├── uni-app-best-practices.mdc    # 最佳实践 (alwaysApply)
├── api.mdc                       # API使用规范
├── vue.mdc                       # Vue3组件开发
├── typescript.mdc                # TypeScript规范
├── scss.mdc                      # SCSS样式规则
├── conditional-compilation.mdc   # 条件编译
├── project-structure.mdc         # 项目结构
├── uni-ui-components.mdc         # uni-ui组件库
└── README.md                     # 说明文档
```