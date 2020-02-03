# RawLIFreader
Reading the raw data from a Leica lif-file in Matlab for further analysis.
Adapted from [bioformats](https://github.com/ome/bioformats/blob/develop/components/formats-gpl/src/loci/formats/in/LIFReader.java). In almost all cases bioformats will be a lot more user friendly than the RawLIFreader, but sometimes you need fast access to the bytes directly.

```
LF = LIFfile(filename); %read the content of the .lif file
dat=LF.getLIFBinaryBlockData('MemBlock_6122'); %contains raw data. Find the name of the memoryblock in LF.binaryBlockHeaders
