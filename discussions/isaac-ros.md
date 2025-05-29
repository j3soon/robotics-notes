# Isaac ROS Discussions

This page contains paraphrased discussions that may be useful for future reference. Also note that these discussions are searchable from the search bar in the website.

For issues related to this page, please [open a GitHub issue](https://github.com/j3soon/robotics-notes/issues).

## The script `run_dev.sh` failed with `urlopen error`.

Q: See [this issue](https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_common/issues/147).

A: This may be due to your internet connection. Try connecting to a different network. I recall that Taiwan university networks are sometimes limited by GitHub, which may cause this issue.

> 2024-09-22. Isaac ROS v3.0.x [e8760a6](https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_common/tree/e8760a63dd9f4e428dbe01b597f265020792217c).

## JetPack version for using Isaac ROS

Q: What is the recommended JetPack version for using Isaac ROS?

A: Please refer to the [Isaac ROS Getting Started Guide](https://nvidia-isaac-ros.github.io/getting_started/index.html#system-requirements). For example, for Isaac ROS v3.1, the recommended JetPack version is JetPack 6.0, as described in the docs.

> 2024-10-12. Isaac ROS v3.1.

## Docker image on NGC vs. building from source

Q: Is better to get the docker image from NGC Catalog or follow the tutorials to build it from source using `run_dev.sh`?

A: I recommend following [the getting started guide](https://nvidia-isaac-ros.github.io/getting_started/dev_env_setup.html) for simplicity. The initial build will take some time, so you may want to let it run while you do other tasks. Docker is pre-installed on Jetson Orin Nano, so you can use its commands to manage containers. Pulling pre-built images from NGC may allow you to skip the build time, but I haven't tried it myself.

> 2024-10-13. Isaac ROS v3.1.
