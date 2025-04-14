# Jetson Discussions

This page contains paraphrased discussions that may be useful for future reference. Also note that these discussions are searchable from the search bar in the website.

Please note that all Jetson modules below refers to the Developer Kit instead of custom carrier boards.

For issues related to this page, please [open a GitHub issue](https://github.com/j3soon/robotics-notes/issues).

## Jetson Orin Nano vs. Jetson Nano

Q: Is Jetson Orin Nano the same as Jetson Nano?

A: Jetson Orin Nano is not the same as Jetson Nano. Since Jetson Orin Nano is a newer model, the Jetpack version and associated packages have different versions compared to Jetson Nano.

Reference: [Jetson Modules](https://developer.nvidia.com/embedded/jetson-modules)

> 2024-10-02. Jetson Orin Nano. <!-- Ack: bautista. -->

## NVMe SSD vs. microSD Card

Q: Is it necessary to install an NVMe SSD on Jetson Orin Nano? Or is a microSD card sufficient?

A: While the optional NVMe SSD is not essential for initial experimentation, it is highly recommended for serious development. The built-in storage on Jetson Orin Nano is quite limited, and an NVMe SSD provides fast, large storage, which is particularly useful when working with containers, such as for Isaac ROS. If budget is a constraint, you can start with the internal eMMC storage and purchase an NVMe SSD later when needed. It is also worth pointing out that the external NVMe SSD [is faster](https://nvidia-isaac-ros.github.io/getting_started/hardware_setup/compute/jetson_storage.html) than the internal eMMC storage, microSD card, and USB. You can also install the operating system on the NVMe SSD.

Related:

- [Jetson Setup \| Isaac ROS](https://nvidia-isaac-ros.github.io/getting_started/hardware_setup/compute/jetson_storage.html)
- [Jetson AGX Orin + SSD \| JetsonHacks](https://youtu.be/DKI1k_aP0Qk)
- [Jetson Orin Nano + SSD \| JetsonHacks](https://youtu.be/q4fGac-nrTI)
- [Jetson Orin Nano Super + SSD \| JetsonHacks](https://youtu.be/497u-CcYvE8)
- [Jetson AGX Xavier + SSD \| JetsonHacks](https://youtu.be/x0TBTYw7HKs)

> 2024-10-02. Jetson Orin Nano. <!-- Ack: bautista. -->

## Recommended NVMe SSD Storage

Q: What is the recommended NVMe SSD storage for Jetson Orin?

A: Personally, I recommend purchasing a 1TB (or 500GB if budget is a constraint) NVMe SSD. If you are located in Taiwan, you may want to purchase them from local retailers such as PCHome or MOMO for shipping within 24 hours. In addition, if you're purchasing for a university lab or company, you may need to enter your Business ID number (統一編號) during purchase. See the following videos for recommended SSDs suggested by JetsonHacks:

References:

- [Jetson AGX Orin + SSD \| JetsonHacks](https://youtu.be/DKI1k_aP0Qk)
- [Jetson Orin Nano + SSD \| JetsonHacks](https://youtu.be/q4fGac-nrTI)
- [Jetson Orin Nano Super + SSD \| JetsonHacks](https://youtu.be/497u-CcYvE8)
- [Jetson AGX Xavier + SSD \| JetsonHacks](https://youtu.be/x0TBTYw7HKs)

> 2024-10-12. Jetson Orin Nano. <!-- Ack: bautista. -->

## LLM/VLM on Jetson AGX Orin

Q: Suggested references for running LLM/VLM on Jetson AGX Orin?

A: I recommend using the following tutorials:

References:

- [Tutorial - LLaVA \| NVIDIA Jetson AI Lab](https://www.jetson-ai-lab.com/tutorial_llava.html)
- [Tutorial - Small Language Models (SLM) \| NVIDIA Jetson AI Lab](https://www.jetson-ai-lab.com/tutorial_slm.html)

> 2024-10-20. Jetson AGX Orin. <!-- Ack: CYL. -->

## Power Supply for Jetson Orin Nano

Q: What is the recommended power supply for using Jetson Orin Nano on mobile ground robots?

A: If your mobile ground robot is large enough, you can simply use a large power bank. Personally I've tried a large enerpad AC40K with 40K mAh, and it seems to work well.

> 2024-10-23. Jetson Orin Nano. <!-- Ack: bautista. -->

## (Open Issue) Fail to Control GPIO in Jetpack 6.x

Q: See [this issue](https://forums.developer.nvidia.com/t/failed-to-setup-jetson-orin-nano-gpio-output-in-jetpack-6-x/313701).

A: This is a known issue in Jetpack 6.0, 6.1, and 6.2. Please see the following for workarounds:

References:

- [`otischung/jetson_linux_36.4`](https://github.com/otischung/jetson_linux_36.4)
- [`otischung/jetson_linux_36.4.3`](https://github.com/otischung/jetson_linux_36.4.3)
- [`jetsonhacks/jetson-orin-gpio-patch`](https://github.com/jetsonhacks/jetson-orin-gpio-patch)

> 2024-11-08. Jetson Orin Nano. <!-- Ack: [@otischung](https://github.com/otischung). -->
>
> - Jetpack 6.0 L4T 36.3.0
> - Jetpack 6.1 L4T 36.4.0
> - Jetpack 6.2 L4T 36.4.3

## Memory Size of Jetson Orin Nano Super

Q: How much memory does the Jetson Orin Nano Super have?

A: The Jetson Orin Nano Super has 8GB of memory (i.e., software upgrade of Jetson Orin Nano 8GB). See the official response:

> The Jetson Orin Nano Super has no physical hardware and package differences compared to the Jetson Orin Nano Developer Kit. The performance upgrade comes from software optimization. Existing Jetson Orin Nano Developer Kit users can experience this performance boost with just a software update.
>
> -- [Jetson FAQ](https://developer.nvidia.com/embedded/faq#differences-orin-nano-and-orin-nano-super-devkits)

Reference:

- [Jetson Orin Nano Super Datasheet](https://nvdam.widen.net/s/zkfqjmtds2/jetson-orin-datasheet-nano-developer-kit-3575392-r2)

> 2025-04-01. Jetson Orin Nano (Super). <!-- Ack: Anita. -->
