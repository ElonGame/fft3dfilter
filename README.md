### fft3dfilter ###

Change log
```
FFT3DFilter v2.4 (20170608)
  - some inline asm (not all) ported to simd intrisics, helps speedup x64 mode, but some of them faster also on x86.
  - intrinsics bt=0 
  - intrinsics bt=2, degrid=0, pfactor=0
  - intrinsics bt=3 sharpen=0/1 dehalo=0/1
  - intrinsics bt=3
  - Adaptive MT settings for Avisynth+: MT_SERIALIZED for bt==0 (temporal), MT_MULTI_INSTANCE for others
  - Copy Alpha plane if exists
  - reentrancy checks against bad multithreading usage
    Note: for properly operating in MT_SERIALIZED mode in Avisynth MT, please use Avs+ r2504 or better.

FFT3DFilter v2.3 (20170221)
  - apply current avs+ headers
  - 10-16 bits and 32 bit float colorspace support in AVS+
  - Planar RGB support
  - look for libfftw3f-3.dll first, then fftw3.dll
  - inline asm ignored on x64 builds
  - pre-check: if plane to process for greyscale is U and/or V return original clip
  - auto register MT mode for avs+: MT_SERIALIZED

Previous versions by Fizick and martin53
``` 
Original Docs:
https://avisynth.org.ru/fft3dfilter/fft3dfilter.html
Project:
https://github.com/pinterf/fft3dfilter
Forum:
https://forum.doom9.org/showthread.php?t=174347



