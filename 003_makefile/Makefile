#伪目标 .PHONY:clean
#声明目标为伪目标之后，makefile将不会判断目标是否存在或该目标是否需要更新
.PHONY:clean show


OBJ=add.o sub.o multi.o calc.o
TARGET=calc

$(TARGET):$(OBJ)
	$(CXX) add.o sub.o multi.o calc.o -lstdc++  -o calc

#模式匹配
%.o:%.cpp
	$(CXX) -c $^ -o $@

clean:
	$(RM) *.o $(TARGET)

show:
	echo $(AS)
	echo $(CC)
	echo $(CPP)
	echo $(CXX)
	echo $(RM)

	#列出当前目录下所有的.cpp文件
	echo $(wildcard ./*.cpp)
	#将对应的.cpp替换成.o文件
	echo $(patsubst %.cpp,%.o,./*.cpp)
