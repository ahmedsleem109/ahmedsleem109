### Ahmed Selim — I find where robot policies break, and what actually fixes it.

I train robot policies (RL locomotion, imitation learning, vision-language-action models) on one 6 GB laptop GPU.
Then I push them until they fail: shoves, payloads, latency, friction, sensor noise, unseen objects.
I measure the failures properly: fixed seeds, confidence intervals, each failure tagged with its cause, scripted parts labelled as scripted.
Then I fix the cause rather than the symptom, and I report what didn't work as well.
All of the work below is in simulation (MuJoCo).

| | Question | Answer |
|---|---|---|
| <img src="https://github.com/ahmedsleem109/humanoidmujoco/raw/main/results/gifs/v3_hero.gif" width="220"> | **[humanoidmujoco](https://github.com/ahmedsleem109/humanoidmujoco)**: the standard robustness recipe bundles random pushes with domain randomization. Which half does the work? | Three Unitree G1 policies, identical except for training disturbances, shoved 22,000 times. Pushes raise the 50 %-recovery force from **337 N to 639 N**. Domain randomization adds only **2.4 %**. |
| <img src="https://github.com/ahmedsleem109/WorkshopRobot/raw/main/media/readme_endtoend.gif" width="220"> | **[WorkshopRobot](https://github.com/ahmedsleem109/WorkshopRobot)**: "bring me the 10mm wrench". Where does a language-commanded mobile manipulator (Go2 + Z1) fail? | **125/125** grasps, **86 %** end to end. **8 of the 10 failures are locomotion** (stepping down while carrying), not manipulation. SmolVLA grasps **18/20** on held-out scenes. |
| <img src="https://github.com/ahmedsleem109/openarm-tray-carry/raw/main/docs/demo.gif" width="220"> | **[openarm-tray-carry](https://github.com/ahmedsleem109/openarm-tray-carry)**: two arms carry a tray with a loose ball on it, from camera images only. Does it survive a sim-to-real model? | **12/12** carries with noise, latency, backlash, weak motors and randomized dynamics all applied at once. Without the balancer: **1/12**. |
| | **[Warehouse-humanoid](https://github.com/ahmedsleem109/Warehouse-humanoid-)**: a G1 carrying a 4 kg tote, with a small vision-language model planning its tasks. Where does it break? | **0/64** falls at 4 kg. It breaks at **≥ 80 ms latency** (100 % falls), ≥ 400 N shoves and floor friction 0.1. |
| <img src="https://github.com/ahmedsleem109/RopePhysics/raw/main/docs/media/harness.gif" width="220"> | **[RopePhysics](https://github.com/ahmedsleem109/RopePhysics)**: a rope and cable simulator (C++/CUDA) checked against textbook physics. Can a robot learn to route a wire harness in it? | Routing success goes from **2 % to 85 %** in 129 s on the GPU. The learned motion routes **1024/1024** new random cables. A hand-written motion routes **0**. |

BSc Mechatronics & Robotics, GUC · Cairo, Egypt · open to remote work · [LinkedIn](https://www.linkedin.com/in/ahmedsleem25/)
