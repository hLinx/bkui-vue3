## 更新日志

### 0.0.3-beta.1

* **[fix]**:
    - bugfix(tag): 支持尺寸配置

* **[feat]**:
    - feat(tag-input): tooltips 展示被折叠的内容


### 0.0.3-beta.2

* **[feat]**:
    - feat(table): 支持拖拽排序功能


### 0.0.3-beta.3

* **[fix]**:
    - bugfix(tree): selected 默认值错误
    - bugfix(doc): 文档示例代码报错
    - bugfix(tag-input): tag tips 显示问题
    - bugfix(collapse): 配置 list 时组件内部CollapsePanel content类型错误
    - bugfix(infobox): props 类型调整，dialog 渲染逻辑变更
    - bugfix(tab): 兼容tab tips 配置不存在的数据局

### 0.0.3-beta.6

* **[fix]**:
    - bugfix(form): 表单 tooltips 最大宽度为 400，可通过覆盖样式来修改


### 1.0.0

* **[feat]**:
    - 新增业务组件文档
    - 默认支持按需加载（无需额外的 webpack、vite 插件）

### 1.0.1

* **[fix]**:
    - bugfix(sideslider) 修复 before-close 执行两次的问题
    - modal 中 handleBeforeClose 的处理增加对 promise 的判断
