ADD_LIBRARY(testtensors SHARED gsttesttensors.c )
ADD_LIBRARY(testtensorsStatic STATIC gsttesttensors.c)

TARGET_LINK_LIBRARIES(testtensors ${pkgs_LIBRARIES} nnstreamer)
TARGET_INCLUDE_DIRECTORIES(testtensors PUBLIC ${pkgs_INCLUDE_DIRS})
TARGET_COMPILE_OPTIONS(testtensors PUBLIC ${pkgs_CFLAGS_OTHER})

TARGET_LINK_LIBRARIES(testtensorsStatic ${pkgs_LIBRARIES} nnstreamer)
TARGET_INCLUDE_DIRECTORIES(testtensorsStatic PUBLIC ${pkgs_INCLUDE_DIRS})
TARGET_COMPILE_OPTIONS(testtensorsStatic PUBLIC ${pkgs_CFLAGS_OTHER})

ADD_LIBRARY(tensorscheck SHARED gsttensorscheck.c )
ADD_LIBRARY(tensorscheckStatic STATIC gsttensorscheck.c)

TARGET_LINK_LIBRARIES(tensorscheck ${pkgs_LIBRARIES} nnstreamer)
TARGET_INCLUDE_DIRECTORIES(tensorscheck PUBLIC ${pkgs_INCLUDE_DIRS})
TARGET_COMPILE_OPTIONS(tensorscheck PUBLIC ${pkgs_CFLAGS_OTHER})

TARGET_LINK_LIBRARIES(tensorscheckStatic ${pkgs_LIBRARIES} nnstreamer)
TARGET_INCLUDE_DIRECTORIES(tensorscheckStatic PUBLIC ${pkgs_INCLUDE_DIRS})
TARGET_COMPILE_OPTIONS(tensorscheckStatic PUBLIC ${pkgs_CFLAGS_OTHER})
