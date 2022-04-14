# 107transfert

A laboratory performs tests on new electronic components to be integrated into its last generation chipset.
Those components are entirely characterized by their transfer function, which determines frequency re-
sponse; this function processes the input frequency and computes an output frequency (caracterizing the
way the component amplifies or reduces the input frequency). The transfer functions of these components
are rational functions, i.e. fractions such as both the numerator and the denominator are polynomials:  

<p align="center">
  <img align="center" width="50%" src="function.png"/>
</p>  
<br>

## Presentation

The goal of the project is to to optimize the transfer function computations and print the frequency responses of the component for a every values in a range from 0 to 1, with a step of 0.001.

```
[107transfert]$ ./107transfert -h
USAGE
    ./107transfert [num den]*
    
DESCRIPTION
   num      polynomial numerator defined by its coefficients
   den      polynomial denominator defined by its coefficients
```
## Exemples
* We want to calculate the function below:
<p align="center">
  <img align="center" width="25%" src="exemple1.png"/>
</p>
The numerator will be: "0 * 1 * 2 * 3 * 4"  

The denominator will be: "1"
<br>
```
[107transfert]$ ./107transfert "0*1*2*3*4" "1" > file
[107transfert]$ head -n 12 file
0.000 -> 0.00000
0.001 -> 0.00100
0.002 -> 0.00201
0.003 -> 0.00302
0.004 -> 0.00403
0.005 -> 0.00505
0.006 -> 0.00607
0.007 -> 0.00710
0.008 -> 0.00813
0.009 -> 0.00916
0.010 -> 0.01020
0.011 -> 0.01125

[107transfert]$ tail file
0.991 -> 9.73282
0.992 -> 9.76223
0.993 -> 9.79171
0.994 -> 9.82126
0.995 -> 9.85087
0.996 -> 9.88056
0.997 -> 9.91031
0.998 -> 9.94014
0.999 -> 9.97003
1.000 -> 10.00000
```







