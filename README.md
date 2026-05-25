

## 一、项目概述

### Mark 格式规范
```
[EM_XXXX-MarkNumber-功能描述-序号/总数-YYYYMMDD-start-]
[EM_XXXX-MarkNumber-功能描述-序号/总数-YYYYMMDD-end-]
[EM_XXXX-MarkNumber-功能描述-序号/总数-YYYYMMDD-start-end-]  ← 单行合并
```

字段说明：
| 字段 | 说明 | 示例 |
|------|------|------|
| XXXX | 开发者代号 | `Derek` |
| MarkNumber | 变更编号 | `M001` |
| 功能描述 | 改动说明 | `SetupPage` |
| 序号/总数 | 第几对/共几对 | `1/3` |
| YYYYMMDD | 日期（可选） | `20260521` |
| 类型 | start / end / start-end | `start` |


## 三、功能清单

### 3.1 高亮功能
- 同一 MarkNumber 的 mark 使用相同颜色
- 不同变更组循环使用颜色调色板（可在设置中自定义）
- `start` 行：左边框 + `▶` 标签
- `end` 行：左边框 + `◀ end` 标签
- `start-end` 单行：左边框 + `◆` 标签
- 区间内容：淡色背景阴影
- 概览滚动条标记

### 3.2 导航命令

| 快捷键 | 命令 | 说明 |
|--------|------|------|
| `Ctrl+Alt+]` | 下一个 Mark | 按行号跳转 |
| `Ctrl+Alt+[` | 上一个 Mark | 按行号跳转 |
| `Ctrl+Alt+P` | 跳转配对 | 从 start 跳到对应 end，反之亦然 |
| `Ctrl+Alt+N` | 重新编号（当前文件） | 自动计算序号/总数 |
| `Ctrl+Shift+Alt+N` | 重新编号（整个工作区） | 跨文件统一编号 |
| `Ctrl+Shift+Alt+R` | 生成 Registry 文档 | 输出 `EM_MARK_REGISTRY.md` |
| //[ | 快捷注释 |
| //# | 快捷注释 |

### 3.3 状态栏
- 显示当前文件的组数和配对数
- 点击状态栏打开 Quick Pick 列表

### 3.4 Quick Pick 列表
- 列出当前文件所有 mark pair
- 支持模糊搜索
- 点击跳转到对应行
<img width="932" height="186" alt="image" src="https://github.com/user-attachments/assets/efe06ebd-1ccb-4770-8aa2-d48e24fbcaf5" />

<img width="1572" height="734" alt="image" src="https://github.com/user-attachments/assets/2dbb5d6e-a722-44d9-915e-dab760627626" />
