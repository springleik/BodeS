# BodeS
S-domain bode plot applet, as described at http://www.williamsonic.com/BodeNyquist/index.html

![Screen Capture](BodeS1.png "BodeS")

BodeS was originally written to be both an application program and an applet, but applets are now deprecated so the best way to launch this is as an application at the command line.  The simplest command line in a DOS Box window would look like this, where the current working directory contains the compiled class files:

```
C:\Java Projects\BodeS>java BodeS
usage: java BodeS numCoeff denCoeff [startFreq [2|3|4 [Hz|rad]]]
S-Domain Bode/Nyquist Plot v. 2.2.1;  by M. Williamsen 12/23/2014
>>Numerator: 39478412.6
Denominator: 1, 12566.37, 39478412.6
Start freq.: 100.0 Hz
```
Five optional positional arguments may be used to set BodeS parameters on opening:

* **Numerator Coefficients**  Transfer function coefficients for the polynomial in the numerator, representing a sum in powers of the Laplace variable _s_. To simplify parsing this argument, you just enter the coefficients in order from highest order to lowest, always ending with the zeroth order coefficient on the right. Leading zeros are optional, trailing zeros aren't. Coefficients are separated with commas, noting that consecutive commas count as one.
* **Denominator Coefficients**  Transfer function coefficients for the polynomial in the denominator. If several polynomials are to be multiplied to form the numerator or denominator, enclose each set of coefficients within parentheses. As a shortcut you can use a semicolon ';' to separate polynomials instead of parentheses. Operation of nested parentheses is not defined. All coefficients are real numbers which may be entered as decimal values (1.234) or using scientific notation (1.23e4).
* **Start Frequency**  Real-valued number giving the frequency at the left edge of the horizontal axis.
* **Number of Decades to Plot**  Decades of frequency in the horizontal axis.  May be either _2_, _3_, or _4_.
* **Units for Horizontal Axis**  Frequency units in the horizontal axis may be either _Hz_ or _rad_.

A typical example of using all five optional arguments might look like this:

```
C:\Java Projects\BodeS>java BodeS (1,0,1) (1,1,1) 0.1 2 rad
S-Domain Bode/Nyquist Plot v. 2.2.1;  by M. Williamsen 12/23/2014
>>Numerator: 1, 0, 1
Denominator: 1, 1, 1
Start freq.: 0.1 rad/sec
```
