markdown file describing how to build BodeS

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
