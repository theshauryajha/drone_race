## Drone Racing

### Description
- A player navigates a given track with either controller or keyboard input and tries to recrod the fastest legit lap
- We will use the ros package joy or teleop-twist-keyboard to give control commands to the drone (controller & keyboard respectively)

### Use the package
- Inside the src folder of your workspace, clone this repository
- Clone the Hector Quadrotor package
    ```
    https://github.com/tu-darmstadt-ros-pkg/hector_quadrotor
    ```
- Make the scripts and the launch files executable by running the following commands inside the drone_race package
  ```bash
  chmod +x src/scripts/*
  chmod +x launch/*
  ```

### Playing the game
- Navigate to drone_race/launch
- To play using a **controller** (suggested for better experience):
  ```bash
  ./launch_tmux.sh player_name
  ```

- To play using a **keyboard**:
  ```bash
  ./launch_tmux.sh player_name --keyboard
  ```
### After the game
- Press Ctrl+C in the terminal
- In the tmux window, run the following command
  ```bash
    tmux kill-session -t drone_race
  ```