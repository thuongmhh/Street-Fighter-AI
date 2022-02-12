# Street Fighter AI
Trained with Reinforcement Learning / PPO / PyTorch / Stable Baselines

## Techniques:
- Use health-based reward function instead of score-based so the agent can learn how to defense themself and attack the enemy.
- Reduce the action space from MultiBinary(12) (4096 choices) to Discrete(14) to make the training more efficient.
- Make the episode one fight only instead of best-of-three. It helps value estimation.
- Preprocess the environment with AtariWrapper (NoopReset, FrameSkip, Resize, Grayscale) to reduce input size.
- Use multiprocessing for faster training and bypass OpenAI Gym Retro limitation on one environment per process.

## Results:
- 100% win-rate against the enemy
- Much HP remaining after the fight
