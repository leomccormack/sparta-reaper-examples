# AmbisonicPanningBinaural

Plug-ins used: [sparta_ambiENC](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambienc), [sparta_ambiBIN](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambibin).

This example project is configured to use the **sparta_ambiENC** plugin to encode mono input signals into seventh-order Ambisonic signals (64-channels), which are then decoded to headphones using the **sparta_ambiBIN** plug-in set to third-order decoding (i.e. only using channels 1-16). 

Things to try, in order to build some more intuition:
* Set **sparta_ambiENC** to just one input, and the decoding order in **sparta_ambiBIN** to first-order. Move the sound source around a bit, and then try setting the decoding order to seventh-order. Listen to how spatially more sharp the binaural rendering becomes.
* Different decoding methods will aim to optimise the decoding in different ways, give them all a try :-) 
