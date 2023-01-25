# CPP-PROJECT-TEMPLATE

Enter project info here


Boost::program_options is used by default

## add submodules
```
git submodule add https://github.com/author/repo third_party/repo
# clone with
git clone --recurse-submodules https://github.com/your_profile/repo
```

## build
```
cmake -S . -B_build
cmake --build _build
# or
cmake --build _build --target target
```

## testing
```
# write tests and add them to CMakeLists.txt
cmake -S . -B_build -DBUILD_TESTS=ON
cmake --build _build
cd _build && ctest
# or 
cmake --build _build --target hello_test
./_build/hello_test
```

## template todo
- [x] add gtest submodule/hunter package by default
- [x] add tests directory, example test, cmake testing instructions
- [x] add to CMakeFile.txt testing
- [ ] add github ci/travis ci
- [ ] add coverage and other tools
- [ ] add CPACK config
- [ ] add artifacts build (github)
- [ ] github branches settings
- [ ] add script for hunter update in repo
- [ ] rewrite CMakeLists.txt (as template)
- [ ] add script for deployment (project name, remove unnecessery info from readme)
