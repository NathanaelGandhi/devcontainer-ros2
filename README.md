# devcontainer-ros2
- If you work on multiple projects, I would recommend cloning this repo with a project name instead of the default repo name. Example:
  - ```git clone https://github.com/NathanaelGandhi/devcontainer-ros2.git my-project```
- Feel free to add 0-unlimited ros2_ws(s) or whatever else you like into this devcontainer

## Extra Notes:
- You are responsible for sourcing ROS2 in every new shell:
  - ```source /opt/ros/humble/setup.bash && source install/local_setup.bash```
- The devcontainer will update and install rosdeps post creation
- The devcontainer targets the latest image at [ghcr.io/NathanaelGandhi/dev-image-ros2](ghcr.io/NathanaelGandhi/dev-image-ros2)
- All files that were not cloned from this repo are ignored by git. See [.gitignore](.gitignore)

