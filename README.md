# devcontainer-ros2
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/NathanaelGandhi/devcontainer-ros2/main.svg)](https://results.pre-commit.ci/latest/github/NathanaelGandhi/devcontainer-ros2/main)
[![Release Drafter](https://github.com/NathanaelGandhi/devcontainer-ros2/actions/workflows/release-drafter.yml/badge.svg?branch=release)](https://github.com/NathanaelGandhi/devcontainer-ros2/actions/workflows/release-drafter.yml)
[![Mirror release to humble](https://github.com/NathanaelGandhi/devcontainer-ros2/actions/workflows/mirror-release-to-humble.yaml/badge.svg?branch=release)](https://github.com/NathanaelGandhi/devcontainer-ros2/actions/workflows/mirror-release-to-humble.yaml)

- If you work on multiple projects, clone this repo with a project name instead of the default. Example:
  - ```git clone --recursive https://github.com/NathanaelGandhi/devcontainer-ros2.git <my-project>```
- Feel free to add 0-unlimited ros2_ws(s)/packages or whatever else you like into this devcontainer,<br>it can act as a ws or just a dir, it is up to you

## Recommendations:
- add a ```.clang-format``` file to your ws such as [ament_clang_format](https://github.com/ament/ament_lint/blob/rolling/ament_clang_format/ament_clang_format/configuration/.clang-format)
- add a ```.pre-commit-config.yaml``` file to your ws such as [pre-commit all the things](https://gist.github.com/NathanaelGandhi/a11fa649d2d25516e4829d90bbb744a5)

## Extra Notes:
- You are responsible for sourcing ROS2 in every new shell:
  - ```source /opt/ros/humble/setup.$(basename $SHELL) && source install/local_setup.$(basename $SHELL)```
  - Helpful envs are provided through direnv. See config in [.envrc](.envrc)
    | Source target | Shell agnostic | bash | zsh |
    | --- | --- | --- | --- |
    | ROS2 | ```$sr``` | ```$bsr``` | ```$zsr``` |
    | colcon | ```$sc``` | ```$bsc``` | ```$zsc``` |
    | local colcon | ```$slc``` | ```$bslc``` | ```$zslc``` |
- The devcontainer will update and install rosdeps post creation
- The devcontainer targets the latest dev image that you can build from the [containers-ros2](containers-ros2) submodule
- [c_cpp_properties.json](.vscode/c_cpp_properties.json) recursively includes from the vscode workspace dir
  - this is a good reason to NOT store separate source and ros_ws(s) under this dir, IntelliSense will hate you
- There are [vscode tasks](.vscode/tasks.json) to ```clean```, ```build``` and ```test```
- All files that were not cloned from this repo are ignored by git. See [.gitignore](.gitignore)
