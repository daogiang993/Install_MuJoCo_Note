# Install MuJoCo Notes on Ubuntu 16.04

1. Get License (2 days)

2. Create folder ~/.mujoco

3. Download and extract mjpro150 to ~/.mujoco folder

4. Copy mjkey.txt to ~/.mujoco and ~/.mujoco/mjpro150/bin

5. Install GLEW <br />
sudo apt-get install libglew-dev

6. Install mujoco_py <br />
cd ~ <br />
git clone https://github.com/openai/mujoco-py.git <br />
cd mujoco_py <br />
pip install --no-cache-dir -e .

7. Try humanoid simulation <br />
cd ~/.mujoco/mjpro150/bin <br />
./simulate ../model/humanoid.xml

8. Add LD_PRELOAD to ~/.bashrc <br />
Add "export LD_PRELOAD=/usr/lib/x86_64-linux-gnu/libGLEW.so:/usr/lib/nvidia-384/libGL.so" to ~/.bashrc
