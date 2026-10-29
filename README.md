# Equalizer APO configuration

The active configuration targets EqualizerAPO-XT with VST3 support. `config.txt` includes the Fifine T669 microphone and FiiO JH5 playback profiles.

## Plugin paths

In EqualizerAPO-XT, relative `VSTPlugin` library paths are resolved from the registered installation's `VSTPlugins` directory, not from this repository. The microphone profile uses `..\..\VSTPlugins\...`, which assumes this layout:

```text
EqualizerAPO-XT/
  current/                    # registered InstallPath
  VSTPlugins/                 # live plugin binaries
    Noise Repellent.vst3
    reagate-standalone.dll
    reacomp-standalone.dll
    LoudMax64 1.47.dll
    rnnoise_mono.dll          # retained for the commented fallback
```

On the configured machine the live plugin directory is `C:\Program Files\EqualizerAPO-XT\VSTPlugins`. The `VSTPlugins` directory in this repository contains the original tracked backups; it is not the plugin directory used by the active XT configuration. The active Noise Repellent, ReaGate and ReaComp binaries are not included in this repository and must be obtained separately from their respective developers. The currently configured Noise Repellent is version 0.4.1, with `Low Latency` and `Adaptive Noise` enabled. RNNoise remains disabled in the microphone profile.

The tracked output profiles and microphone device selectors contain device-specific Windows endpoint identifiers. Verify and update them on another machine. Windows APO registration and per-device selection are separate from this repository.
