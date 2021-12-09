
cuda-stream: CUDAStream.o main.o
	/scr0/ivan/src/llvm-project/build-clang/bin/clang++  CUDAStream.o main.o -o cuda-stream -lcpucudart -L/scr0/ivan/src/cpucuda_runtime/build/src -lm -fopenmp=libomp

CUDAStream.o:
	/scr0/ivan/src/llvm-project/build-clang/bin/clang++  -DCUDA -DMEM=DEFAULT -I../src/cuda -I../src --cuda-path=/opt/cuda-10.2/ --cuda-gpu-arch=sm_80 --cuda-host-only -I/scr0/ivan/src/llvm-project/build-clang/projects/openmp/runtime/src/ -resource-dir=/scr0/ivan/src/llvm-project/build-clang/lib/clang/14.0.0/ -fopenmp=libomp -O3 -lcpucudart -L/scr0/ivan/src/cpucuda_runtime/build/src -lm -lcpucudart -L/scr0/ivan/src/cpucuda_runtime/build/src -lm -fopenmp=libomp -arch=sm_70 --cuda-path=/opt/cuda-10.2/ --cuda-gpu-arch=sm_80 --cuda-host-only -I/scr0/ivan/src/llvm-project/build-clang/projects/openmp/runtime/src/ -resource-dir=/scr0/ivan/src/llvm-project/build-clang/lib/clang/14.0.0/ -fopenmp=libomp -O3 -lcpucudart -L/scr0/ivan/src/cpucuda_runtime/build/src -lm -lcpucudart -L/scr0/ivan/src/cpucuda_runtime/build/src -lm -fopenmp=libomp  -DNDEBUG --cuda-gpu-arch=sm_70 --cuda-path=/opt/cuda-10.2 -O3 -march=native --cuda-path=/opt/cuda-10.2/ --cuda-gpu-arch=sm_80 --cuda-host-only -I/scr0/ivan/src/llvm-project/build-clang/projects/openmp/runtime/src/ -resource-dir=/scr0/ivan/src/llvm-project/build-clang/lib/clang/14.0.0/ -c ../src/cuda/CUDAStream.cu -o CUDAStream.o
main.o:
	/scr0/ivan/src/llvm-project/build-clang/bin/clang++ -DCUDA -I../src/cuda/ -I../src/ -c ../src/main.cpp -o main.o

clean:
	rm CUDAStream.o main.o cuda-stream
