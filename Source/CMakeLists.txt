include_directories(1DPipes)
include_directories(Act)
include_directories(Boundaries)
include_directories("Concentric Pipe")
include_directories(Connections)
include_directories(Control)
include_directories(DPF)
include_directories(Engine)
include_directories(Extern)
include_directories(Includes)
include_directories(Labels)
include_directories(Math_wam)
include_directories(ODModels)
include_directories(Output)
include_directories(Turbocompressor)
include_directories(Wrappers)
add_subdirectory(1DPipes)
add_subdirectory(Act)
add_subdirectory(Boundaries)
add_subdirectory(Connections)
add_subdirectory(Control)
add_subdirectory(Engine)
add_subdirectory(Extern)
add_subdirectory(Labels)
add_subdirectory(Math_wam)
add_subdirectory(ODModels)
add_subdirectory(Output)
add_subdirectory(Turbocompressor)
add_subdirectory(Wrappers)
add_executable(OpenWAM
  OpenWAM.cpp
  TOpenWAM.cpp
  TTimeControl.cpp
  OpenWAM.rc
)
target_link_libraries(
  OpenWAM
  1DPipes
  Act
  Boundaries
  Connections
  Control
  Engine
  Extern
  Labels
  Math_wam
  ODModels
  Output
  Turbocompressor
  Wrappers
)
