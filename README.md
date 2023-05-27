<img src="src/main/resources/assets/sodium/icon.png" width="128">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f8/Vulkan_API_logo.svg/512px-Vulkan_API_logo.svg.png?20161220132648" width="128">

### THIS PROJECT IS NOT AFFILIATED WITH SODIUM OR VULKANMOD!

# Sodium with VulkanMod support (for Fabric)
![GitHub license](https://img.shields.io/github/license/CaffeineMC/sodium-fabric.svg)
![GitHub issues](https://img.shields.io/github/issues/Skypixel-ECAS/Sodium-Vulkan.svg)
![GitHub tag](https://img.shields.io/github/tag/Skypixel-ECAS/Sodium-Vulkan.svg)

This fork works by removing/editing classes that intefere with VulkanMod
This fork will be updated as fast as possible after the mainstream Sodium



## NOTICE: VULKANMOD IS NOT EMBEDDED, YOU NEED TO DOWNLOAD IT FROM https://modrinth.com/mod/VulkanMod

Sodium is a free and open-source optimization mod for the Minecraft client that improves frame rates, reduces
micro-stutter, and fixes graphical issues in Minecraft. 

:warning: Sodium has had a lot of time to shape up lately, but the mod is still alpha software. You may run into minor
graphical issues or crashes while using it. Additionally, the
[Fabric Rendering API](https://fabricmc.net/wiki/documentation:rendering) is not yet supported, which may cause crashes
and other issues with some mods.

---

## Installation

### Manual installation (recommended)

You will need Fabric Loader 0.10.x or newer installed in your game in order to load Sodium. If you haven't installed
Fabric mods before, you can find a variety of community guides for doing so [here](https://fabricmc.net/wiki/install).


### Reporting Issues

You can report bugs and crashes by opening an issue on the [Sodium-Vulkan issue tracker](https://github.com/Skypixel-ECAS/Sodium-Vulkan/issues).
Before opening a new issue, use the search tool to make sure that your issue has not already been reported and ensure
that you have completely filled out the issue template. Issues that are duplicates or do not contain the necessary
information to triage and debug may be closed. 

Please note that while the issue tracker is open to feature requests, development is primarily focused on
improving hardware compatibility, performance, and finishing any unimplemented features necessary for parity with
the vanilla renderer.

### Building from sources

Support is not provided for setting up build environments or compiling the mod. We ask that
users who are looking to get their hands dirty with the code have a basic understanding of compiling Java/Gradle
projects. The basic overview is provided here for those familiar.

#### Requirements

- JRE 8 or newer (for running Gradle)
- JDK 8 (optional)
  - If you neither have JDK 8 available on your shell's path or installed through a supported package manager (such as
[SDKMAN](https://sdkman.io)), Gradle will automatically download a suitable toolchain from the [AdoptOpenJDK project](https://adoptopenjdk.net/)
and use it to compile the project. For more information on what package managers are supported and how you can
customize this behavior on a system-wide level, please see [Gradle's Toolchain user guide](https://docs.gradle.org/current/userguide/toolchains.html).
- Gradle 6.7 or newer (optional)
  - The [Gradle wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html#sec:using_wrapper) is provided in
    this repository can be used instead of installing a suitable version of Gradle yourself. However, if you are building
    many projects, you may prefer to install it yourself through a suitable package manager as to save disk space and to
    avoid many different Gradle daemons sitting around in memory.

#### Building with Gradle

Sodium uses a typical Gradle project structure and can be built by simply running the default `build` task. After Gradle
finishes building the project, you can find the build artifacts (typical mod binaries, and their sources) in
`build/libs`.

**Tip:** If this is a one-off build, and you would prefer the Gradle daemon does not stick around in memory afterwards,
try adding the [`--no-daemon` flag](https://docs.gradle.org/current/userguide/gradle_daemon.html#sec:disabling_the_daemon)
to ensure that the daemon is torn down after the build is complete. However, subsequent builds of the project will
[start more slowly](https://docs.gradle.org/current/userguide/gradle_daemon.html#sec:why_the_daemon) if the Gradle
daemon is not available to be re-used.


Build artifacts ending in `dev` are outputs containing the sources and compiled classes
before they are remapped into stable intermediary names. If you are working in a developer environment and would
like to add the mod to your game, you should prefer to use the `modRuntime` or `modCompile` configurations provided by
Loom instead of these outputs.

---
### License

Sodium is licensed under GNU LGPLv3, a free and open-source license. For more information, please see the
[license file](https://github.com/CaffeineMC/sodium-fabric/blob/1.16.x/dev/LICENSE.txt).

The "Nicer Fast Leaves" pack included in Sodium is by [Vanilla Tweaks](https://vanillatweaks.net/), licensed for Sodium under the GNU LGPLv3.
