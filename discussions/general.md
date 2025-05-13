# General Discussions

This page contains paraphrased discussions that may be useful for future reference. Also note that these discussions are searchable from the search bar in the website.

For issues related to this page, please [open a GitHub issue](https://github.com/j3soon/robotics-notes/issues).

## Docker Hub (`docker.io`) vs. NGC (`nvcr.io`) Docker Images

Q: What's the difference between Docker Hub and NGC Docker images?

A: I'm unsure about the actual difference, but I'll suggest sticking to NGC Docker images for simplicity if you're using NVIDIA GPUs. Since it deal with many NVIDIA dependencies for you.

For example the following CUDA images seem to be the same as they have the same hash:

- [`nvidia/cuda:12.9.0-cudnn-devel-ubuntu24.04`](https://hub.docker.com/r/nvidia/cuda/tags)
- [`nvcr.io/nvidia/cuda:12.9.0-cudnn-devel-ubuntu24.04`](https://catalog.ngc.nvidia.com/orgs/nvidia/containers/cuda/tags).

However, the PyTorch images are different and have different tags:

- [`pytorch/pytorch:2.7.0-cuda11.8-cudnn9-runtime`](https://hub.docker.com/r/pytorch/pytorch/tags)
- [`nvcr.io/nvidia/pytorch:25.04-py3`](https://catalog.ngc.nvidia.com/orgs/nvidia/containers/pytorch/tags).

To inspect what's inside the NGC image, see the [NVIDIA Optimized Frameworks Release Notes](https://docs.nvidia.com/deeplearning/frameworks/index.html#optimized-frameworks-release-notes).

Related:

- [PyTorch: NVIDIA NGC image or Docker Hub image?](https://stackoverflow.com/q/62978545)
- [Official Docker Image \| PyTorch Forums](https://discuss.pytorch.org/t/official-docker-image/4159)

> 2025-05-14.
