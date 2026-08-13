# 具身智能 · 基于 VLA 与世界模型

> 系统学习具身智能（感知 → 决策 → 动作执行的物理闭环），
> 核心两支柱 **VLA（视觉-语言-动作）** + **World Model（世界模型）**，
> 逐步复现经典模型（CLIP、Diffusion Policy、OpenVLA、DreamerV3 等）的学习仓库。

📚 配套学习路线文档见 `study_docs/Embodied AI/`。

## 🎯 仓库定位

- **方向**：具身智能「大脑」—— VLA + 世界模型 + 数据引擎闭环
- **目标**：读懂论文 → 复现代码 → 验证结果

## 🗺️ 学习路线总览（精简版）

```
感知(看懂三维世界) → 决策(结合语言指令) → 动作执行(机械臂/轮式/灵巧手)
       ↓                    ↓                    ↓
    VLM/CLIP         强化学习 MDP/PPO      动作生成(动作token)
    ViT               模仿学习
        ↓
   VLA 端到端：Vision → Language → Action
   (RT-2, Diffusion Policy, OpenVLA, π0, Gr00t N1, 3D-VLA)
        ↓
   World Model：预测未来状态/帧 (DreamerV3, Sora, UniSim)
        ↓
   数据引擎闭环：世界模型生成数据 → 训练 VLA → 收集新数据 → 再训练
```

## ✅ 阶段产出清单

| 阶段 | 内容 | 交付物 |
|------|------|--------|
| 0 | Python/数学/Linux | PyTorch MNIST demo |
| 1 | 深度学习 | CIFAR10 分类器 |
| 2 | 视觉与语言 (VLM) | CLIP 图文检索 demo |
| 3 | 强化学习 | Gymnasium 训练 CartPole |
| 4 | VLA + 世界模型 | OpenVLA / DreamerV3 demo |
| 5 | 仿真与闭环 | 仿真机械臂抓取 |
| 6 | 论文复现 | 精读并复现一篇核心论文 |

## 🔧 环境与依赖

- Python 3.8+ · PyTorch 2.x · CUDA 11/12（训练基本需 GPU，单卡 16GB+）
- 框架：gymnasium、openai-clip、Transformers、open3d
- 仿真：Gymnasium/MuJoCo、Isaac Sim/Lab、Sapien、CARLA、nuScenes
- 数据/调度：Data-Juicer + Flyte（数据闭环）

## 🚀 31 天打卡

| 天数 | 内容 |
|------|------|
| 1-3 | 安装 PyTorch，跑通 MNIST |
| 4-7 | 手写实现并可视化梯度下降 |
| 8-14 | 理解 CNN + 训练 CIFAR10 |
| 15-20 | 手写自注意力（Transformer 核心） |
| 21-28 | CLIP 图文对齐 + 读 Diffusion Policy |
| 25-30 | 读 RT-2 + 跑 OpenVLA demo |

## 🐾 进度追踪

- [ ] 跑通 MNIST，理解梯度
- [ ] 完成一个 CNN / Transformer
- [ ] 跑通 CLIP 图文对齐 demo
- [ ] gym 里训练一个 agent
- [ ] 跑 OpenVLA / π0 demo
- [ ] 仿真里完成一次抓取
- [ ] 精读并复现一篇论文（写笔记）

## 📌 环境选型速查

| 平台 | 用途 | 难度 | 适合 |
|------|------|------|------|
| Gymnasium/MuJoCo | RL 经典 | 低 | RL 入门 |
| Isaac Sim/Lab | 机器人操作物理仿真 | 中 | VLA 综合项目 |
| Sapien | 机器人操作科研 | 中 | 论文复现 |
| CARLA | 自动驾驶仿真 | 中 | 驾驶方向 |
| nuScenes | 数据集+评测 | 中 | 驾驶/感知 |
