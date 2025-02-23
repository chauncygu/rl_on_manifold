# Acting on the Tangent Space of the Constraint Manifold
<p align="center">
<img src=https://github.com/PuzeLiu/rl_on_manifold/blob/master/fig/manifold.gif width="400">
</p>
Implementation of "Robot Reinforcement Learning on the Constraint Manifold"

[[paper]](https://www.ias.informatik.tu-darmstadt.de/uploads/Team/PuzeLiu/CORL_2021_Learning_on_the_Manifold.pdf)
[[website]](https://sites.google.com/view/robot-air-hockey/atacom)

## Install (for python 3.7, 3.8)
```python
pip install -e .
conda install pinocchio -c conda-forge
```

## Install (for python 3.6)
```python
pip install -e .
conda install pinocchio -c conda-forge
pip3 install torch==1.2.0+cpu torchvision==0.4.0+cpu -f https://download.pytorch.org/whl/torch_stable.html
Looking in links: https://download.pytorch.org/whl/torch_stable.html
```


## Run Examples
```python
cd examples
```
### CircularMotion Environment. 
Environment options [A, E, T], algorithms options [TRPO, PPO, SAC, DDPG, TD3]
```python
python circle_exp.py --render --env A --alg TRPO
```

```python
python circle_exp.py --render --env A --alg PPO
```

### PlanarAirHockey Environment. 
Environment options [H, D, UH, UD], algorithms options [TRPO, PPO, SAC, DDPG, TD3]
```python
python planar_air_hockey_exp.py --debug-gui --env H --alg SAC
```

### IiwaAirHockey Environment. 
Environment options [7H, RMP], algorithms options [TRPO, PPO, SAC, DDPG, TD3]
```python
python iiwa_air_hockey_exp.py --debug-gui --env 7H --alg SAC
```

### CollisionAvoidance Environment. 
Environment options [C], algorithms options [TRPO, PPO, SAC, DDPG, TD3]
```python
python collision_avoidance_exp.py --render --env C --alg SAC
```


## Bibtex
```bibtex
@inproceedings{CORL_2021_Learning_on_the_Manifold,
  author =      "Liu, P. and  Tateo D. and  Bou-Ammar, H. and  Peters, J.",
  year =        "2021",
  title =       "Robot Reinforcement Learning on the Constraint Manifold",
  booktitle =   "Proceedings of the Conference on Robot Learning (CoRL)",
  key =	        "robot learning, constrained reinforcement learning, safe exploration",
}
```
