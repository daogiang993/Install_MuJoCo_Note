# Install MuJoCo Notes on Ubuntu 16.04

1. Get License (2 days)

2. Create folder ~/.mujoco

3. Download and extract mjpro150 to ~/.mujoco folder

4. Copy mjkey.txt to ~/.mujoco and ~/.mujoco/mjpro150/bin

5. Install GLEW
sudo apt-get install libglew-dev

6. Install mujoco_py
cd ~
git clone https://github.com/openai/mujoco-py.git
cd mujoco_py
pip install --no-cache-dir -e .

7. Try humanoid simulation
cd ~/.mujoco/mjpro150/bin
./simulate ../model/humanoid.xml

8. Add LD_PRELOAD to ~/.bashrc
Add "export LD_PRELOAD=/usr/lib/x86_64-linux-gnu/libGLEW.so:/usr/lib/nvidia-384/libGL.so" to ~/.bashrc
