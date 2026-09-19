<h2 align="center">我的 WezTerm 配置</h2>

<p align="center">
  <a href="README.md">English</a> | <a href="README.zh-CN.md">简体中文</a>
</p>

![screenshot](./.github/screenshots/demo-2.gif)

---

> 基于 [KevinSilvester/wezterm-config](https://github.com/KevinSilvester/wezterm-config) 的个性化定制分支（`custom` 分支）。

### 定制内容

- 无标题栏（`window_decorations = 'RESIZE'`）+ 亚克力毛玻璃 + 95% 透明度
- 默认 shell：Git Bash（`bash.exe -l`），启动目录 `D:\code`
- 字体：JetBrainsMono Nerd Font + 中文/emoji 回退（Microsoft YaHei / Segoe UI Emoji）
- 接入 [resurrect.wezterm](https://github.com/StephenGemin/resurrect.wezterm) 会话保存/恢复（5 分钟自动保存、失焦即存）
- 补充键位：Ctrl+V 粘贴、Shift+Enter、标签跳转/移动等

---

### 快捷键

大部分键位围绕 <kbd>SUPER</kbd> 和 <kbd>SUPER_REV</kbd>（反向组合键）：

- **Windows/Linux**：<kbd>SUPER</kbd> ⇨ <kbd>Alt</kbd>，<kbd>SUPER_REV</kbd> ⇨ <kbd>Alt</kbd>+<kbd>Ctrl</kbd>
- **MacOS**：<kbd>SUPER</kbd> ⇨ <kbd>Super</kbd>，<kbd>SUPER_REV</kbd> ⇨ <kbd>Super</kbd>+<kbd>Ctrl</kbd>
- 全平台：<kbd>LEADER</kbd> ⇨ <kbd>SUPER_REV</kbd>+<kbd>Space</kbd>

#### 常用/杂项

| 按键 | 功能 |
| --------------------------------- | ------------ |
| <kbd>F1</kbd> | 复制模式 |
| <kbd>F2</kbd> | 命令面板 |
| <kbd>F3</kbd> | 启动器 |
| <kbd>F4</kbd> | 启动器（仅标签） |
| <kbd>F5</kbd> | 启动器（仅工作区） |
| <kbd>F11</kbd> | 全屏切换 |
| <kbd>F12</kbd> | 调试控制台 |
| <kbd>SUPER</kbd>+<kbd>f</kbd> | 搜索文本 |
| <kbd>SUPER_REV</kbd>+<kbd>u</kbd> | 打开 URL |

&nbsp;

#### 复制粘贴

| 按键 | 功能 |
| --------------------------------------------- | -------------------- |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>c</kbd> | 复制 |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>v</kbd> | 粘贴 |
| <kbd>Ctrl</kbd>+<kbd>v</kbd> | 粘贴 |
| <kbd>Shift</kbd>+<kbd>Enter</kbd> | 发送 `ESC+CR`（Claude Code 等 TUI 中为插入换行） |

&nbsp;

#### 会话（resurrect.wezterm）

| 按键 | 功能 |
| --------------------------------------------- | ---------------------------- |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>s</kbd> | 保存工作区状态 |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>S</kbd> | 保存窗口状态 |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>T</kbd> | 保存标签状态 |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>r</kbd> | 模糊搜索并恢复 |
| <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>x</kbd> | 模糊搜索并删除 |

> 每 5 分钟自动保存一次，窗口失焦时也会立即保存。恢复内容包括布局和工作目录；
> 只有白名单内的前台程序（`herdr`）会随恢复自动重启。

&nbsp;

#### 光标移动

| 按键 | 功能 |
| -------------------------------------- | ------------------------------------------------------------ |
| <kbd>SUPER</kbd>+<kbd>←</kbd> | 光标移到行首 |
| <kbd>SUPER</kbd>+<kbd>→</kbd> | 光标移到行尾 |
| <kbd>SUPER</kbd>+<kbd>Backspace</kbd> | 清空当前行（PowerShell/cmd 下无效） |

&nbsp;

#### 标签页

##### 新建/关闭

| 按键 | 功能 |
| --------------------------------- | ------------------------------------- |
| <kbd>SUPER</kbd>+<kbd>t</kbd> | 新建标签（默认域） |
| <kbd>SUPER_REV</kbd>+<kbd>t</kbd> | 新建标签（WSL:Ubuntu） |
| <kbd>SUPER_REV</kbd>+<kbd>w</kbd> | 关闭当前标签 |

##### 切换/移动

| 按键 | 功能 |
| --------------------------------- | -------------- |
| <kbd>SUPER</kbd>+<kbd>[</kbd> | 上一个标签 |
| <kbd>SUPER</kbd>+<kbd>]</kbd> | 下一个标签 |
| <kbd>SUPER_REV</kbd>+<kbd>[</kbd> | 左移标签 |
| <kbd>SUPER_REV</kbd>+<kbd>]</kbd> | 右移标签 |
| <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>1..8</kbd> | 跳转到第 N 个标签 |
| <kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>{</kbd> | 左移标签 |
| <kbd>Shift</kbd>+<kbd>Alt</kbd>+<kbd>}</kbd> | 右移标签 |

##### 显隐/重命名

| 按键 | 功能 |
| ----------------------------- | -------------- |
| <kbd>SUPER</kbd>+<kbd>9</kbd> | 显隐标签栏 |
| <kbd>SUPER</kbd>+<kbd>0</kbd> | 重命名当前标签 |
| <kbd>SUPER_REV</kbd>+<kbd>0</kbd> | 撤销重命名 |

&nbsp;

#### 窗口

| 按键 | 功能 |
| ----------------------------- | ------------------------------------------------------------------ |
| <kbd>SUPER</kbd>+<kbd>n</kbd> | 新建窗口 |
| <kbd>SUPER_REV</kbd>+<kbd>Enter</kbd> | 最大化/还原窗口 |
| <kbd>SUPER</kbd>+<kbd>=</kbd> | 放大窗口（Windows 下因 bug 禁用） |
| <kbd>SUPER</kbd>+<kbd>-</kbd> | 缩小窗口（Windows 下因 bug 禁用） |

&nbsp;

#### 分屏

##### 新建分屏

| 按键 | 功能 |
| ---------------------------------- | ------------------------------------------------ |
| <kbd>SUPER</kbd>+<kbd>\\</kbd> | 垂直分屏（上下） |
| <kbd>SUPER_REV</kbd>+<kbd>\\</kbd> | 水平分屏（左右） |

##### 缩放/关闭

| 按键 | 功能 |
| --------------------------------- | --------------------- |
| <kbd>SUPER</kbd>+<kbd>Enter</kbd> | 当前分屏最大化切换 |
| <kbd>SUPER</kbd>+<kbd>w</kbd> | 关闭当前分屏 |

##### 切换

| 按键 | 功能 |
| --------------------------------- | ----------------------- |
| <kbd>SUPER_REV</kbd>+<kbd>k</kbd> | 切到上方分屏 |
| <kbd>SUPER_REV</kbd>+<kbd>j</kbd> | 切到下方分屏 |
| <kbd>SUPER_REV</kbd>+<kbd>h</kbd> | 切到左侧分屏 |
| <kbd>SUPER_REV</kbd>+<kbd>l</kbd> | 切到右侧分屏 |
| <kbd>SUPER_REV</kbd>+<kbd>p</kbd> | 与所选分屏交换位置 |

##### 滚动

| 按键 | 功能 |
| ----------------------------- | ------------------------------------ |
| <kbd>SUPER</kbd>+<kbd>u</kbd> | 上滚 5 行 |
| <kbd>SUPER</kbd>+<kbd>d</kbd> | 下滚 5 行 |
| <kbd>PageUp</kbd> | 上翻一页 |
| <kbd>PageDown</kbd> | 下翻一页 |

&nbsp;

#### 背景图片

| 按键 | 功能 |
| --------------------------------- | ---------------------------- |
| <kbd>SUPER</kbd>+<kbd>/</kbd> | 随机换图 |
| <kbd>SUPER</kbd>+<kbd>,</kbd> | 下一张 |
| <kbd>SUPER</kbd>+<kbd>.</kbd> | 上一张 |
| <kbd>SUPER_REV</kbd>+<kbd>/</kbd> | 模糊选图 |
| <kbd>SUPER</kbd>+<kbd>b</kbd> | 背景专注模式开关 |

&nbsp;

#### 键位表（Key Tables）

> 见：<https://wezfurlong.org/wezterm/config/key-tables.html>

| 按键 | 功能 |
| ------------------------------ | ------------- |
| <kbd>LEADER</kbd>+<kbd>f</kbd> | 调整字号模式 |
| <kbd>LEADER</kbd>+<kbd>p</kbd> | 调整分屏模式 |

##### 调整字号（`resize_font`）

| 按键 | 功能 |
| -------------- | ------------------------------- |
| <kbd>k</kbd> | 增大字号 |
| <kbd>j</kbd> | 减小字号 |
| <kbd>r</kbd> | 重置字号 |
| <kbd>q</kbd>/<kbd>Esc</kbd> | 退出 |

##### 调整分屏（`resize_pane`）

| 按键 | 功能 |
| -------------- | ---------------------------------------------- |
| <kbd>k</kbd> | 向上扩大 |
| <kbd>j</kbd> | 向下扩大 |
| <kbd>h</kbd> | 向左扩大 |
| <kbd>l</kbd> | 向右扩大 |
| <kbd>q</kbd>/<kbd>Esc</kbd> | 退出 |

---

### 参考/灵感

- 上游仓库：<https://github.com/KevinSilvester/wezterm-config>
- <https://github.com/rxi/lume>
- <https://github.com/catppuccin/wezterm>
- <https://github.com/wez/wezterm/discussions/628#discussioncomment-1874614>
- <https://github.com/wez/wezterm/discussions/628#discussioncomment-5942139>
