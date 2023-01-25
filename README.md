# CPP-PROJECT-TEMPLATE

Enter project info here

## add submodules
```
git submodule add https://github.com/author/repo third_party/repo
# clone with
git clone --recurse-submodules https://github.com/your_profile/repo
```

## Build
```
cmake -S . -B_build
cmake --build _build
# or
cmake --build _build --target target
```

## Testing
```
cmake -S . -B_build -DBUILD_TESTS=ON
cmake --build _build
cd _build && ctest
# or 
cmake --build _build --target hello_test
./_build/hello_test
```
