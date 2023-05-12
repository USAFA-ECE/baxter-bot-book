# Welcome to the BAXTER Bot

The BAXTER Bot is a two-armed robot donated to DFEC by AFRL.  This book will document the setup and usage of the robot.

This book is built as a Jupyter Book.  Check out [the Jupyter Book documentation](https://jupyterbook.org) for more information.

```{tableofcontents}
```


# Getting Started with BAXTER
1. BAXTER communicates over a wired ethernet connection, locate the ethernet port on the back of the bot and connect it to your computer
    - Set your wired IP to 169.25.9.100 and your netmask to 255.255.255.0 so you can communicate to baxter
    - Test connectivity by pinging BAXTER at 169.25.9.188 from your machine
2. You need an installation of ROS 1 to run the AFRL BAXTER enviorment, they used melodic but noetic works with some tweaks.
    - Follow ROS Noetic instalation:https://wiki.ros.org/noetic/Installation/Ubuntu and enviorment setup instructions:https://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment
    - If you want to use Melodic, good luck but it is possible to build from source: https://wiki.ros.org/melodic/Installation/Source
    - **Important Note** when setting up your ROS enviorment, name the workspace directory ros_ws, not catkin_ws.
3. Download and extract afrl-files.zip and ros_ws.zip from the baxter-bot-book git repo.
4. Delete devel and build directories from the extracted ros_ws.
5. Copy the remaining contents of the extracted ros_ws into your new ros_ws.
6. catkin_make and source /devel/setup.bash
7. Open the baxter.sh file in ros_ws with the text editor of your choice
    - edit line 30 to specify your chosen ROS distribution

# Running USAFA.py
USAFA.py written by Cason Couch is a parody of the YMCA dance where BAXTER spells out USAFA with its arms.
1. Open a terminal in your ros_ws and run:
    - ". baxter.sh"
    - "rosrun baxter_tools enable_robot.py -e"
3. in a seperate terminal in the ros_ws run:
    - ". baxter.sh"
    - "cd /home/your-pycharm-installation/bin directory" (ex. /home/dfec/Desktop/pycharm-community-2023.1.1/bin)
    - "./pycharm.sh" to open pycharm in the enviorment
4. In pycharm navigate to ros_ws/src/brain/motions and open USAFA.py
5. Run USAFA.py from pycharm

# Notes from working with BAXTER
- The AFRL zip file has all the documentation that was provided to USAFA from BAXTER's previous owners (AFRL)  highly reccommend reading them in their entirety.
- The ros_ws zip file contains the last known 'working' ros workspace in its entierty, a good project may be to update it for python 3 and ROS noetic use.
- Everything is written in python2 so if you are running python 3 you will have to fix some syntax errors
- An alternative is to just use the latest version of python 2, which is recommended.

