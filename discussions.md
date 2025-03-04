# Discussions

This page contains paraphrased discussions that may be useful for future reference. Also note that these discussions are searchable from the search bar in the website.

For issues related to this page, please [open a GitHub issue](https://github.com/j3soon/robotics-notes/issues).

## Arrow Gizmo on the Xform Icon

Q: What do the orange and blue arrows on the Xform icon in Isaac Sim GUI mean?

A: Xform without any gizmos is a normal Xform. Orange arrow gizmo indicates a USD reference, blue arrow gizmo indicates a USD payload, and the light blue `I` indicates a USD instance.

Related:

- [Reference vs Payload vs Instance?](https://docs.omniverse.nvidia.com/isaacsim/latest/isaac_FAQ.html)
- [USD Variant Authoring - Part 3: LVRPS](https://youtu.be/HXZysoTjsV8?list=PL3jK4xNnlCVfuQjmvL_p98jtLHz-Zh6Xa)

> 2025-01-22. Isaac Sim v4.5.0. Ack: Yi-Jie Du.

## Replicator Documentation in Omniverse and Isaac Sim

Q: What's the difference between the Omniverse Replicator documentation and the Isaac Sim Replicator documentation?

A: The [Omniverse Replicator documentation](https://docs.omniverse.nvidia.com/extensions/latest/ext_replicator.html) is for using Replicator directly through Omniverse Kit, without using Isaac Sim. While the [Isaac Sim Replicator documentation](https://docs.omniverse.nvidia.com/isaacsim/latest/replicator_tutorials/index.html) is for using Replicator through Isaac Sim, including examples related to robotics applications. For Isaac Sim users, I suggest directly refer to the Isaac Sim Replicator documentation, and use the Omniverse Replicator documentation as a reference for general Replicator usage.

> 2025-02-22. Isaac Sim v4.5.0. Ack: Yi-Jie Du.

## Omniverse Launcher Deprecation

Q: How can I download Isaac Sim after the Omniverse Launcher deprecation?

A: You can directly download Isaac Sim binaries from [the Isaac Sim website](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/download.html#download-isaac-sim-short). This is actually a good change for Isaac Sim users, because it allows Isaac Sim to be directly downloaded without using Omniverse Launcher, which previously requires logging in with a NVIDIA account. Alternatively, you can [install it with Pip](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/install_python.html) or [pulling the docker image](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/install_container.html).

Related:

- [Legacy Tools for Omniverse Launcher](https://developer.nvidia.com/omniverse/legacy-tools)

> 2025-02-27. Isaac Sim v4.5.0. Ack: Ren-Jie, Lu?

## GUI Mode in Isaac Sim Docker Container

Q: How can I run Isaac Sim in GUI mode in a Docker container?

A: See [docker-isaac-sim](docker-isaac-sim.md).

> 2025-02-28. Isaac Sim v4.5.0. Ack: Audrey Chung.

## GUI Mode in Ubuntu Server

Q: How can I run Isaac Sim in GUI mode on an Ubuntu server (non-desktop environment)?

A: You can use [WebRTC](https://docs.isaacsim.omniverse.nvidia.com/latest/installation/manual_livestream_clients.html) or desktop forwarding such as VNC. Make sure you have a stable internet connection between the server and the client. Otherwise, you may encounter latency (or lagging) issues.

> 2025-03-03. Isaac Sim v4.5.0. Ack: Eric Chen.

## Objects Penetration Issue

Q: When using soft body simulation in Isaac Lab, the objects may penetrate into each other depending on the simulation parameters. Is there a way to prevent this?

A: This may be due to objects moving too fast, meshes being too thin, or etc. You can [decrease `dt`](https://isaac-sim.github.io/IsaacLab/main/source/api/lab/isaaclab.sim.html#isaaclab.sim.SimulationCfg.dt) in Isaac Lab to make it less sensitive to these issues.

Related:

- [Contact penetration](https://github.com/isaac-sim/IsaacLab/discussions/1721)
- [Legged Robot Foot Contact Penetration](https://github.com/isaac-sim/IsaacLab/issues/1898)
- [Interpenetration between shadow hand and rigid body during interaction](https://github.com/isaac-sim/IsaacLab/issues/1515)
- [Objects penetrating each other - Collision Physics Issue in Nvidia Isaac Sim](https://forums.developer.nvidia.com/t/objects-penetrating-each-other-collision-physics-issue-in-nvidia-isaac-sim/269387)

> 2025-03-02. Isaac Lab v2.0.1. Ack: [@ben25000233](https://github.com/ben25000233).

## Deformable Body Mass

Q: Modifying the density of a soft body doesn't seem to affect the mass of the body. Is this expected?

A: Modifying [DeformableBodyMaterialCfg.density](https://isaac-sim.github.io/IsaacLab/main/source/api/lab/isaaclab.sim.spawners.html#isaaclab.sim.spawners.materials.DeformableBodyMaterialCfg.density) can affect the mass of the deformable body. However, it may not be easily observable depending on the simulation environment. For an example, take [the deformable body example](https://isaac-sim.github.io/IsaacLab/main/source/tutorials/01_assets/run_deformable_object.html), and [add a `density` field to the `DeformableBodyMaterialCfg`](https://github.com/isaac-sim/IsaacLab/blob/4868e19c1df21715d6f58c03578d2ea0f29c7561/scripts/tutorials/01_assets/run_deformable_object.py#L68) and set it to `1` and then `1000`. You should see the mass of the deformable body changes. Alternatively, you can use the [Mass API](https://github.com/isaac-sim/IsaacLab/blob/4868e19c1df21715d6f58c03578d2ea0f29c7561/source/isaaclab/test/sim/test_spawn_meshes.py#L141-L147) instead of the `density` field.

> 2025-03-02. Isaac Lab v2.0.1. Ack: [@ben25000233](https://github.com/ben25000233).

## Fluid Simulation

Q: How can I add fluid simulation to my scene in Isaac Lab?

A: It is possible to [add fluid simulation](https://youtu.be/eMyroevX1nA) in Isaac Sim through `Particle Sampler`. However, I'm not sure if the fluid/liquid/cloth/particle simulation is possible in Isaac Lab. See the [Cloth and Fluid Simulation API tracker](https://github.com/isaac-sim/IsaacLab/issues/2004) for more details.

Related:

- [Checklist of environments to add to the framework](https://github.com/isaac-sim/IsaacLab/issues/748)
- [Liquid manipulation task does not update](https://github.com/isaac-sim/IsaacLab/discussions/509)
- [Particle reset](https://github.com/isaac-sim/IsaacLab/discussions/1120)
- [Resetting a Cloth object (or any custom object outside of SceneCfg)](https://github.com/isaac-sim/IsaacLab/discussions/1105)
- [Deformable Object Simulation Capability](https://github.com/isaac-sim/IsaacLab/discussions/587)

> 2025-03-02. Isaac Lab v2.0.1. Ack: [@ben25000233](https://github.com/ben25000233).
