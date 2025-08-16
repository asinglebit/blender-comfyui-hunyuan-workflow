Video tutorial:

https://www.youtube.com/watch?v=R_Mfa19yT3g

Step-by-step guide:

0. Install git, if you haven't already (you want to go for Windows/x64 Setup version): https://git-scm.com/downloads/win
1. Install Anaconda: https://www.anaconda.com/
2. Create a python 3.12 environment
3. Clone the ComfyUI repository: https://github.com/comfyanonymous/ComfyUI
4. Use `nvidia-smi` command to check your CUDA version
5. Install the NVIDIA Toolkit: https://developer.nvidia.com/cuda-toolkit-archive
6. Instead of installing the default pytorch, go here and a find version suitable for your system:  https://pytorch.org/get-started/locally/
7. The rest of the instructions you can follow here: https://docs.comfy.org/installation/manual_install#nvidia
8. Install the ComfyUI Manager Addon: https://github.com/Comfy-Org/ComfyUI-Manager
9. Install Hunyuan3DWrapper and follow instructions: https://github.com/kijai/ComfyUI-Hunyuan3DWrapper
9.1. If you need to build your own custom_rasterizer, install Visual Studio / Build Tools first: https://visualstudio.microsoft.com/downloads/
10. Import the example_workflow.png into ComfyUI and test it. You will need to install missing nodes and remap the faulty nodes to use trimesh inputs instead of mesh inputs.
11. First generation will take time, let it finish, as it downloads multiple models.
12. Install Blender: https://www.blender.org/download/
13. Install the Blender ComfyUI Addon: https://github.com/AIGODLIKE/ComfyUI-BlenderAI-node
14. Upon first run, make sure to run comfyu through the plugin, by using the Local settings, as it will create the initially missing bridge nodes. You will need to provide the path to your comfyui folder and python.exe. (You can use the `where python` command to list all of the available installations. Then you need to pick the path for your conda environment version of `python.exe`)
15. After initial run, you can disconnect the plugin, and connect in `Remote` mode by typing in `127.0.0.1` and port number `8188`
16. Recreate the Hunyuan3DWrapper example workflow within Blender and add the Blender export node in the end. Be sure to set the file format to `glb`

Have fun!
