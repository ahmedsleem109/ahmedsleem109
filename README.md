<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:1F6FEB,100:8957E5&height=200&section=header&text=Ahmed%20Sleem&fontSize=60&fontColor=FFFFFF&fontAlignY=36&desc=Robot%20Learning%20Engineer%20%C2%B7%20Simulation-First%20Robotics&descAlignY=58&descSize=18&animation=fadeIn" width="100%" alt="Ahmed Sleem — Robot Learning Engineer" />

<a href="https://www.linkedin.com/in/ahmedsleem25/"><img src="https://img.shields.io/badge/LinkedIn-ahmedsleem25-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<img src="https://img.shields.io/badge/Open_to-Remote_%C2%B7_Relocation-2EA44F?style=for-the-badge" alt="Open to remote or relocation">
<img src="https://img.shields.io/badge/Cairo-Egypt-30363D?style=for-the-badge" alt="Cairo, Egypt">

</div>

I build robots that learn to walk, grasp and follow instructions in simulation, and then I test them until they fail.
I care less about a good demo than about knowing **why** a system breaks: every result I publish comes with its trial count, its seeds, its failure cases and the script that produced it.

- 🎓 **BSc Mechatronics & Robotics**, German University in Cairo
- 🤖 **Focus:** reinforcement learning for locomotion and whole-body control, vision-language-action (VLA) models, world models
- 💻 **Compute:** everything below was trained on one 6 GB laptop GPU (RTX 3060)

## Featured projects

### 🔧 WorkshopRobot — "bring me the 10mm wrench"

<img src="https://github.com/ahmedsleem109/WorkshopRobot/raw/main/media/readme_endtoend.gif" width="380" align="right" alt="Go2 quadruped with a Z1 arm fetching a tool">

A robot dog with an arm hears a tool request, walks to the workbench, finds the tool, picks it up and brings it back, and says something useful when it can't.

- **Grasping:** 125/125 (5 tools × 25 trials, while standing on its legs)
- **End to end:** 60/70 (86 %) over 7 scenario suites × 10 seeds; 8 of the 10 failures are falls on a step, not manipulation
- **Learned policy:** a fine-tuned SmolVLA went from 0/20 to **18/20** grasps on held-out scenes after a step-by-step diagnosis of why it failed

Stack: MuJoCo · RL walking policy · Qwen3-VL for finding objects · SmolVLA / LeRobot
**[Code & full results →](https://github.com/ahmedsleem109/WorkshopRobot)**

<br clear="right">

### 🛡️ Humanoid robustness study — what actually stops a humanoid from falling?

<img src="https://github.com/ahmedsleem109/humanoidmujoco/raw/main/results/gifs/v3_hero.gif" width="380" align="right" alt="Three G1 policies receiving the same shove">

The usual recipe for robust walking mixes random pushes during training with domain randomization. I trained three Unitree G1 policies that differ **only** in that, then shoved them 22,000 times.

- **Pushes do the work:** the force the robot survives half the time rises from **337 N to 639 N**
- **Domain randomization adds only 2.4 %** on top
- Includes a bug in my own evaluation that I found, fixed and documented (it was hiding the falls)

Stack: MuJoCo / mjlab · PPO · 4,096 parallel robots
**[Code & full results →](https://github.com/ahmedsleem109/humanoidmujoco)**

<br clear="right">

### 🤝 Bimanual tray carry — balancing a ball from camera images

<img src="https://github.com/ahmedsleem109/openarm-tray-carry/raw/main/docs/demo.gif" width="380" align="right" alt="Two arms carrying a tray with a ball, balancer off vs on">

Two OpenArm v2 arms pick up a tray and carry it while keeping a loose ball from rolling off, using only two camera images, with real collisions and nothing glued in place.

- **12/12** carries with camera noise, 40 ms latency, backlash, weak motors and randomized dynamics **all at once** (12 randomized layouts, fixed seeds)
- Without the balancer: **1/12**
- **[Try it in your browser →](https://ahmedsleem109.github.io/openarm-tray-carry/web/)** (real MuJoCo physics, shove the ball yourself)

**[Code & full results →](https://github.com/ahmedsleem109/openarm-tray-carry)**

<br clear="right">

## More projects

- **[RopePhysics](https://github.com/ahmedsleem109/RopePhysics)**: a C++/CUDA rope and cable simulator checked against textbook physics; a learned policy routes 1024/1024 new wire harnesses where a hand-written one routes none.
- **[Warehouse humanoid](https://github.com/ahmedsleem109/Warehouse-humanoid-)**: a G1 carrying a 4 kg tote (0/64 falls), planned by a small local vision-language model, with its breaking points mapped (latency, shoves, friction, motor strength).
- **[Baglens](https://github.com/ahmedsleem109/Baglens)**: checks whether a robot recording can be trusted before anyone debugs from it; published precision/recall, runs as an MCP server.
- **[Jointly](https://jointlyapp.netlify.app/)**: a desktop app that turns CAD into simulation-ready URDF, MJCF, SDF and USD robot models.
- **Humanoid triple backflip** *(private)*: a G1 runs off a cliff, does three backflips across the gap and lands running; 100 % strict success in evaluation with motors boosted to 2× torque.

## Currently working on

**Foresight**: a Unitree G1 with real Dex3-1 hands follows language instructions ("put the red mug on the shelf"), grasping with actual finger contact. A VLA model drives an RL whole-body controller, and a learned **world model imagines the next 1–2 seconds and blocks actions predicted to fall, collide or drop the object**.

## Open source

- **[unitree_rl_mjlab](https://github.com/unitreerobotics/unitree_rl_mjlab/pulls?q=author%3Aahmedsleem109)** (Unitree): dependency bounds that keep fresh installs working
- **[ros2_medkit](https://github.com/selfpatch/ros2_medkit/pulls?q=author%3Aahmedsleem109)**: fault debouncing and diagnostic-data fixes for ROS 2 robots

## Tech stack

<div align="center">

<img src="https://img.shields.io/badge/MuJoCo-1F6FEB?style=for-the-badge" alt="MuJoCo">
<img src="https://img.shields.io/badge/mjlab_%C2%B7_MJX_%C2%B7_Brax-6E40C9?style=for-the-badge" alt="mjlab, MJX, Brax">
<img src="https://img.shields.io/badge/RL-PPO-F78166?style=for-the-badge" alt="RL: PPO">
<img src="https://img.shields.io/badge/LeRobot_%C2%B7_SmolVLA-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="LeRobot, SmolVLA">
<img src="https://img.shields.io/badge/VLMs-Qwen--VL-8957E5?style=for-the-badge" alt="Qwen-VL">
<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++">
<img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" alt="CUDA">
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch">
<img src="https://img.shields.io/badge/JAX-A8B9CC?style=for-the-badge" alt="JAX">
<img src="https://img.shields.io/badge/ROS_2-22314E?style=for-the-badge&logo=ros&logoColor=white" alt="ROS 2">
<img src="https://img.shields.io/badge/ONNX-005CED?style=for-the-badge&logo=onnx&logoColor=white" alt="ONNX">

</div>

---

<div align="center">

*Looking for robot learning, RL and simulation roles.* **[Let's talk on LinkedIn →](https://www.linkedin.com/in/ahmedsleem25/)**

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8957E5,50:1F6FEB,100:0D1117&height=100&section=footer" width="100%" alt="" />

</div>
