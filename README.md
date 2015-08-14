# TX81Z-Patch-Degrader
This project is based on TX81Z Editor 1.0 (http://www.maxforlive.com/library/device/2202/tx81z-editor) by Jeroen Liebregts who was kind enough to share his work on maxforlive.com. 

TX81Z Patch Degrader is a Max for Live MIDI effect that chips away at patches on the Yamaha TX81Z by randomly changing (or degrading) parameters at a specified rate. What makes the process interesting is that it is possible to ramp up or down (interpolate) to the new value rather than changing it instantaneously.

The features unique to TX81Z Patch Derader are visible in the second panel of the TX81Z Patch Degrader Max MIDI effect. I’ll describe them from the top down:

1. Level bypass prevents the operator levels from being included in the degradation process so that the sound doesn’t completely die out.
2. When the interpolate switch is on new values (as long as they have an adequate range) are ramped up or down to the new value based on the rate.
3. Loop causes the degradation to continue indefinitely by reshuffling after all 73 parameters included have been degraded.
4. Free/sync toggles between changing the parameters at an arbitrary pace set by rate, or note divisions based on the project’s tempo (therefore sync will only degrade while playing)
5. Rate adjusts the rate of degradation when in free mode, and the time it takes to ramp up or down to new values when interpolate is on. Rate is milliseconds and ranges from 15ms to 2000ms.
6. Below rate are the note durations for sync mode ranging from a 1/128th note up to a dotted whole note.
7. Finally the degrade button starts the process while interrupt stops everything so when you hear something you like you can save the patch on the TX81Z.

The TX81Z has a fairly small buffer for MIDI values, so spraying values at it too quickly will generate the "MIDI Buffer Error". However, even after getting the error it will continue listening to the incoming data, so even though it might be skipping a parameter here and there it lets us keep throwing things at it.

More info:
http://audiocookbook.org/
http://audiocookbook.org/tx81z-patch-degrader-with-interpolation/
http://audiocookbook.org/vintage-fm-swapping-bricks-for-loaves-of-bread/
