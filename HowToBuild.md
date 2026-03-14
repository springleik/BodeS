# How to Build BodeS

The BodeS Java app can be built from source code, either in your favorite IDE or at the command line. I've had good success with both Eclipse (on Windows, Mac, and Linux) and Geany (on Linux). If building on the command line, first be sure you have a Java compiler and run-time installed. The current version of BodeS is over ten years old, so when compiling you'll get some warnings about obsolete operations, but will still create the class files. Following example is of downloading the project, and building and running BodeS in a MacOS terminal window. This process works the same way in Windows and Linux as well.

```
MarksiMac:Projects williamm$ git clone https://github.com/springleik/BodeS.git
Cloning into 'BodeS'...
remote: Enumerating objects: 30, done.
remote: Counting objects: 100% (30/30), done.
remote: Compressing objects: 100% (27/27), done.
remote: Total 30 (delta 6), reused 4 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (30/30), 69.57 KiB | 1.48 MiB/s, done.
Resolving deltas: 100% (6/6), done.

MarksiMac:Projects williamm$ cd BodeS

MarksiMac:BodeS williamm$ javac BodeS.java
Note: BodeS.java uses unchecked or unsafe operations.
Note: Recompile with -Xlint:unchecked for details.

MarksiMac:BodeS williamm$ java BodeS
usage: java -cp BodeS.jar BodeS numCoeff denCoeff [startFreq [2|3|4 [Hz|rad]]]
S-Domain Bode/Nyquist Plot v. 2.2.1;  by M. Williamsen 12/23/2014
>>Numerator: 39478412.6
Denominator: 1, 12566.37, 39478412.6
Start freq.: 100.0 Hz
MarksiMac:BodeS williamm$
```

In looking over this output I noticed that the usage text mentions a jar file which doesn't actually exist. Just type "java BodeS" and the app should run and open a new window like this:

![BodeS Window at Startup](BodeSwindow.png)

With no arguments on the command line the app defaults to a first-order low-pass filter with cut-off frequency at 1 kHz. Gain is 6 dB down and phase is -90 degrees at 1 kHz.
