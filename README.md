# ios.mini.cmake

!!!DEPRECATED, moved to https://github.com/yasio/yasio/blob/dev/1k/ios.cmake

## Why ios.mini.cmake
This mini ios toolchain file fix follow issues:  
- Fix try_compile failed when build arm dylib or dynamcic framework
- Fix compile failed with armv7 deployment target >= 11.0, xcode clang will report follow error:  
```clang: error: invalid iOS deployment version '--target=armv7-apple-iosxx.x```

## Why not [ios-cmake](https://github.com/leetal/ios-cmake) toolchain
- It disable restrict try_compile, yes it will allow cmake generate xcode project file succeed with arm deploy target, but it not correct for every project with cmake build system
- It will lead static library detect platform library which not exists and cause link error whe use the library
- It will lead dynamic library link failed with incorrect platform libraries detect
