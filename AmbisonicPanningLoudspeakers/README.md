# AmbisonicPanningLoudspeakers

Plug-ins used: [sparta_ambiENC](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambienc), [sparta_ambiDEC](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambidec), [sparta_panner](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#panner).
Optional: [sparta_binauraliser](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#binauraliser).

Here, mono signals are encoded into Ambisonics using the **sparta_ambiENC** plugin, which are then decoded to a loudspeaker array with **sparta_ambiDEC**. The same mono signals may instead also be directly panned to the same loudspeaker setup using the VBAP-based **sparta_panner**. Note that your loudspeaker setup should be programmed into each plugin. For convenience, note that you only need to do this once, since the plugins can export the loudspeaker directions as a .json file, which can then be loaded into the other SPARTA or IEM plugins.

Note that the **sparta_panner** will always produce a sharper phantom image than the **sparta_ambiENC** plus **sparta_ambiDEC** combination. However, the source width/spread will also change as the source is panned between the loudspeakers using the panner plugin. If this is not desirable, then the **sparta_panner** plugin can optionally also spread the sound sources by assigning the input signal with panning gains surrounding the specified direction. Alternatively, the Ambisonic panning, through the **sparta_ambiENC** plus **sparta_ambiDEC** combination, will also inherently introduce source spreading depending on the encoding/decoding order. This latter approach also allows e.g. spot-mics to be encoded and mixed with Ambisonic microphone array recordings, and decoded with one instance of **sparta_ambiDEC** in the same workflow.

Optionally, this example can also be listened to using headphones by un-bypassing the **sparta_binauraliser** plugin, which is attached to the master bus. Just make sure that the source directions in the binauraliser plugin match the loudspeaker directions in the decoder/panner.


