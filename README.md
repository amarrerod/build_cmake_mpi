# Github Action template for building custom CMake and MPI Projects in Github.


[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/tterb/atomic-design-ui/blob/master/LICENSEs)


## Authors

- [@amarrerod](https://www.github.com/amarrerod)


## Usage/Examples

```yaml
name: Build

on:
  push:
    branches: "**"
  pull_request:

env:
  # Customize the CMake build type here (Release, Debug, RelWithDebInfo, etc.)
  BUILD_TYPE: Release

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      
      - name: Build Project
        uses: amarrerod/build_cmake_mpi@master
        with:
          variant: env.BUILD_TYPE   
```
