### Arm Control 

Webapp for basic control and sequence management is at `http://ip.add.re.ss:9072/`

There are two ways to control the arm *remotely* via code:

#### ROS

- ssh login to the raspberry-pi is `pi`, password `evodyne2020`

- Once logged into the pi:
  - The webserver home directory is `~/system/srv` if needed
  - Go to `~/userprograms` to see example python scripts to control the arm via ROS

You can change the rosmaster in `~/ros_master.txt` to point it at a different machine if needed, or your other machine can point to the Pi as the master. Then to see simple control commands, see `~/userprograms/example.py` as an example.

#### HTTP

You can use simple HTTP rest commands from any external/on-board script/program to access the arm position and send movement commands, like so:
`http://192.168.1.75:9072/command?cmd=direct&v1=r:233.915,h:110,v:30,a:97.80102`
where:
- `r` is radius, distance of gripper tip from center of base
- `h` is height of gripper tip
- `v` is angle of gripper from vertical, 0 being straight down

Together `r`, `h`, `v` define the 2D position of the gripper using inverse kinematics.
By adding the base swivel angle using "a", allows for specifying a 3d position in range of motion

`a` through `f` are the angles of each motor from base to gripper, with 90 being the center. For example, to close the gripper:
`http://192.168.1.75:9072/command?cmd=direct&v1=f:60`

Whenever you provide multiple joint targets in the same command, it will attempt synchronized
movement as much as possible, for example:
`http://192.168.1.75:9072/command?cmd=direct&v1=a:50,b:60,c:70`

To query the arm's current position, use `http://192.168.1.75:9072/getstatus`

All responses should be in json.

### Camera

After starting the camera service, you can access the camera feed in any browser or in python OpenCV using:
`http://ip.add.re.ss:8000/stream.mjpg`

More useful sometimes, you can get the most recent frame using:
`http://ip.add.re.ss:8000/frame.jpg`

You can even start/stop the camera like so:
- `http://ip.add.re.ss:9072/command?cmd=servicestart&v1=camera`
- `http://ip.add.re.ss:9072/command?cmd=servicestop&v1=camera`

If needed to do on-board computation, Opencv 3.4.12 is pre-installed. 

To see an example python script which does face-following by fetching the feed from the on-board camera, see:
`https://www.evodyneacademy.com/forum/evoarm-apps/how-do-you-post-commands-to-the-robot-from-desktop`

On the raspberry pi, you can also see the script `~/userprograms/facedetect/facedetect-cont.py` and run the script `runfacedetect-continuous.sh`.
On the raspberry pi itself, it will run very slow if you have the legacy version of the Raspberry Pi zero, but much faster if you have the newer Raspberry Pi Zero 2.
