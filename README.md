# Snake AI with Deep Q-Learning

An autonomous Snake game agent implemented in Python using PyTorch and Pygame. This project demonstrates Reinforcement Learning (RL), Deep Q-Networks (DQN), and Experience Replay to train an AI to play Snake.

## Overview

This project implements a Deep Q-Learning agent that learns to play Snake from scratch. The agent starts with zero knowledge and learns by trial and error. It observes the environment (state), takes actions, and receives rewards (positive for eating, negative for dying), progressively optimizing a neural network to maximize its score.

## Key Features

* **Deep Q-Network (DQN):** Uses a feed-forward neural network (Linear_QNet) to predict the best action based on the current game state.
* **Experience Replay:** Implements a memory buffer (`deque`) to store past experiences and retrains on random batches to improve long-term stability.
* **Epsilon-Greedy Strategy:** Balances exploration (random moves) and exploitation (using the trained model) to prevent getting stuck in local optima.
* **Real-time Visualization:** Uses Matplotlib to plot the score and mean score in real-time as the agent trains.

### Code Structure

#### 1. Agent (`agent.py`)
The "brain" of the operation. It manages the training loop, stores memory, and makes decisions.

#### 2. Model (`model.py`)
Defines the Neural Network architecture and the optimization logic.

#### 3. Game (`game.py`)
Manages the game environment using Pygame.

#### 4. Helper (`helper.py`)
Visualization utilities.

## Getting Started

### Prerequisites
* Anaconda or Miniconda installed on your machine.
* Basic understanding of terminal/command prompt usage.

### Installation & Usage

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/atienze/SnakeAgent.git](https://github.com/atienze/SnakeAgent.git)
    cd snake-ai-pytorch
    ```

2.  **Create and Activate Conda Environment**
    Create a fresh environment with Python 3.10 to ensure all dependencies work smoothly.
    ```bash
    conda create -n snake-ai python=3.10
    conda activate snake-ai
    ```

3.  **Install All Dependencies via Conda**
    Install PyTorch, Pygame, Matplotlib, and IPython using the `conda-forge` and `pytorch` channels.
    ```bash
    conda install pytorch torchvision -c pytorch
    conda install -c conda-forge pygame matplotlib ipython
    ```

4.  **Run the Training**
    ```bash
    python agent.py
    ```

## Example Output

When running the program, a Pygame window will show the gameplay, and a Matplotlib graph will appear showing the training progress:

```text
Game 1 Score 0 Record 0
Game 2 Score 1 Record 1
...
Game 85 Score 32 Record 32
