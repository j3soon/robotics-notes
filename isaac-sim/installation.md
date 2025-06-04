# Isaac Sim Installation

We assume you're using an Ubuntu x86 system.

## System Requirements

Check if your system meets the [system requirements](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/requirements.html):

```sh
cd ~/Downloads
wget https://download.isaacsim.omniverse.nvidia.com/isaac-sim-comp-check%404.5.0-rc.6%2Brelease.675.f1cca148.gl.linux-x86_64.release.zip
mkdir ~/isaac-sim-comp-check
unzip "isaac-sim-comp-check@4.5.0-rc.6+release.675.f1cca148.gl.linux-x86_64.release.zip" -d ~/isaac-sim-comp-check
cd ~/isaac-sim-comp-check
./omni.isaac.sim.compatibility_check.sh
```

## Installation

Download Isaac Sim by following the [Workstation Installation Guide](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/install_workstation.html).

```sh
cd ~/Downloads
wget https://download.isaacsim.omniverse.nvidia.com/isaac-sim-standalone%404.5.0-rc.36%2Brelease.19112.f59b3005.gl.linux-x86_64.release.zip
unzip "isaac-sim-standalone@4.5.0-rc.36+release.19112.f59b3005.gl.linux-x86_64.release.zip" -d ~/isaacsim
mkdir ~/isaacsim
cd ~/isaacsim
./post_install.sh
./isaac-sim.selector.sh
```

## WebRTC Streaming Client

Start [Isaac Sim WebRTC streaming](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/manual_livestream_clients.html#isaac-sim-short-webrtc-streaming-client):

```sh
cd ~/isaacsim
./isaac-sim.streaming.sh
```

Wait until seeing the following message:

```
Isaac Sim Full Streaming App is loaded.
```

Download and run the [WebRTC Streaming Client](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/manual_livestream_clients.html):

```sh
cd ~/Downloads
wget https://download.isaacsim.omniverse.nvidia.com/isaacsim-webrtc-streaming-client-1.0.6-linux-x64.AppImage
./isaacsim-webrtc-streaming-client-1.0.6-linux-x64.AppImage
```

## Alternatives

- [Install Isaac Sim with Pip](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/install_python.html)  
  Integration with Jupyter Notebook, Visual Studio Code, and Anaconda are available.
- [Install Isaac Sim with Docker](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/install_container.html)  
  Consider checking out [docker-isaac-sim](https://tutorial.j3soon.com/robotics/docker-isaac-sim/) for more details.
- [Install Isaac Sim on Cloud](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/install_cloud.html)
- [Install Isaac Sim with ROS Support](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/install_ros.html)  

## FAQ

- [Setup Tips \| Isaac Sim Documentation](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/install_faq.html)
- [Linux Troubleshooting \| Omniverse Developer Guide](https://docs.omniverse.nvidia.com/dev-guide/latest/linux-troubleshooting.html)
- [Robot Simulation Tips \| Isaac Sim Documentation](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/robot_simulation/robot_simulation_tips.html)
