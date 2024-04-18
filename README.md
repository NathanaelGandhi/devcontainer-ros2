# devcontainer-ros2
- If you work on multiple projects, clone this repo with a project name instead of the default. Example:
  - ```git clone https://github.com/NathanaelGandhi/devcontainer-ros2.git <my-project>```
- Feel free to add 0-unlimited ros2_ws(s) or whatever else you like into this devcontainer

## Recommendations:
- add a ```.clang-format``` file to your ws such as [ament_clang_format](https://github.com/ament/ament_lint/blob/rolling/ament_clang_format/ament_clang_format/configuration/.clang-format)
- add a ```.pre-commit-config.yaml``` file to your ws such as [pre-commit all the things](https://gist.github.com/NathanaelGandhi/a11fa649d2d25516e4829d90bbb744a5)

## Extra Notes:
- You are responsible for sourcing ROS2 in every new shell:
  - ```source /opt/ros/humble/setup.bash && source install/local_setup.bash```
- The devcontainer will update and install rosdeps post creation
- The devcontainer targets the latest image at [ghcr.io/NathanaelGandhi/dev-image-ros2](ghcr.io/NathanaelGandhi/dev-image-ros2)
- [c_cpp_properties.json](.vscode/c_cpp_properties.json) recursively includes from the vscode workspace dir
- There are [vscode tasks](.vscode/tasks.json) to ```clean```, ```build``` and ```test```
- All files that were not cloned from this repo are ignored by git. See [.gitignore](.gitignore)
