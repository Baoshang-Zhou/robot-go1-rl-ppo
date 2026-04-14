CartPole PPO Training with RSL-RL
Overview
This project implements a complete reinforcement learning training pipeline for the classic CartPole-v1 balance task, based on the RSL-RL framework and the PPO (Proximal Policy Optimization) algorithm.
The program integrates environment wrapping, agent training, real-time training visualization, model weight saving, and policy inference demonstration. It enables the intelligent agent to autonomously learn stable balancing control from scratch, monitors training convergence through dynamic charts, and supports permanent model export and offline performance verification.
Key Features
Custom Environment Wrapper: Adapt the original Gymnasium CartPole environment to the RSL-RL VecEnv interface, realizing interactive stepping, automatic reset, reward statistics and state tensor conversion.
PPO Algorithm Framework: Build Actor-Critic dual neural network structure to optimize control policy through episodic sampling, experience storage and iterative update.
Real-time Visualization: Dynamically plot episode reward, episode length, training loss and action distribution to observe training trends intuitively.
Model Saving: Automatically export well-trained model weights as .pth files for permanent storage and secondary loading.
Inference Demo: Launch a rendered simulation environment after training, load the trained policy and verify the balancing performance visually.
Project Structure
plaintext
.
├── daolibai.py          # Main training & inference script
├── cartpole_best_model.pth  # Saved trained model
└── tutorial_for_mujoco-main/
    └── rsl_rl/          # Local RSL-RL dependency library
Dependencies
plaintext
python>=3.10
torch
gymnasium
matplotlib
numpy
tensordict
rsl-rl
How to Run
Install required dependencies.
Place the rsl_rl folder in the correct directory path.
Execute the main script:
bash
运行
python daolibai.py
Training Process
Initialize the CartPole simulation environment and neural network models.
Interact with the environment to collect exploration experience.
Update Actor and Critic networks via PPO optimization.
Refresh real-time visualization charts to record training indicators.
Complete iterative training until the agent converges to the optimal balance policy.
Model & Inference
After training, the optimal model will be saved as cartpole_best_model.pth.
The program automatically starts a rendered demo, where the trained agent keeps the pole balanced for a maximum of 500 steps.
The saved model can be loaded independently for secondary testing, parameter fine-tuning and deployment.
Performance
The agent can quickly converge during training, reach the maximum score of 500 points in CartPole-v1, and maintain stable long-term balance control in continuous inference.
