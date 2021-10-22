# $< : la primera dependencia
# $@ :target

#name.x: name.cpp
#%.x: %.cpp
#	g++ $< -o $@

all: fig.pdf

plantilla.x: plantilla.cpp
	g++ plantilla.cpp -o plantilla.x

datos.txt: plantilla.x
	./plantilla.x > datos.txt

fig.pdf: plot.gp datos.txt
	gnuplot $<

clean:
	rm -f a.out *.x *.txt *.pdf
