# Example CUVS Project Template

This template project provides a drop-in sample to either start building a new application with, or using CUVS in an existing CMake project. 

First, please refer to our [installation docs](https://docs.rapids.ai/api/cuvs/stable/build.html#cuda-gpu-requirements) for the minimum requirements to use CUVS.

Once the minimum requirements are satisfied, this example template application can be built with the provided `build.sh` script. This is a bash script that calls the appropriate CMake commands, so you can look into it to see the typical CMake based build workflow.  

This directory (`CUVS_SOURCE/cpp/template`) can be copied directly in order to build a new application with CUVS.

CUVS can be integrated into an existing CMake project by copying the contents in the `configure rapids-cmake` and `configure cuvs` sections of the provided `CMakeLists.txt` into your project, along with `cmake/thirdparty/get_cuvs.cmake`. 

Make sure to link against the appropriate Cmake targets. Use `cuvs::cuvs` to utilize the shared library.

```cmake
target_link_libraries(your_app_target PRIVATE cuvs::cuvs)
```

