# AmbisonicRoomEncoding

Plug-ins used: [sparta_ambiRoomSim](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambiroomsim), [sparta_ambiBIN](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambibin),
[sparta_ambiDEC](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambidec).
Optional: [FdnReverb](https://plugins.iem.at/docs/plugindescriptions/#fdnreverb) (external: from the [IEM plug-in suite](https://plugins.iem.at/))

The sparta_ambiRoomSim.RPP example project is configured to use the **sparta_ambiRoomSim** plugin to encode mono input signals into Ambisonic signals, along with modelling room reflections corresponding to a shoe-box shaped geometry. The simulated Ambisonic signals are then decoded to headphones using the **sparta_ambiBIN** plugin, or to loudspeakers using the **sparta_ambiDEC** plugin.

Note that the **sparta_ambiRoomSim** plugin only models the early reflections, up to a specified reflection order.
Optionally, the **FdnReverb** plugin from the IEM suite may also be used to model late/diffuse reverb. By default, the FDN track is muted, but if you have the plugin installed, then try unmuting the track and adjusting the balance :-) 
