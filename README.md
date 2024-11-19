# fftw2.15
Old fftw code used to build GrIMP C code

This repository contains a very old version of fftw2.15. The configure process will not work on some systems (e.g., MacOS). As a result, the binaries for the individual routines needed to build the GrIMP code can be built with the script that accompanies the tar file. In many cases, the code has been compiled with the .o files, fftw/$(MACHTYPE)-$OS directories.

The tar file of the original distribution is included for completeness.  The Greenland Ice Mapping Project (GrIMP) uses floats rather than doubles. Getting the original install procedure to work accross multiple compilers with a Makefile created more than 2 decades ago is problematic. Thus, we have hardwired the fftw.h in the directory fftw2.15/fftw directly so that fftw_real is typedefed to float. 

For working with with GrIMP code, the easiest way to proceed is to cd to fftw2.15/fftw and execute a make command. 

