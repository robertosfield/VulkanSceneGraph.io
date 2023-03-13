![VulkanSceneGraph](https://raw.githubusercontent.com/vsg-dev/VulkanSceneGraph/master/docs/images/VSGlogo.png)

VulkanSceneGraph (VSG), is a modern, cross platform, high performance scene graph library built upon [Vulkan](https://www.khronos.org/vulkan/) graphics/compute API. The software is written in [C++17](https://en.wikipedia.org/wiki/C%2B%2B17), and follows the [CppCoreGuidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines) and [FOSS Best Practices](https://github.com/coreinfrastructure/best-practices-badge/blob/master/doc/criteria.md).  The source code is published under the [MIT License](LICENSE.md).

The project aims to bring the performance of Vulkan to the wider developer community by providing a modern, high quality software library that is easy to use and focused on making the development of high performance graphics and compute applications a productive and fun experience.  Sharing the same lead author as the OpenSceneGraph, all the lessons about software quality, performance and the needs of application developers are applied to VulkanSceneGraph to provide a distillation of what a next gen scene graph needs to be.
## Features
The VulkanSceneGraph project is comprised of the main VulkanSceneGraph library (provided by this repo) and a collection of optional libraries, each in their own dedicated repositories hosted alongside each other on [https://github.com/vsg-dev](https://github.com/vsg-dev), that provide additional features and example programs and templates for your own VulkanSceneGraph projects.

### Features provided by the core VulkanSceneGraph library are:

* Robust, thread safe memory management with custom block memory allocator and high performance smart pointers that are smaller and faster than std equivalents.
* GLSL style maths class - no need for 3rd party libs like GLM.
* Coherent Object model with easy to use and extend serialization, including native binary and ascii file support for all scene graph objects.
* C++ classes that encapsulate Vulkan Graphics and Compute C API in robust and convenient form, with robust resource management, including serialization support. Complexities and verbose setup usually associated with Vulkan are all dealt with for you so you can concentrate on your compute and graphics tasks.
* Vulkan extensions for ray tracing and mesh shading.
* Built in GLSL and SPIR-V shaders for Physics Based Rendering. phong and flat shading and text rendering.
* GLSL shader compilation to SPIR-V, using compiled in [glslang](https://github.com/vsg-dev/glslang), so users don't need to convert offline and can leverage #pragma(tic) shader composition.
* Class design focused on performance of scene graph operations by minimizing CPU bottlenecks: optimizing data density, layout, cache coherency and minimizing branching leading to better utilization of modern CPU and memory architectures. Traversals through to IO operations can be up to 10 times faster than the OpenSceneGraph.
* Optimized scene graph performance has been essential for making the most of the performance that Vulkan itself provides over OpenGL/DirectX, benchmarks on large databases show 3 to 20 X performance improvements over OpenSceneGraph/OpenGL.
* Multi-threading support at the viewer level, file loading and database paging.
* Flexible Viewer architecture built around Vulkan command recording and queue submission.
* Native windowing and event support under Windows, Linux, Android, macOS and iOS.
* Support for double matrices in Camera and Transform class providing support for large database coordinates system such as whole earth/GIS rendering whilst minimizing precision issues.
* Modern CMake build system that provides config installation alongside binaries making it easier to find and use all the appropriate build options for using the VulkanSceneGraph in your own projects.
* Minimal and complete approach to design - the whole VulkanSceneGraph interface and implementation, providing all the above functionality, takes 60 thousand lines of C++ code, compared to over 58 thousand for GLM headers, or vulkan.hpp (C++ wrapper for Vulkan) at over 94 thousand lines of code.  The VulkanSceneGraph replaces both and provides much more functionality besides.

### Features provided by companion projects:
* [vsgXchange](https://github.com/vsg-dev/vsgXchange) reading and writing of 3rd party image and 3d models and HTTP support.
* [osg2vsg](https://github.com/vsg-dev/osg2vsg) OpenSceneGraph integration library that enables converting of OSG to VSG scene graph and use of OpenSceneGraph loaders.
* [vsgImGui](https://github.com/vsg-dev/vsgImGui) ImGui integration enabling UI in graphics window.
* [vsgQt](https://github.com/vsg-dev/vsgQt) Qt integration with VulkanSceneGraph.
* [vsgUnity](https://github.com/vsg-dev/vsgUnity) plugin for Unity that provides export to native VulkanSceneGraph binary/ascii format.
* [vsgExamples](https://github.com/vsg-dev/vsgExamples) tests & examples.
* [MyFirstVsgApplication](https://github.com/vsg-dev/MyFirstVsgApplication) simple standalone VSG application that can be used as a template for your own applications.
* [vsgFramework](https://github.com/vsg-dev/vsgFramework) template project that uses CMake FetchContent to pull in all the main libraries associated with VulkanSceneGraph and dependencies and builds them together.
* [vsgSDL](https://github.com/ptrfun/vsgSDL) SDL integration with VulkanSceneGraph.
* [vsgvr](https://github.com/geefr/vsgvr) OpenVR integration with VulkanSceneGraph.

## Reference Documentation:
* [VulkanSceneGraph](ref/VulkanSceneGraph/html/annotated.html)
* [vsgXchange](ref/vsgXchange/html/annotated.html)
* [vsgImGui](ref/vsgImGui/html/annotated.html)
* [vsgQt] - TODO
* [vsgExamples](ref/vsgExmaples/html/annotated.html)

---

## Website creation links:
* [NOTES](NOTES.md)
