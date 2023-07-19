cmake_minimum_required(VERSION 3.10)

# set the project name
project(PolybenchC VERSION 4.2.1)

set(CMAKE_C_STANDARD 17)
set(CMAKE_C_STANDARD_REQUIRED True)

add_executable(covariance datamining/covariance/covariance.c utilities/polybench.c)
target_include_directories(covariance PRIVATE utilities)
target_link_libraries(covariance PRIVATE m)

add_executable(correlation datamining/correlation/correlation.c utilities/polybench.c)
target_include_directories(correlation PRIVATE utilities)
target_link_libraries(correlation PRIVATE m)

add_executable(lu linear-algebra/solvers/lu/lu.c utilities/polybench.c)
target_include_directories(lu PRIVATE utilities)
target_link_libraries(lu PRIVATE m)

add_executable(cholesky linear-algebra/solvers/cholesky/cholesky.c utilities/polybench.c)
target_include_directories(cholesky PRIVATE utilities)
target_link_libraries(cholesky PRIVATE m)

add_executable(gramschmidt linear-algebra/solvers/gramschmidt/gramschmidt.c utilities/polybench.c)
target_include_directories(gramschmidt PRIVATE utilities)
target_link_libraries(gramschmidt PRIVATE m)

add_executable(durbin linear-algebra/solvers/durbin/durbin.c utilities/polybench.c)
target_include_directories(durbin PRIVATE utilities)
target_link_libraries(durbin PRIVATE m)

add_executable(trisolv linear-algebra/solvers/trisolv/trisolv.c utilities/polybench.c)
target_include_directories(trisolv PRIVATE utilities)
target_link_libraries(trisolv PRIVATE m)

add_executable(ludcmp linear-algebra/solvers/ludcmp/ludcmp.c utilities/polybench.c)
target_include_directories(ludcmp PRIVATE utilities)
target_link_libraries(ludcmp PRIVATE m)

add_executable(syr2k linear-algebra/blas/syr2k/syr2k.c utilities/polybench.c)
target_include_directories(syr2k PRIVATE utilities)
target_link_libraries(syr2k PRIVATE m)

add_executable(gemm linear-algebra/blas/gemm/gemm.c utilities/polybench.c)
target_include_directories(gemm PRIVATE utilities)
target_link_libraries(gemm PRIVATE m)

add_executable(gemver linear-algebra/blas/gemver/gemver.c utilities/polybench.c)
target_include_directories(gemver PRIVATE utilities)
target_link_libraries(gemver PRIVATE m)

add_executable(syrk linear-algebra/blas/syrk/syrk.c utilities/polybench.c)
target_include_directories(syrk PRIVATE utilities)
target_link_libraries(syrk PRIVATE m)

add_executable(gesummv linear-algebra/blas/gesummv/gesummv.c utilities/polybench.c)
target_include_directories(gesummv PRIVATE utilities)
target_link_libraries(gesummv PRIVATE m)

add_executable(trmm linear-algebra/blas/trmm/trmm.c utilities/polybench.c)
target_include_directories(trmm PRIVATE utilities)
target_link_libraries(trmm PRIVATE m)

add_executable(symm linear-algebra/blas/symm/symm.c utilities/polybench.c)
target_include_directories(symm PRIVATE utilities)
target_link_libraries(symm PRIVATE m)

add_executable(bicg linear-algebra/kernels/bicg/bicg.c utilities/polybench.c)
target_include_directories(bicg PRIVATE utilities)
target_link_libraries(bicg PRIVATE m)

add_executable(mvt linear-algebra/kernels/mvt/mvt.c utilities/polybench.c)
target_include_directories(mvt PRIVATE utilities)
target_link_libraries(mvt PRIVATE m)

add_executable(atax linear-algebra/kernels/atax/atax.c utilities/polybench.c)
target_include_directories(atax PRIVATE utilities)
target_link_libraries(atax PRIVATE m)

add_executable(3mm linear-algebra/kernels/3mm/3mm.c utilities/polybench.c)
target_include_directories(3mm PRIVATE utilities)
target_link_libraries(3mm PRIVATE m)

add_executable(doitgen linear-algebra/kernels/doitgen/doitgen.c utilities/polybench.c)
target_include_directories(doitgen PRIVATE utilities)
target_link_libraries(doitgen PRIVATE m)

add_executable(2mm linear-algebra/kernels/2mm/2mm.c utilities/polybench.c)
target_include_directories(2mm PRIVATE utilities)
target_link_libraries(2mm PRIVATE m)

add_executable(nussinov medley/nussinov/nussinov.c utilities/polybench.c)
target_include_directories(nussinov PRIVATE utilities)
target_link_libraries(nussinov PRIVATE m)

add_executable(floyd-warshall medley/floyd-warshall/floyd-warshall.c utilities/polybench.c)
target_include_directories(floyd-warshall PRIVATE utilities)
target_link_libraries(floyd-warshall PRIVATE m)

add_executable(deriche medley/deriche/deriche.c utilities/polybench.c)
target_include_directories(deriche PRIVATE utilities)
target_link_libraries(deriche PRIVATE m)

add_executable(jacobi-1d stencils/jacobi-1d/jacobi-1d.c utilities/polybench.c)
target_include_directories(jacobi-1d PRIVATE utilities)
target_link_libraries(jacobi-1d PRIVATE m)

add_executable(fdtd-2d stencils/fdtd-2d/fdtd-2d.c utilities/polybench.c)
target_include_directories(fdtd-2d PRIVATE utilities)
target_link_libraries(fdtd-2d PRIVATE m)

add_executable(jacobi-2d stencils/jacobi-2d/jacobi-2d.c utilities/polybench.c)
target_include_directories(jacobi-2d PRIVATE utilities)
target_link_libraries(jacobi-2d PRIVATE m)

add_executable(seidel-2d stencils/seidel-2d/seidel-2d.c utilities/polybench.c)
target_include_directories(seidel-2d PRIVATE utilities)
target_link_libraries(seidel-2d PRIVATE m)

add_executable(heat-3d stencils/heat-3d/heat-3d.c utilities/polybench.c)
target_include_directories(heat-3d PRIVATE utilities)
target_link_libraries(heat-3d PRIVATE m)

add_executable(adi stencils/adi/adi.c utilities/polybench.c)
target_include_directories(adi PRIVATE utilities)
target_link_libraries(adi PRIVATE m)
