# AlphaGo Zero for Connect6

#### This repository is based on alpha-omok made by RLKorea. [Original Code for Omok version](https://github.com/reinforcement-learning-kr/alpha_omok)

AlphaZero is a Reinforcement Learning algorithm which is effectively combine [MCTS(Monte-Carlo Tree Search)](https://en.wikipedia.org/wiki/Monte_Carlo_tree_search) with Actor-Critic. The RL model is implemented by [Pytorch](https://pytorch.org/).

**Usage**
- Go [Pytorch](https://pytorch.org/) and install it.
- pip install pygame
- python main.py (for training, default: 9x9 board)
- python eval_main.py (you can play the game with alpha)


<br>

## Project objective

There are 2 objectives to achieve in this project  
1. Implement AlphaZero on Connect6
2. Optimize the code

<br>

## Documents (Original version, will be modified soon.)

- [ID-based implementation](https://github.com/reinforcement-learning-kr/alpha_omok/blob/developer/docs/1_ID_based.md)
- [Description of the parameters](https://github.com/reinforcement-learning-kr/alpha_omok/blob/developer/docs/2_Parameters.md)
- [How to change the environment](https://github.com/reinforcement-learning-kr/alpha_omok/blob/developer/docs/3_How_to_change_env.md)
- [How to load the saved model](https://github.com/reinforcement-learning-kr/alpha_omok/blob/developer/docs/4_How_to_load_model.md)
- [How to use eval_main](https://github.com/reinforcement-learning-kr/alpha_omok/blob/developer/docs/5_How_to_use_eval_main.md)
- [Log file](https://github.com/reinforcement-learning-kr/alpha_omok/blob/developer/docs/6_Log_file.md)

<br>

## Description of the Folders

### 1_tictactoe_MCTS

<p align= "center">
  <img src="./image/tictactoe.PNG" width="300" alt="TicTacToe Image" />
</p>

 This folder is for implementing MCTS in [Tic-Tac-Toe](https://en.wikipedia.org/wiki/Tic-tac-toe). If you want to study MCTS only, please check the files in this folder. <br>

The description of the files in the folder is as follows. (files with **bold text** are codes for implementation)

- env: Tic-Tac-Toe environment code (made with [pygame](https://www.pygame.org/news))
- **mcts_guide**: MCTS doesn't play the game, it only recommends how to play. 
- **mcts_vs**: User can play against MCTS algorithm. 
- utils: functions for implementing algorithm. 


<br>


### 2_AlphaOmok

<p align= "center">
  <img src="./image/mini_omok_game.png" width="300" alt="mini omok Image" />
</p>

  The folder is for implementing AlphaZero algorithm in omok environment. There are two versions of omok (env_small: 9x9, env_regular: 15x15). The above image is sample image of 9x9 omok game <br>

 The description of the files in the folder is as follows. (files with **bold text** are codes for implementation)

- **eval_main**: code for evaluating the algorithm on both local PC and web
- **main**: main training code of Alpha Zero
- model: Network model (PyTorch)
- agents: Agent and MCTS algorithm 
- utils: functions for implementing algorithm 
- WebAPI: Implementation of web API

<br>


## Reference

1. [Mastering the Game of Go with Deep Neural Networks and Tree Search](https://storage.googleapis.com/deepmind-media/alphago/AlphaGoNaturePaper.pdf)
2. [Mastering the Game of Go without Human Knowledge](https://www.nature.com/articles/nature24270)

