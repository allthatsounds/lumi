# lumi
polyphonic midi interface to pure data
written for ROLI LUMI Keys, and tested on Linux, 
but should work for any standard MIDI device.

Prerequisites: Pure Data (0.54.1)

Usage from within pd: [lumi lowest_MIDI_channel highest_MIDI_channel synth_patch]

Usage from the command line: 
```
$pd -midiindev "2" -nogui -open lumi.pd -send ";in 24 96 cgen"
```

where 24 and 96 is the frequency range to be covered [MIDI values]
and cgen is the name of the synthesizer patch to be used for each key

the synthesizer patch should take MIDI key and velocity as an input and
route the audio signal directly to [dac~]

