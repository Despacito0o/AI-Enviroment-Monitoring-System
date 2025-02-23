# AI-Environment-Monitoring-System

## 项目简介
这是一个结合 AI 和 Arduino 的智能环境监测系统，实时监测温度和湿度，并使用 AI 模型预测未来温度。

## 硬件要求
- Arduino Uno 开发板
- DHT11 温度湿度传感器
- 连接线

## 软件要求
- Arduino IDE
- Python 3.x
- Python 库：`pyserial`、`scikit-learn`、`pandas`、`matplotlib`

## 安装步骤
1. **硬件连接**：
   - 将 DHT11 的信号引脚连接到 Arduino 的数字引脚 2，VCC 接 5V，GND 接 GND。
2. **安装软件**：
   - 下载并安装 Arduino IDE 和 Python 3.x。
   - 在命令行中运行 `pip install pyserial scikit-learn pandas matplotlib` 安装 Python 库。
3. **上传 Arduino 代码**：
   - 将 `TemperatureMonitor.ino` 上传到 Arduino。
4. **运行 Python 脚本**：
   - 修改 `data_analysis.py` 中的串口名称。
   - 运行 `python data_analysis.py`。

## 使用方法
- 运行 Python 脚本后，系统会收集100组数据并预测未来10分钟的温度。
- 数据会保存到 `environment_data.csv`，并显示预测图表。

## 文件说明
- `TemperatureMonitor.ino`：Arduino 代码。
- `data_analysis.py`：Python 数据分析和预测脚本。
- `environment_data.csv`：（可选）采集的环境数据。

## 注意事项
- 确保 Arduino 和 Python 脚本中的串口名称一致。
- 如果数据读取失败，检查传感器连接和库安装。
