BIN = lens
CXX = g++
CXXFLAGS = -std=c++11 -g -Wall -O2

plot: clean_dat $(BIN)
	./$(BIN) > /dev/null
	gnuplot plotFDTD.gp -

build: $(BIN)

run: clean_dat $(BIN)
	./$(BIN) 

$(BIN): FDTD.cpp
	$(CXX) $(CXXFLAGS) FDTD.cpp -o $(BIN) 

clean_dat:
	rm -Rf FDTD.dat

clean: clean_dat
	rm -Rf $(BIN)
