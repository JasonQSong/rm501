## To test
git clone https://github.com/JasonQSong/rm501.git
cd rm501
git fetch --all
git checkout -b proj2 origin/proj2
make
./rm501

![rm501.png](doc/rm501.png)


## Features

 * OpenGL gui,
 * ncurses gui (WIP),
 * controll from keyboard, JoyPad or SpaceNavigator,
 * forward and inverse kinematics (double precision math),
 * inter-process communication via UNIX domain socket (WIP).

## Video

[![Mitsubishi RM-501 Movemaster II Robot Simulator](http://img.youtube.com/vi/ddvIzk9aeJo/0.jpg)](https://www.youtube.com/watch?v=ddvIzk9aeJo)

## Compile and run

Required libraries: OpenGL, SDL2, SDL2_ttf (-- not SDL_ttf2!)
Optional libraries: ncurses, LinuxCNC/Machinekit HAL

```bash
$ sudo apt-get -y install mesa-common-dev libsdl2-dev libsdl2-ttf-dev libsdl2-net-dev
```

```bash
$ make
$ ./rm501
```

Remote control:
```bash
$ socat READLINE,history=$HOME/.rm501_history TCP:127.0.0.1:8888,crlf
```
or
```bash
$ nc localhost 8888 # if the above command does not work for you.
```

## Authors

https://github.com/koppi
