

# Guide
Stitching_detailed3.cpp is for opencv C++ version 3.4.16

Stitching_detailed4_5_5.cpp is for opencv C++ version 4.5.5

# Compile code
g++ stitching_detailed3.cpp `pkg-config opencv --cflags --libs` -o stitching_detailed3

# Run Code
To run (CPU):   
./stitching_detailed3 --try_cuda no --expos_comp no --warp plane --wave_correct no  --features surf --match_conf 0.3 ./Images/img_0.jpg ./Images/img_1.jpg ./Images/img_2.jpg ./Images/img_3.jpg ./Images/img_4.jpg ./Images/img_5.jpg ./Images/img_6.jpg ./Images/img_7.jpg ./Images/img_8.jpg ./Images/img_9.jpg --output CPU_r0-1-2-3-4-5-6-7-8-9.jpg

To run (GPU):   (need to have GPU and CUDA support):   
./stitching_detailed3 --try_cuda yes --expos_comp no --warp plane --wave_correct no  --features surf --match_conf 0.3 ./Images/img_0.jpg ./Images/img_1.jpg ./Images/img_2.jpg ./Images/img_3.jpg ./Images/img_4.jpg ./Images/img_5.jpg ./Images/img_6.jpg ./Images/img_7.jpg ./Images/img_8.jpg ./Images/img_9.jpg --output GPU_r0-1-2-3-4-5-6-7-8-9.jpg

# Check Environments
* Check opencv version: 
pkg-config --modversion opencv

* Check CUDA version: 
ls -l /usr/local | grep cuda
