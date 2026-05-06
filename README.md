# Train Circle - ROS 2 + Gazebo Sim

Ce projet ROS 2 (Jazzy) simule un train compose d une locomotive et 3 wagons qui tournent en cercle autour d un bloc central dans Gazebo Sim.

## Description
- Une locomotive rouge et 3 wagons (bleu, vert, jaune) tourment en cercle
- Les wagons sont colles les uns aux autres grace aux joints fixes
- Le train utilise le plugin TrajectoryFollower de Gazebo Sim
- Le trajet circulaire est calcule mathematiquement avec 80 points de passage

## Lancer le projet
```bash
gz sim -r ~/ros2_ws/src/train_circle/worlds/train_world.world
```
https://github.com/user-attachments/assets/30ae854e-cf75-4db0-b389-d8774a013730
## Commandes utiles
```bash
# Mettre en pause le train
gz topic -t "/model/train/trajectory_follower/pause" -m gz.msgs.Boolean -p "data: true"

# Reprendre le train
gz topic -t "/model/train/trajectory_follower/pause" -m gz.msgs.Boolean -p "data: false"
```

## Technologies
- ROS 2 Jazzy
- Gazebo Sim
- Plugin TrajectoryFollower
- Python 3
