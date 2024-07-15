## guide
* install `prismlauncher` (do not use binary version, as it doesnt work on arch due to some make flags) (you can also use `prismlauncher-qt5-bin`, it works but is on old qt)
* also i prefer to install `jdk17-openjdk` instead of `jre` cuz i might be programming in java, if you are a programmer too, consider this; else just install `jre17-openjdk`
* Mods for performance:
* Other mods:
* I personally recommend sildur's vibrant shaders
* if you use amd graphics you can use this as a wrapper command: `env mesa_glthread=true allow_glsl_extension_directive_midshader=true gamemoderun`
* idk if it works i found it on the web
* if you use nvidia buy amd card or change to windows idc
* they're trash
* seriously
* fuck you nvidia


<!-- CHECK THIS:
Linux Wayland Users
Type these commands in your terminal:

git clone https://github.com/ninja-/glfw.git -b wayland_fixes

cd glfw

sudo cmake --build . --target install

This will install a custom GLFW fork for Minecraft on Wayland, which provides some fixes/performance improvements.

Then, in Settings > Minecraft > Native library workarounds, check Use system installation of GLFW. -->

## Settings
* you can play with settings yourself, but i found that it is best to disable vsync and framerate cap, also set Rendering Threads to small value like 1