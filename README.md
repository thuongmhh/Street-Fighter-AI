# Street Fighter II AI

Trained with Reinforcement Learning / PPO / PyTorch / Stable Baselines, inspired by [@nicknochnack](https://github.com/nicknochnack/StreetFighterRL).

## Techniques

-   Use health-based reward function instead of score-based so the agent can learn how to defend itself while attacking the enemy. It makes a defensive strategy to win the game. You may want to modify the function to penalize the time spent for a more offensive strategy.
-   Reduce the action space from MultiBinary(12) (4096 choices) to Discrete(14) to make the training more efficient. You may want to add [combos](https://www.eventhubs.com/moves/usf2/ryu/) to make the fight more interesting.
-   Make the episode one fight only instead of best-of-three. It helps value estimation.
-   Preprocess the environment with AtariWrapper (NoopReset, FrameSkip, Resize, Grayscale) to reduce input size.
-   Use multiprocessing for faster training and bypass OpenAI Gym Retro limitation on one environment per process.

## Results

-   100% win-rate against the enemy
-   Much HP remaining after the fight
-   Trained model is saved in [latest_model.zip](latest_model.zip)
-   Training and Testing scripts can be viewed in [StreetFighter.ipynb](StreetFighter.ipynb)

## Replay

![Game 1](replays/game_1.gif)
