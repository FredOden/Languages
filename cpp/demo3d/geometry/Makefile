ROOT=${HOME}/projects/Languages/cpp/demo3d
CPPFLAGS=-O3 -I${ROOT}/screen -I${ROOT}/geometry -I${ROOT}
.cpp.o:
	c++ ${CPPFLAGS} -c $<

all:testMatrix testRenderer

renderer.o:renderer.cpp renderer.h matrix.h angles.h vectors.h points.h column.h ../screen/color.h 


testMatrix:testMatrix.cpp matrix.h angles.h vectors.h points.h column.h ../screen/color.h
	c++ ${CPPFLAGS} -o testMatrix $<
testRenderer:testRenderer.cpp renderer.o ../screen/ansi.o matrix.h angles.h vectors.h points.h column.h renderer.h ../screen/color.h
	c++ ${CPPFLAGS} -o testRenderer $< renderer.o ../screen/ansi.o
