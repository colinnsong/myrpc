# 将指定路径下的所有源文件加入到需要编译的源文件列表
# aux_source_directory(. SRC_LIST)
# set(SRC_LIST userservice.cpp ../user.pb.cc)
set(SRC_LIST friendservice.cpp ../friend.pb.cc)

# 生成可执行文件server, 以及指定需要编译的源文件列表
add_executable(server ${SRC_LIST})

# 表示生成可执行文件需要链接的库文件
target_link_libraries(server protobuf myrpc)