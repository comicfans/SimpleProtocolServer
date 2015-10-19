project (SimpleProtocolServer)

cmake_minimum_required(VERSION 3.3)

#add_definitions(-DUNICODE -D_UNICODE)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -mconsole -municode")

add_executable(SimpleProtocolServer
guid.cpp loopback-capture.cpp main.cpp prefs.cpp simpletcpserver.cpp)

target_link_libraries(SimpleProtocolServer ws2_32 iprop ole32 avrt winmm ksuser)
