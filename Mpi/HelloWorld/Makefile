F90 = mpif90
FFLAGS = -O2 -g
LDFLAGS =
LIBS = -lm

all: hello_world.exe

f08: hello_world_f08.exe

%.exe: %.o
	$(F90) $(FFLAGS) -o $@ $^ $(LDFLAGS) $(LIBS)

%.o: %.f90
	$(F90) $(FFLAGS) -c -o $@ $<

clean:
	rm -f *.o *.mod *.exe core
