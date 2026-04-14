# CartPole-PPO-RSL-RL
Lightweight complete reinforcement learning project for CartPole balance control based on **RSL-RL** and **PPO** algorithm.

## Overview
This project implements a full training pipeline for the classic CartPole-v1 task. It wraps the Gymnasium environment to fit RSL-RL interface, trains an Actor-Critic policy with PPO, and provides real-time visualization, model saving and offline inference demo.

## Features
- Custom environment wrapper adapted for RSL-RL
- Stable PPO reinforcement learning training
- Real-time plotting: reward, episode length, loss and action distribution
- Auto save trained model weights (`.pth`)
- Rendered simulation demo for policy validation

## Requirements
```
python>=3.10
torch
gymnasium
matplotlib
numpy
tensordict
```

## Quick Start
```bash
python daolibai.py
```

## Workflow
1. Initialize CartPole environment and neural networks
2. Collect environment interaction data
3. Optimize policy and value network via PPO
4. Visualize training metrics in real time
5. Save model and run rendered demonstration

## Result
The agent rapidly converges and masters stable pole balancing, reaching the maximum score of 500 steps. The saved model can be reused for independent testing and deployment.

<img width="302" height="222" alt="image" src="https://github.com/user-attachments/assets/b71ba1e4-c102-4bdc-b7ce-36f5aa92309c" />
