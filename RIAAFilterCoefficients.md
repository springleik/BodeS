# Using BodeS to Plot an RIAA Filter

When playing vinyl records on a turntable, one must remember that manufacturers use equalization when recording to optimize dynamic range and headroom. This pre-emphasis curve is defined by the Recording Industry Association of America (RIAA) as a transfer function with three time constants.

$$H(s) = \frac{\left(sT_1+1\right)\left(sT_3+1\right)}{\left(sT_2+1\right)}

On playback, one can then invert the transfer function to implement a de-emphasis filter, recovering the original sound with optimized dynamic range and headroom.

$$H(s) = \frac{\left(sT_2+1\right)}{\left(sT_1+1\right)\left(sT_3+1\right)}
