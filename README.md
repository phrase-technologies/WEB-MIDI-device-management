# WEB-MIDI-device-management
Crowd-sourced documentation of quirks when working with MIDI.
Written with WEB MIDI in mind, but really this applies to all MIDI.
Please submit a pull request if you learn something quirky about
working with WEB-MIDI that you think may be helpful to others!

## Different Interpretations of the WEB MIDI Specification
Just because your app works correctly when testing with one keyboard
does not mean it will work correctly with all keyboards.
Here are some differences in what gets outputed by various keyboards:

### Note-Off Value
MAudio signal note off 144, whereas most devices signal it with 128

### Note-Off Velocity
Some keyboard models universally assign a velocity of `0` on note off.
Others further will assign a non-zero value.
It's not clear what these values mean, but you can't just check for `0`.

## Device Naming
Several people have reported that the manufacturer listed from 
`midiAccess` is incorrect. Examples:

- `Novation` reported as `Focusrite A.E ltd`

