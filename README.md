<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:1F6FEB,100:8957E5&height=210&section=header&text=Ahmed%20Sleem&fontSize=62&fontColor=FFFFFF&fontAlignY=36&desc=Robot%20Learning%20Engineer%20%E2%80%A2%20Humanoids%20%E2%80%A2%20RL%20%E2%80%A2%20VLAs%20%E2%80%A2%20World%20Models&descAlignY=58&descSize=17&animation=fadeIn" width="100%" alt="Ahmed Sleem — Robot Learning Engineer" />

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=3200&pause=900&color=58A6FF&center=true&vCenter=true&multiline=false&width=720&height=40&lines=I+teach+humanoid+robots+to+move.;Then+I+find+exactly+where+they+break.;Then+I+fix+the+cause%2C+not+the+symptom." alt="I teach humanoid robots to move. Then I find exactly where they break." />

<br>

<a href="https://www.linkedin.com/in/ahmedsleem25/"><img src="https://img.shields.io/badge/LinkedIn-ahmedsleem25-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<img src="https://img.shields.io/badge/Open_to-Remote_%C2%B7_Relocation-2EA44F?style=for-the-badge&logo=rocket&logoColor=white" alt="Open to remote or relocation">
<img src="https://img.shields.io/badge/Cairo-Egypt-30363D?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Cairo, Egypt">

</div>

<br>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&pause=100000&color=E6EDF3&vCenter=true&width=500&height=34&lines=%3E+about_me" alt="about me" />

```yaml
role:      Robot learning engineer (simulation-first)
focus:     [RL locomotion & whole-body control, vision-language-action models, world models]
robots:    [Unitree G1 + Dex3-1 hands, Unitree Go2 + Z1 arm, OpenArm v2 bimanual]
method:    train -> stress-test -> measure with confidence intervals -> fix the root cause
hardware:  one 6 GB laptop GPU (RTX 3060), no cluster
education: BSc Mechatronics & Robotics, German University in Cairo
```

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&pause=100000&color=E6EDF3&vCenter=true&width=500&height=34&lines=%3E+projects" alt="projects" />

> **🦾 Humanoid triple backflip** — An RL policy that makes a Unitree G1 run off a cliff, chain **three backflips** across the gap, land on the lower cliff and keep running. Reached **100 % strict success** through a staged curriculum, with every failed attempt diagnosed and documented. *(Motors boosted to 2× torque, labelled.)*

> **🛡️ [Humanoid robustness study](https://github.com/ahmedsleem109/humanoidmujoco)** — Pushes or domain randomization: which one actually makes a humanoid robust? Three G1 policies, **22,000 shoves**. Pushes nearly double the recovery force (**337 N → 639 N**); domain randomization adds only **2.4 %**.

> **🔧 [Language-commanded mobile manipulator](https://github.com/ahmedsleem109/WorkshopRobot)** — *"Bring me the 10mm wrench."* A Go2 quadruped with a Z1 arm finds, grasps and delivers tools using a VLM, an RL walker and a fine-tuned SmolVLA. **125/125 grasps, 86 % end to end**, failures traced to their real cause.

> **🤝 [Bimanual tray carry](https://github.com/ahmedsleem109/openarm-tray-carry)** — Two OpenArm v2 arms carry a tray while balancing a loose ball, from camera images only. **12/12** carries under noise, latency, backlash and weak motors at once. [Runs in the browser.](https://ahmedsleem109.github.io/openarm-tray-carry/web/)

> **📦 [Warehouse humanoid](https://github.com/ahmedsleem109/Warehouse-humanoid-)** — A G1 carrying a 4 kg tote, planned by a local 4-bit VLM. **0/64 falls** at full load, with the exact breaking points mapped: latency, shove force, floor friction, motor strength.

> **🧵 [RopePhysics](https://github.com/ahmedsleem109/RopePhysics)** — A C++/CUDA cable simulator validated against textbook physics. A learned policy routes **1024/1024** unseen wire harnesses; the hand-written baseline routes none.

> **🔍 [Baglens](https://github.com/ahmedsleem109/Baglens)** — Audits robot recordings before anyone debugs from them: silent gaps, stale data, broken transforms. Published precision and recall, and an honest *"unassessable"* when it can't tell. Ships as an MCP server.

> **⚙️ [Jointly](https://jointlyapp.netlify.app/)** — A desktop app that converts CAD (STEP, SolidWorks, meshes) into simulation-ready **URDF, MJCF, SDF and USD** automatically.

> **🔭 Foresight** *(in progress)* — A G1 with real Dex3-1 hands performs language-instructed loco-manipulation with **finger-contact grasping**. A VLA drives an RL whole-body controller, and a learned **world model vetoes actions predicted to fall, collide or drop**.

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&pause=100000&color=E6EDF3&vCenter=true&width=500&height=34&lines=%3E+open_source" alt="open source" />

- **[unitree_rl_mjlab](https://github.com/unitreerobotics/unitree_rl_mjlab/pulls?q=author%3Aahmedsleem109)** (Unitree) — dependency bounds that keep fresh installs working
- **[ros2_medkit](https://github.com/selfpatch/ros2_medkit/pulls?q=author%3Aahmedsleem109)** — fault debouncing and diagnostic-data fixes for ROS 2 robots

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=24&pause=100000&color=E6EDF3&vCenter=true&width=500&height=34&lines=%3E+tech_stack" alt="tech stack" />

<div align="center">

**Robot learning**<br>
<img src="https://img.shields.io/badge/Reinforcement_Learning-PPO-F78166?style=for-the-badge" alt="RL">
<img src="https://img.shields.io/badge/Imitation_Learning-LeRobot-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="LeRobot">
<img src="https://img.shields.io/badge/VLA-SmolVLA-FF9D00?style=for-the-badge&logo=huggingface&logoColor=black" alt="SmolVLA">
<img src="https://img.shields.io/badge/VLMs-Qwen--VL-8957E5?style=for-the-badge" alt="Qwen-VL">

**Simulation**<br>
<img src="https://img.shields.io/badge/MuJoCo-1F6FEB?style=for-the-badge" alt="MuJoCo">
<img src="https://img.shields.io/badge/mjlab-0D1117?style=for-the-badge" alt="mjlab">
<img src="https://img.shields.io/badge/MJX_%C2%B7_Brax-6E40C9?style=for-the-badge" alt="MJX, Brax">
<img src="https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white" alt="CUDA">

**Engineering**<br>
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++">
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch">
<img src="https://img.shields.io/badge/JAX-A8B9CC?style=for-the-badge" alt="JAX">
<img src="https://img.shields.io/badge/ROS_2-22314E?style=for-the-badge&logo=ros&logoColor=white" alt="ROS 2">
<img src="https://img.shields.io/badge/ONNX-005CED?style=for-the-badge&logo=onnx&logoColor=white" alt="ONNX">
<img src="https://img.shields.io/badge/SolidWorks-DA291C?style=for-the-badge" alt="SolidWorks">

</div>

<br>

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&pause=1500&color=8B949E&center=true&vCenter=true&width=700&height=30&lines=Looking+for+robot+learning+%C2%B7+RL+%C2%B7+simulation+roles.;Let's+build+robots+that+don't+fall+over." alt="Looking for robot learning, RL and simulation roles" />

<a href="https://www.linkedin.com/in/ahmedsleem25/"><img src="https://img.shields.io/badge/Let's_talk-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="Let's talk on LinkedIn"></a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8957E5,50:1F6FEB,100:0D1117&height=110&section=footer" width="100%" alt="" />

</div>
