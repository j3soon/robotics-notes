# Deprecated Components

This page lists components in robotics that are no longer actively maintained or supported. This includes components that are deprecated, have reached End-of-Life (EOL), or have been rebranded under different names. The information here helps users migrate from legacy systems to currently supported alternatives.

## Omniverse Launcher

[Omniverse Launcher](https://docs.omniverse.nvidia.com/launcher/latest/overview.html) and legacy tools [will be deprecated on October 1, 2025](https://developer.nvidia.com/omniverse/legacy-tools).

> Launcher will be deprecated on October 1, 2025.
>
> -- [NVIDIA Omniverse Launcher](https://developer.nvidia.com/omniverse/legacy-tools)

Please [migrate](https://developer.nvidia.com/omniverse/legacy-tools) accordingly:

- [Applications](https://developer.nvidia.com/omniverse/legacy-tools#ii4jrq): Applications previously available on Omniverse Launcher [falls into the following categories](https://developer.nvidia.com/omniverse/legacy-tools#ii4jrq):
  - Applications still available for download and will continue to be supported. This includes: Blender 4.2 Alpha USD Branch (as [add-on hosted on GitHub](https://github.com/NVIDIA-Omniverse/blender_omniverse_addons)), Isaac Sim (as [executable binaries](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/download.html), [pip package](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/install_python.html), or [docker image](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/install_container.html) on [NGC Catalog](https://catalog.ngc.nvidia.com/orgs/nvidia/containers/isaac-sim)), NVIDIA RTX Remix (on [NVIDIA App](https://github.com/NVIDIAGameWorks/rtx-remix)), Omniverse External Application Template (in [kit-app-template](https://github.com/NVIDIA-Omniverse/kit-app-template)), Omniverse Kit (in [kit-app-template](https://github.com/NVIDIA-Omniverse/kit-app-template)), Omniverse Farm Agent (on [NGC Catalog](https://catalog.ngc.nvidia.com/orgs/nvidia/teams/omniverse/containers/farm-agent-k8s)), Omniverse Farm Queue (on [NGC Catalog](https://catalog.ngc.nvidia.com/orgs/nvidia/teams/omniverse/containers/farm-queue)), Isaac Sim Compatibility Checker (as [executable binaries](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/download.html) or on [NGC Catalog](https://catalog.ngc.nvidia.com/orgs/nvidia/containers/isaac-sim-comp-check)), Omniverse USD Composer (formerly _Omniverse Create_, in [kit-app-template](https://github.com/NVIDIA-Omniverse/kit-app-template)), Omniverse USD Explorer (in [kit-app-template](https://github.com/NVIDIA-Omniverse/kit-app-template)), USDView (in [kit-app-template](https://github.com/NVIDIA-Omniverse/kit-app-template) as _USD Viewer_).
  - Applications available for download but will no longer be supported. This includes: Omniverse Nucleus Cache, Omniverse Drive Beta, Omniverse Nucleus Navigator, Omniverse Nucleus Workstation, Omniverse Nucleus Wrapp.
  - Applications no longer available for download and are no longer supported. This includes: Bentley LumenRT, Omniverse Create XR, Omniverse Code, Omniverse Kaolin, Omniverse Machinima Beta, Omniverse Marbles RTX, Omniverse Mineways, Omniverse Showroom, Omniverse USD Presenter (formerly _Omniverse View_).
- [Connectors](https://developer.nvidia.com/omniverse/legacy-tools#izitqj): Connectors previously available on Omniverse Launcher can [continue to be downloaded](https://developer.nvidia.com/omniverse/legacy-tools#izitqj) in [NGC Catalog](https://catalog.ngc.nvidia.com/orgs/nvidia/teams/omniverse/collections/omni_connectors). They may no longer be actively developed but will receive patches as needed. This includes: Adobe Substance 3D Painter, Autodesk 3ds Max, Autodesk Alias, Autodesk Maya, Autodesk Revit, Epic Games Unreal Engine, Graphisoft Archicad, Kitware Paraview, McNeel Rhino/Grasshopper, PTC Creo, SideFX Houdini, Trimble SketchUp, Unity.
- [Extensions](https://developer.nvidia.com/omniverse/legacy-tools#ivr252): Extensions previously available on Omniverse Launcher can [continue to be downloaded](https://developer.nvidia.com/omniverse/legacy-tools#ivr252) and used by developers, but are no longer supported. This includes ALPHA3D, Avataar, Avaturn, BAYA3D, Convai, Echo3D, Edge Impulse Data Ingestion, Evermotion, Fabricator, HDR Lightmap, in3D, KAEDIM, Moment Factory MPCDI, Moment Factory NDI, Motionverse, Move.AI, Nextspace, OctaneRender, PBRMax, Replica Studios, SmartCow LP-SDG, Syntway, Timedomain AI Singer, and VistoryBoard Omniverse.
- [Content](https://developer.nvidia.com/omniverse/legacy-tools#i9torf): Sample assets and projects can be found in Omniverse Documentation under [USD example datasets](https://docs.omniverse.nvidia.com/usd/latest/usd_content_samples/sample_content.html) and [downloadable content packs](https://docs.omniverse.nvidia.com/usd/latest/usd_content_samples/downloadable_packs.html).

## Isaac Orbit

[Isaac Orbit](https://isaac-orbit.github.io) is renamed to _Isaac Lab_. The [GitHub repository](https://github.com/NVIDIA-Omniverse/Orbit) is released under the [BSD 3-Clause License](https://github.com/NVIDIA-Omniverse/Orbit/blob/main/LICENSE). It also has corresponding [research paper](https://arxiv.org/abs/2301.04195) and [project page](https://isaac-orbit.github.io/).

> Orbit will continue to evolve as Isaac Lab to become an even lighter application on Isaac Sim for robot learning.
>
> -- [Isaac Orbit](https://isaac-orbit.github.io)

> Isaac Lab will be replacing previously released frameworks for robot learning and reinforcement learning, including [IsaacGymEnvs](https://github.com/isaac-sim/IsaacGymEnvs) for the [Isaac Gym Preview Release](https://developer.nvidia.com/isaac-gym), [OmniIsaacGymEnvs](https://github.com/isaac-sim/OmniIsaacGymEnvs) for Isaac Sim, and [Orbit](https://isaac-orbit.github.io/orbit/index.html) for Isaac Sim.
>
> -- [NVIDIA Isaac Lab](https://docs.omniverse.nvidia.com/isaacsim/latest/isaac_lab_tutorials/index.html#deprecated-frameworks)

Please [migrate](https://isaac-sim.github.io/IsaacLab/main/source/migration/migrating_from_orbit.html) to [Isaac Lab](https://isaac-sim.github.io/IsaacLab/main/index.html).

## (Omniverse) Isaac Gym

[(Omniverse) Isaac Gym](https://github.com/isaac-sim/OmniIsaacGymEnvs) is the predecessor of Isaac Lab. The GitHub repository is named as Omniverse Isaac Gym Environments (OmniIsaacGymEnvs, abbreviated as OIGE), and is released under the [BSD 3-Clause License](https://github.com/isaac-sim/OmniIsaacGymEnvs/blob/main/LICENSE.txt).

The latest release of Omniverse Isaac Gym is 4.0.0, and [will not be updated further](https://github.com/isaac-sim/OmniIsaacGymEnvs).

> Version 4.0.0 will be the last release of OmniIsaacGymEnvs. Moving forward, OmniIsaacGymEnvs will be merging with IsaacLab (https://github.com/isaac-sim/IsaacLab).
>
> -- [NVIDIA Omniverse Isaac Gym](https://github.com/isaac-sim/OmniIsaacGymEnvs)

Please [migrate](https://isaac-sim.github.io/IsaacLab/main/source/migration/migrating_from_omniisaacgymenvs.html) to [Isaac Lab](https://isaac-sim.github.io/IsaacLab/main/index.html).

## Isaac Gym (Preview Release)

[Isaac Gym (Preview Release)](https://developer.nvidia.com/isaac-gym) is the predecessor of (Omniverse) Isaac Gym that does not base on Isaac Sim (and Omniverse). The GitHub repository is named as Isaac Gym Environments ([IsaacGymEnvs](https://github.com/NVIDIA-Omniverse/IsaacGymEnvs), abbreviated as IGE), and is released under the [BSD 3-Clause License](https://github.com/NVIDIA-Omniverse/IsaacGymEnvs/blob/main/LICENSE.txt). The documentation is provided in an offline form that can be accessed after download, and has been unofficially hosted [here](https://docs.robotsfan.com/isaacgym/index.html). It also has corresponding [research paper](https://arxiv.org/abs/2108.10470), [project page](https://sites.google.com/view/isaacgym-nvidia), and [YouTube videos](https://youtu.be/nleDq-oJjGk?list=PLq2Xfjf6QzkrgDkQdtEzlnXeUAbTPEXNH).

The latest release of Isaac Gym (Preview Release) is Preview 4, and [will not be updated further](https://developer.nvidia.com/isaac-gym).

> Isaac Gym - Now Deprecated
>
> Note: This is legacy software. Developers may download and continue to use it, but it is no longer supported.
>
> -- [NVIDIA Isaac Gym](https://developer.nvidia.com/isaac-gym)

Please [migrate](https://isaac-sim.github.io/IsaacLab/main/source/migration/migrating_from_isaacgymenvs.html) to [Isaac Lab](https://isaac-sim.github.io/IsaacLab/main/index.html).

## Isaac SDK

[Isaac SDK](https://developer.nvidia.com/isaac-sdk) is the predecessor of Isaac ROS. It also has a corresponding [blog post](https://developer.nvidia.com/blog/introducing-isaac-sdk-2020-1/). Isaac SDK consists of Isaac GEMs and Isaac Applications based on Isaac (Robotics) Engine. The Isaac Sight GUI also belongs to Isaac SDK.

> Isaac SDK has been deprecated, and Isaac is now focusing on adding gems/nodes to ROS
>
> -- [NVIDIA Forum](https://forums.developer.nvidia.com/t/missing-isaac-sim-warehouse-scene-file-and-related-isaac-sdk-documentation/223417)

Please migrate to [Isaac ROS](https://nvidia-isaac-ros.github.io/).

## Isaac AMR

[Isaac AMR](https://developer.nvidia.com/isaac/amr) 1.0 and 2.0 are predecessors of Isaac Perceptor in Isaac ROS. Isaac AMR is an extension of Isaac SDK based on the Isaac Sight UI screenshots in [the documentation](https://docs.nvidia.com/isaac/doc/extensions/navigation_stack/doc/navigation_stack_on_isaac_sim.html), and some Isaac SDK docs have been redirected to Isaac AMR docs. It has a corresponding [blog post](https://blogs.nvidia.com/blog/isaac-amr-nova-orin-autonomous-mobile-robots/).

> Yes, GXF bridge was deprecated. The AMR stack will be based on ROS going forward.
>
> -- [NVIDIA Forum](https://forums.developer.nvidia.com/t/gxf-bridge-deprecated/278607)

Please migrate to [Isaac Perceptor](https://nvidia-isaac-ros.github.io/reference_workflows/isaac_perceptor/index.html) in [Isaac ROS](https://nvidia-isaac-ros.github.io/).

## Isaac Sim Unity3D

[Isaac Sim Unity3D](https://docs.nvidia.com/isaac/archive/2020.1/doc/simulation/unity3d.html) support [has been deprecated](https://forums.developer.nvidia.com/t/no-isaac-sim-unity3d-to-download/212951). The term _Isaac Sim_ now refer to the Omniverse Kit-based version.

> Unfortunately the Unity 3D support has been deprecated, as stated also on the Isaac SIM Download page. Omniverse is now your go-to platform for Isaac simulation projects.
>
> -- [NVIDIA Forum](https://forums.developer.nvidia.com/t/no-isaac-sim-unity3d-to-download/212951)

Please migrate to [Isaac Sim](https://docs.isaacsim.omniverse.nvidia.com/latest/index.html).

## (Omniverse) Replicator Insight

[Replicator Insight](https://developer.nvidia.com/nvidia-omniverse/replicator-insight-eap) has been deprecated. The product webpage now redirects to the main Omniverse landing page, indicating it is no longer supported.

Please migrate to [Replicator](https://docs.omniverse.nvidia.com/extensions/latest/ext_replicator.html).

## ROS 1

Robot Operating System (ROS) 1 [will reach EOL on May 2025](https://wiki.ros.org/Distributions).

[ROS 1 distributions](https://wiki.ros.org/Distributions) include: Noetic Ninjemys, Melodic Morenia, Lunar Loggerhead, Kinetic Kame, Jade Turtle, Indigo Igloo, Hydro Medusa, Groovy Galapagos, Fuerte Turtle, Electric Emys, Diamondback, C Turtle, Box Turtle.

> The last ROS 1 release Noetic will go end of life on May 31st with that the ROS Wiki will also be EOL and transition to being an archive.
>
> -- [ROS 1](https://wiki.ros.org/Distributions)

Please [migrate](https://docs.ros.org/en/rolling/How-To-Guides/Migrating-from-ROS1.html) to [ROS 2](https://docs.ros.org/en/rolling/index.html) ([distros](https://docs.ros.org/en/rolling/Releases.html) such as [Humble](https://docs.ros.org/en/humble/index.html)).

## Gazebo Classic

[Gazebo Classic](https://classic.gazebosim.org/) is deprecated.

> As a convention we refer to older versions of Gazebo, those with release numbers like Gazebo 9 and Gazebo 11 as “Gazebo Classic”. Newer versions of Gazebo, formerly called “Ignition”, with lettered releases names like Harmonic, are referred to as just “Gazebo”.
>
> -- [Gazebo](https://gazebosim.org/docs/latest/gazebo_classic_migration/)

Gazebo 11 is the last major release of Gazebo.

> It is bittersweet to announce that Gazebo Classic (Gazebo11) has reached end-of-life (EOL).
>
> -- [Gazebo](https://community.gazebosim.org/)

Please [migrate](https://gazebosim.org/docs/latest/gazebo_classic_migration/) to [Gazebo](https://gazebosim.org) ([distros](https://gazebosim.org/docs/latest/releases/) such as [Harmonic](https://gazebosim.org/docs/latest/releases/)) or [Isaac Sim](https://docs.isaacsim.omniverse.nvidia.com/latest/index.html).

## Ignition

Ignition is renamed to _Gazebo_.

> Going forward, the modern robotics software collection formerly known as Ignition, is now branded Gazebo.
>
> -- [Gazebo](https://gazebosim.org/about)

Please [migrate](https://gazebosim.org/docs/latest/migration_from_ignition/) to [Gazebo](https://gazebosim.org) or [Isaac Sim](https://docs.isaacsim.omniverse.nvidia.com/latest/index.html).
