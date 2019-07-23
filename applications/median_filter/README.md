Median Filter
======================

This is an optimized implementation of a median filter being used to remove noise in images targeting execution on an SDAccel supported FPGA acceleration card.

### PERFORMANCE
Board|Image Size|Frames / Second
-----|-----|-----
xilinx:adm-pcie-7v3:1ddr|128 x 128|22,222
## SUPPORTED PLATFORMS
Platform | Board             | Software Version
---------|-------------------|-----------------
xilinx_u200_qdma|Xilinx Alveo U200|SCOUT 2019.2
xilinx_u280_xdma|Xilinx Alveo U280|SCOUT 2019.2
xilinx_u250_qdma|Xilinx Alveo U250|SCOUT 2019.2
xilinx_u200_xdma|Xilinx Alveo U200|SCOUT 2019.2
xilinx_u250_xdma|Xilinx Alveo U250|SCOUT 2019.2
xilinx_u280-es1_xdma|Xilinx Alveo U280|SCOUT 2019.2


##  DESIGN FILES
Application code is located in the src directory. Accelerator binary files will be compiled to the xclbin directory. The xclbin directory is required by the Makefile and its contents will be filled during compilation. A listing of all the files in this example is shown below

```
data/goldenImage.bmp
data/inputImage.bmp
src/krnl_medianFilter.cl
src/medianFilter.cpp
```

##  COMMAND LINE ARGUMENTS
Once the environment has been configured, the application can be executed by
```
./median <krnl_median XCLBIN> ./data/inputImage.bmp ./data/goldenImage.bmp
```
