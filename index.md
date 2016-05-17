---
layout: default
title: {{ site.name }}
---

# The MoMEMta project

**MoMEMta** is a software package designed in a modular way to cover the needs of the experimental analysis workflows at the LHC. MoMEMta provides working examples for the most common final states (ttbar, WW, ...). If you are expert user, be prepared to feel the freedom of configure your MEM computation at all levels.

MoMEMta is based on:

 - C++, ROOT, Lua scripting language
 - Cuba library for integration
 - External PDFs (LHAPDF by default)
 - External Matrix Element (provided with MadGraph C++ exporter)

# Get MoMEMta

## Install from source

You can get the latest release of MoMEMta on [our github repository](https://github.com/MoMEMta/MoMEMta/releases). We use `cmake` as our build system.

The following set of commands is usually enough to build MoMEMta:

```
mkdir build
cd build
cmake ..
make
sudo make install
```

Find more details [here](https://github.com/MoMEMta/MoMEMta/blob/prototype/README.md#install).

# Documentation

For more information, checkout out the MoMEMta [documentation](http://momemta.github.io/MoMEMta/).

# Our team

 - Sébastien Brochet
 - Alessia Saggio
 - Miguel Vidal
 - Sébastien Wertz

# Support and contact

Having trouble with MoMEMta? [Email us](mailto:momemta-contact@cern.ch)

---

## *Acknowledgments*

*This work would not have been possible without the help of the [MadWeight](https://cp3.irmp.ucl.ac.be/projects/madgraph/wiki/MadWeight) team*
