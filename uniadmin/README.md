# Uni-Admin 后台管理系统开发规则

这个目录包含了适用于uni-admin后台管理系统开发的Cursor规则集，基于uni-app + Vue3 + TypeScript + uniCloud。

## 规则文件说明

### 核心规则 (alwaysApply: true)
- **uni-admin-best-practices.mdc**: uni-admin最佳实践规则，包含后台管理系统开发核心指导

### 技术规则 (按需应用)
- **api.mdc**: uni-app API使用规范，生命周期、TypeScript类型等
- **vue.mdc**: Vue3组件开发规则，组合式API、scoped等
- **typescript.mdc**: TypeScript配置和开发规范
- **scss.mdc**: SCSS样式规则，优先使用uni.scss预定义样式，减少手写代码
- **conditional-compilation.mdc**: 条件编译规则，跨平台兼容性
- **project-structure.mdc**: uni-admin项目结构和命名规范
- **uni-ui-components.mdc**: uni-ui组件库使用指南，专注后台管理系统组件
- **unicloud.mdc**: uniCloud云开发规则，云函数、云数据库等
- **uni-modules.mdc**: uni_modules模块开发和使用规范

## 主要特性

专为uni-admin后台管理系统开发优化：

### 新增的文件
- `unicloud.mdc` - uniCloud云开发规则，优先推荐云对象，云数据库、云存储等
- `uni-modules.mdc` - uni_modules模块开发和使用规范
- `typescript.mdc` - TypeScript开发规范
- `scss.mdc` - SCSS开发规范，强制使用uni.scss预定义样式

### 核心文件
- `uni-admin-best-practices.mdc` - uni-admin专用最佳实践
- `project-structure.mdc` - uni-admin项目结构规范
- `uni-ui-components.mdc` - 专注后台管理系统的uni-ui组件使用

### MCP配置
- `mcp.json` - 集成context7和uni-app-x工具，支持uni-admin文档查询

## 使用方法

1. 将此目录复制到项目的`.cursor/rules/`目录下
2. 确保项目配置了TypeScript和Vue3
3. 安装必要的依赖：`@dcloudio/types`、`@dcloudio/uni-ui`
4. 配置`tsconfig.json`继承`@vue/tsconfig/tsconfig.json`
5. 创建uniCloud服务空间并关联项目
6. 配置pages.json中的easycom规则以支持uni-ui组件自动导入

## 技术栈特性

- **Vue 3**: 组合式API、`<script setup>`语法
- **TypeScript**: 严格类型检查、类型定义
- **uni-app**: 跨平台API、条件编译
- **uniCloud**: 云对象（推荐）、云函数、云数据库、云存储
- **uni-ui**: 丰富的后台管理组件库
- **uni_modules**: 插件生态系统
- **SCSS**: 强制使用SCSS，优先使用uni.scss预定义样式
- **响应式设计**: rpx单位、flex布局
- **状态管理**: 支持pinia
- **工具链**: HBuilderX云端一体化开发

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
uniadmin/rules/
├── uni-admin-best-practices.mdc  # uni-admin最佳实践 (alwaysApply)
├── api.mdc                       # API使用规范
├── vue.mdc                       # Vue3组件开发
├── typescript.mdc                # TypeScript规范
├── scss.mdc                      # SCSS样式规则
├── conditional-compilation.mdc   # 条件编译
├── project-structure.mdc         # uni-admin项目结构
├── uni-ui-components.mdc         # uni-ui后台管理组件库
├── unicloud.mdc                  # uniCloud云开发规则（云对象优先）
├── uni-modules.mdc               # uni_modules模块规范
└── README.md                     # 说明文档
```