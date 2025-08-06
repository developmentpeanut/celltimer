# celltimer

一个轻量级的 Jupyter / IPython 单元执行计时扩展，可以在每个 Notebook 单元格执行后自动显示耗时。支持自定义颜色与输出文字。
无需依赖旧版本 pandas，完全兼容 Python 3.7+ 和最新版 Jupyter。

---

## 功能特点

- **自动计时**：每次运行单元格后自动打印耗时  
- **轻量无依赖**：只依赖 IPython (>=7.0)  
- **简单易用**：通过 `%load_ext celltimer` 一键开启  
- **自动打印运行时间**（秒数 + timedelta）
- **可修改输出颜色**（支持常用颜色名和 ANSI 转义码）
- **可修改输出文字标签**

---

## 安装

### 从源码安装
下载 `celltimer-0.1.0.zip` 并使用 pip 安装：
```bash
pip install celltimer-0.1.0.zip
```

或github安排：
```bash
git clone https://github.com/developmentpeanut/celltimer.git
cd celltimer
pip install .
```

或从源码安装：
```bash
unzip celltimer-0.1.0.zip
cd celltimer
pip install .
```

## 使用方法

### 1. 加载扩展
```python
%load_ext celltimer
```
加载后，每个单元执行完都会自动打印运行时间。

### 2. 修改颜色
可使用内置颜色：
```python
%celltimer color red
%celltimer color cyan
%celltimer color green
%celltimer color gray
```

也可使用 ANSI 转义码：
```python
%celltimer color \033[38;5;245m   # 自定义灰色
%celltimer color \033[38;5;214m   # 橙色
```

### 3. 修改输出文字
可将默认的“执行时间”替换成任意文字：
```python
%celltimer label 耗时
%celltimer label 运行时间
%celltimer label ExecutionTime
```

### 4. 卸载扩展
若不再需要计时功能：
```python
%unload_ext celltimer
```

```bash
pip uninstall celltimer -y
```

## 输出示例

默认输出：
```
执行时间: 0.123 秒 | 0:00:00.123000
```

修改颜色与文字后：
```
耗时: 1.234 秒 | 0:00:01.234000   （红色）
```

## 功能特性
- 自动为每个单元计时  
- 同时显示秒数与 timedelta 格式  
- 颜色可通过名称或 ANSI 码自定义  
- 输出文字可自定义，支持多语言  
- 无外部依赖，轻量易安装  

## License
MIT License
