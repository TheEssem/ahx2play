This branch contains a hack that makes the `--render-to-wav` setting output a 4-channel WAV file. This can be useful for getting split audio stems of AHX tunes.

Note that normal playback seems to be broken (at least with SDL, I haven't tried the WinMM driver). You may need to add the `-s 100` option for proper separation.

Original readme is below.

# ahx2play
Aims to be an accurate C port of AHX 2.3d-sp3's internal replayer. \
The project contains example code in the ahx2play folder on how to interface with the API. \
This is a direct port of the original tracker source codes.

# Notes
- This player is not optimized for speed, it's optimized for accuracy and sound quality
- To compile ahx2play (the test program) on macOS/Linux, you need SDL2
- When compiling, you need to pass the driver to use as a compiler pre-processor definition (f.ex. AUDIODRIVER_WINMM, check "paula.h")
