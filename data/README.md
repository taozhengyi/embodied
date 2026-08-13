# 数据文件夹

结构：
- `./dataset/` -> 实际数据集（通常很大，用软链接指向外部存储，这里 .gitignore）
- `./preprocess/` -> 预处理脚本（图像/点云/动作数据）
- `./utils/` -> 数据加载、变换工具函数
- `./visualize/` -> 相机/点云/动作轨迹可视化脚本

## 常用数据集

- [ ] RLDS (Robot Learning Datasets)
- [ ] BridgeData V2
- [ ] Google Robot Dataset
- [ ] RLBench
