# Isaac Lab Discussions

This page contains paraphrased discussions that may be useful for future reference. Also note that these discussions are searchable from the search bar in the website.

For issues related to this page, please [open a GitHub issue](https://github.com/j3soon/robotics-notes/issues).

## Objects Penetration Issue

Q: When using soft body simulation in Isaac Lab, the objects may penetrate into each other depending on the simulation parameters. Is there a way to prevent this?

A: This may be due to objects moving too fast, meshes being too thin, or etc. You can [decrease `dt`](https://isaac-sim.github.io/IsaacLab/main/source/api/lab/isaaclab.sim.html#isaaclab.sim.SimulationCfg.dt) in Isaac Lab to make it less sensitive to these issues.

Related:

- [Contact penetration](https://github.com/isaac-sim/IsaacLab/discussions/1721)
- [Legged Robot Foot Contact Penetration](https://github.com/isaac-sim/IsaacLab/issues/1898)
- [Interpenetration between shadow hand and rigid body during interaction](https://github.com/isaac-sim/IsaacLab/issues/1515)
- [Objects penetrating each other - Collision Physics Issue in Nvidia Isaac Sim](https://forums.developer.nvidia.com/t/objects-penetrating-each-other-collision-physics-issue-in-nvidia-isaac-sim/269387)

> 2025-03-02. Isaac Lab v2.0.1.

## Deformable Body Mass

Q: Modifying the density of a soft body doesn't seem to affect the mass of the body. Is this expected?

A: Modifying [DeformableBodyMaterialCfg.density](https://isaac-sim.github.io/IsaacLab/main/source/api/lab/isaaclab.sim.spawners.html#isaaclab.sim.spawners.materials.DeformableBodyMaterialCfg.density) can affect the mass of the deformable body. However, it may not be easily observable depending on the simulation environment. For an example, take [the deformable body example](https://isaac-sim.github.io/IsaacLab/main/source/tutorials/01_assets/run_deformable_object.html), and [add a `density` field to the `DeformableBodyMaterialCfg`](https://github.com/isaac-sim/IsaacLab/blob/4868e19c1df21715d6f58c03578d2ea0f29c7561/scripts/tutorials/01_assets/run_deformable_object.py#L68) and set it to `1` and then `1000`. You should see the mass of the deformable body changes. Alternatively, you can use the [Mass API](https://github.com/isaac-sim/IsaacLab/blob/4868e19c1df21715d6f58c03578d2ea0f29c7561/source/isaaclab/test/sim/test_spawn_meshes.py#L141-L147) instead of the `density` field.

> 2025-03-02. Isaac Lab v2.0.1.

## Fluid Simulation

Q: How can I add fluid simulation to my scene in Isaac Lab?

A: It is possible to [add fluid simulation](https://youtu.be/eMyroevX1nA) in Isaac Sim through `Particle Sampler`. However, I'm not sure if the fluid/liquid/cloth/particle simulation is possible in Isaac Lab. See the [Cloth and Fluid Simulation API tracker](https://github.com/isaac-sim/IsaacLab/issues/2004) for more details.

Related:

- [Checklist of environments to add to the framework](https://github.com/isaac-sim/IsaacLab/issues/748)
- [Liquid manipulation task does not update](https://github.com/isaac-sim/IsaacLab/discussions/509)
- [Particle reset](https://github.com/isaac-sim/IsaacLab/discussions/1120)
- [Resetting a Cloth object (or any custom object outside of SceneCfg)](https://github.com/isaac-sim/IsaacLab/discussions/1105)
- [Deformable Object Simulation Capability](https://github.com/isaac-sim/IsaacLab/discussions/587)

> 2025-03-02. Isaac Lab v2.0.1.

## PhysX Error: Patch Buffer Overflow Detected

Q: I'm getting the following error when running the simulation:

```
[Error] [omni.physx.plugin] PhysX error: Patch buffer overflow detected, please increase its size to at least 503808 in the scene desc!
```

A: Increase the value of `gpu_max_rigid_patch_count` (such as `2**24`) in [simulation_cfg.py](https://github.com/isaac-sim/IsaacLab/blob/a520a883ce996d855cc9d5255d71fd1c1307633f/source/extensions/omni.isaac.lab/omni/isaac/lab/sim/simulation_cfg.py#L113).

Related:

- [[Question] Is there a solution for the Patch buffer overflow error?](https://github.com/isaac-sim/IsaacLab/issues/931)
- [How to resolve this error: “Patch buffer overflow detected”](https://forums.developer.nvidia.com/t/how-to-resolve-this-error-patch-buffer-overflow-detected/276511)
- [[Question] PhysX Error: Material Limit and Buffer Overflow Issues with High Agent Counts in IsaacLab](https://github.com/isaac-sim/IsaacLab/issues/941)

> 2025-05-29. Isaac Lab v1.x.
