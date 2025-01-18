CXX = clang++
# Uncomment the next line and comment the above to switch to g++
# CXX = g++

# Rule to build the executable lab00Test
lab00Test: lab00Test.o tddFuncs.o arrayFuncs.o
	${CXX} lab00Test.o tddFuncs.o arrayFuncs.o -o lab00Test

# Rules for individual .o files (not strictly needed due to implicit rules)
# %.o: %.cpp
#	${CXX} -c $< -o $@

# Clean rule to remove generated files
clean:
	/bin/rm -f *.o helloWorld lab00Test

# Rule to build helloWorld for testing Makefiles
helloWorld: helloWorld.o
	${CXX} helloWorld.o -o helloWorld

helloWorld.o: helloWorld.cpp
	${CXX} -c helloWorld.cpp