# AmbisonicDecoding

## Binaural examples 
### linearDecodingBinauralFOA.RPP

Plug-ins used: [sparta_ambiBIN](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambibin).

Here, first-order (FUMA) Ambisonic recordings are decoded to headphones using the **sparta_ambiBIN** plug-in.

### linearDecodingBinauralEigenmike.RPP

Plug-ins used: [sparta_array2sh](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#array2sh). [sparta_ambiBIN](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambibin).

In this example, the **sparta_array2sh** plugin is used to encode Eigenmike recordings into fourth-order Ambisonic signals, which are then decoded to headphones using the **sparta_ambiBIN** plug-in.


### parametricDecodingBinauralFOA.RPP

Plug-ins used: [sparta_ambiBIN](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambibin), [compass_binaural](https://leomccormack.github.io/sparta-site/docs/plugins/compass-suite/#binaural), [hodirac_binaural](https://leomccormack.github.io/sparta-site/docs/plugins/hodirac-suite/#binaural),
[cropac_binaural](https://leomccormack.github.io/sparta-site/docs/plugins/cropac-binaural/#plug-in-description).

Here, first-order (FUMA) Ambisonic recordings are decoded to headphones using the **sparta_ambiBIN**, or **compass_binaural**,  **hodirac_binaural**, or **cropac_binaural**.

Note that the COMPASS, HO-DirAC, and CroPaC decoders are signal-dependent, and aim to adapt the processing to be more spatially accurate. They also allow for sound-field modifications, which would not be possible with a linear decoder, such as adjusting the direct-to-diffuse balance.


## Loudspeaker examples

### linearDecodingLoudspeakersFOA.RPP

Plug-ins used: [sparta_ambiDEC](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambidec).

Here, first-order (FUMA) Ambisonic recordings are decoded to a loudspeaker array using the **sparta_ambiDEC** plug-in. Note that, for convenience, you can export the loudspeaker directions as a .json file, which can then be loaded by other SPARTA/IEM plugins, so you need only specify the directions for your specific setup once.

### linearDecodingLoudspeakersEigenmike.RPP

Plug-ins used: [sparta_array2sh](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#array2sh). [sparta_ambiDEC](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambidec).

In this example, the **sparta_array2sh** plugin is used to encode Eigenmike recordings into fourth-order Ambisonic signals, which are then decoded to a loudspeaker setup using the **sparta_ambiDEC** plug-in.

### parametricDecodingLoudspeakersEigenmike.RPP

Plug-ins used: [sparta_ambiDEC](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#ambidec), [compass_decoder](https://leomccormack.github.io/sparta-site/docs/plugins/compass-suite/#decoder), [hodirac_decoder](https://leomccormack.github.io/sparta-site/docs/plugins/hodirac-suite/#decoder).
Optional: [sparta_ambiDEC](https://leomccormack.github.io/sparta-site/docs/plugins/sparta-suite/#binauraliser).

Here, first-order (FUMA) Ambisonic recordings are decoded to headphones using the **sparta_ambiDEC**, or **compass_decoder**,  or **hodirac_decoder**.

Note that the COMPASS and HO-DirAC decoders are signal-dependent, and aim to adapt the processing to be more spatially accurate. They also allow for sound-field modifications, which would not be possible with a linear decoder, such as adjusting the direct-to-diffuse balance.

Optionally, the **sparta_binauraliser** plug-in may be un bypassed on the master bus, in order to listen to these loudspeaker decoders over headphones. 
