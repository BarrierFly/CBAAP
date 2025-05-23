# Calculate Bond Angles At Particle
This *OVITO* [Python modifier](https://docs.ovito.org/python/introduction/custom_modifiers.html) outputs the angles between all pairwise combinations of bonds at one particle.

## Description
Python modifier for *OVITO* that looks up all bonds connected to the specified particle and calculates the angles between all pairwise combinations of those bonds. In other words, it returns the bond pair ids, particle triplet ids and angles for all particle triplets A--B--C that have the specified particle as center particle (B).

## Parameters 
- `center_particle` / "Compute for particle": The particle index or identifier of the central particle that all bonds are attached to.
- `mode` / "Choose particle by: Index/Identifier": Choose whether input center particle is specified by index or identifier.
- `bond_mode` / "List bonds by: Index/Identifier": Choose whether output bond pairs are listed by their index or identifier.

## Output
Likely a data table identified f"bond-angles-{self.center_particle}", with properties 'Angle' (y property), 'Particle Triplet' and 'Bond Pair'.

## Example
![Screenshot of OVITO Pro Desktop application](./Examples/CalculateBondAnglesAtParticleModifier.png)

## Installation
- OVITO Pro built-in Python interpreter
```
ovitos -m pip install --user git+https://github.com/ovito-org/CalculateBondAnglesAtParticle.git
``` 
- Standalone Python package or Conda environment
```
pip install --user git+https://github.com/ovito-org/CalculateBondAnglesAtParticle.git
```
- Please note that the `--user` tag is recommended but optional and depends on your Python installation.

## Technical information / dependencies
- Tested on OVITO version 3.9.1

## Contact
This is what the original repository said: Constanze Kalcher kalcher@ovito.org
