# Using BodeS to Plot an RIAA Filter

When playing vinyl records on a turntable, one must remember that manufacturers use equalization when recording to optimize dynamic range and headroom. This pre-emphasis curve is defined by the Recording Industry Association of America (RIAA) as a transfer function with three time constants. The time constants are defined as follows:

| Symbol | Value (usec) |
| ------ | ----- |
| $T_1$  | 3180  |
| $T_2$  |  318  |
| $T_3$  |   75  |

The pre-emphasis curve used for recording is defined with this second-order transfer function, having two zeros and one pole:

```math
H(s) = \frac{\left(sT_1+1\right)\left(sT_3+1\right)}{\left(sT_2+1\right)}
```

On playback, one can then invert the transfer function to implement a de-emphasis filter for playback, recovering the original sound with optimized dynamic range and headroom. This transfer function has one zero and two poles:

```math
H(s) = \frac{\left(sT_2+1\right)}{\left(sT_1+1\right)\left(sT_3+1\right)}
```
