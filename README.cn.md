# Fashion Store | 电商原型

## 1. 项目介绍
本项目由 4Geeks Academy AI Engineering 课程的学员协作完成。

项目目标是为一家总部位于法国的服装品牌打造线上商店的视觉原型。

原型应提供现代、一致且响应式的体验，并遵循 Web 开发、SEO、无障碍设计和 Git 协作的最佳实践。

## 2. 项目目标

- 开发电商的五个主要页面。
- 在所有页面中建立一致的视觉形象。
- 确保页面适配手机、平板和桌面设备。
- 使用语义化 HTML 并遵循 SEO 最佳实践。
- 在适当情况下加入 Schema.org 结构化数据。
- 通过 Git、分支和 Pull Request 练习协作开发。
- 使用 Spec-Driven Development（SDD）组织工作。

## 3. 功能范围

### 3.1 首页（`index.html`）

- 包含 Logo、搜索和账户菜单的导航栏。
- 用于展示营销活动和精选商品的 Hero 区域。
- 新品上架区域。
- 热销商品区域。
- 包含商品类别、法律信息和联系方式的页脚。

### 3.2 商品目录（`catalog.html`）

- 使用统一的导航栏和页脚。
- 按类别和尺码筛选。
- 参考网格为 4 列、5 行，共 20 件商品。
- 提供商品详情页链接。

### 3.3 商品详情（`product.html`）

- 商品主图。
- 名称、商品编号和价格。
- 尺码和数量选择。
- 添加到购物车按钮。
- 详细描述、材质和推荐用途。

### 3.4 购物车（`cart.html`）

- 完整的购物车页面。
- 三件示例商品。
- 每件商品的缩略图、价格、数量和小计。
- 显示小计、税费和总价的摘要。
- 前往结账按钮。

### 3.5 结账（`checkout.html`）

付款表单在视觉上分为三个步骤：

1. 个人信息。
2. 配送地址。
3. 银行卡付款信息。

结账流程仅用于演示，不会处理真实付款，也不会存储银行卡信息。

## 4. 技术

| 技术 | 用途 |
| --- | --- |
| HTML5 | 页面结构与内容 |
| Tailwind CSS | 样式与响应式布局 |
| Schema.org | 结构化数据 |
| Git | 版本控制 |
| GitHub | 代码仓库与协作 |
| GitHub Codespaces | 开发环境 |

**限制：**不得使用 React、Vue、Angular、自定义 JavaScript、后端或其他框架。

需要动态逻辑的交互将通过 HTML 进行演示，不得暗示尚未实现的功能。

## 5. 项目结构

```
fashion-store/
├── AGENTS.md
├── CONTEXT.md
├── README.md
├── docs/
│   └── design-system.md
├── memory-bank/
│   ├── decisions.md
│   └── progress.md
├── index.html
├── catalog.html
├── product.html
├── cart.html
├── checkout.html
├── assets/
│   └── images/
└── specs/
    ├── 01-home/
    │   ├── spec.md
    │   ├── plan.md
    │   └── task.md
    ├── 02-catalog/
    ├── 03-product/
    ├── 04-cart/
    └── 05-checkout/
```

Home 目前在 `specs/01-home/` 中包含 `spec.md`、`plan.md` 和 `task.md`。其他页面目录已推迟到后续分支，目前尚无获批的 SDD 文档。

SDD 文档用于定义各个已批准页面的需求、实现方案和可验证任务。

## 6. 开发方法

项目将采用 Spec-Driven Development（SDD）：

1. **背景：**了解项目、范围和限制。
2. **SPEC：**明确需要构建的内容。
3. **PLAN：**确定实现方式。
4. **TASKS：**将工作拆分为可验证的任务。
5. **实现：**开发已批准的任务。
6. **验证：**检查需求、响应式布局、SEO 和无障碍性。

AI 代理必须遵循 `AGENTS.md` 中的说明。

`memory-bank/` 中的 Memory Bank 用于保持不同工作会话之间的信息连续性：`decisions.md` 汇总已批准的决策及其来源，`progress.md` 记录已核实的状态、证据和待办事项。这些摘要不能替代详细规格或计划。

## 7. Git 协作

### 分支策略

- `main`：稳定版本。
- `develop`：集成开发人员的工作。
- `feature/*`：开发单项功能的分支。

示例：

```
feature/home
feature/catalog
feature/product
feature/cart
feature/checkout
```

### 工作流程

1. 同步 `develop` 分支。
2. 创建 `feature/*` 分支。
3. 开发分配的功能。
4. 验证修改。
5. 创建描述清晰的提交。
6. 将分支推送到 GitHub。
7. 创建目标为 `develop` 的 Pull Request。
8. 请另一位开发人员进行审查。
9. 合并已批准的修改。

常规开发期间不得直接修改 `main`。

## 8. 开发规范

- 使用语义化 HTML5。
- 采用 mobile-first 设计方式。
- 一致地使用 Tailwind CSS。
- 使用无障碍标签，并为图片添加替代文本。
- 为每个页面设置合适的标题和元描述。
- 为文件和资源使用清晰的名称。
- 保持导航栏、页脚和页面导航的一致性。
- 避免不必要的依赖。
- 不得包含真实客户信息或银行卡信息。

## 9. 运行项目

项目由静态 HTML 文件组成。

预览方式：

1. 在 GitHub Codespaces 或本地编辑器中打开仓库。
2. 在浏览器中打开 `index.html`，或使用环境中可用的静态服务器提供该目录。
3. 通过页面链接浏览五个页面。

无需后端或构建流程。

## 10. 总体验收标准

- 五个页面均已实现并互相链接。
- 导航栏和页脚的设计保持一致。
- 网站适配手机、平板和桌面设备。
- 使用语义化 HTML。
- 遵循 SEO 和 Schema.org 最佳实践。
- 各页面中的示例商品和价格保持一致。
- 原型符合技术限制。
- 代码通过 Git 和 Pull Request 完成集成与审查。

## 11. 项目状态

**阶段：**Home 页面已在 `home` 分支部分实现。目录、商品详情、购物车和结账页面推迟到后续分支，目前仍为空。

当前 Home 迭代已批准：

- 临时品牌 MAISON NOVA 及共享导航栏/页脚，详见 `docs/design-system.md`。
- 十个编号热销商品占位卡片，预留图片和价格区域。
- 暂不添加新品卡片；该区域显示“即将推出”。

待完成：

- 经批准的 Hero 活动标题、文案和图片；当前文案仅为临时内容。
- 十个热销商品的真实名称、图片、价格和货币。
- 手动检查响应式布局、浏览器渲染、键盘操作和对比度。
- 后续分支中四个页面的规格和实现。
- 两位开发人员之间的职责分配。

## 12. 团队

本项目由两位 4Geeks Academy AI Engineering 课程学员协作完成。

具体职责将在开始实施前确定。
