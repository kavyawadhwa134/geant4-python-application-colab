# Geant4 in Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kavyawadhwa134/geant4-python-application-colab/blob/main/geant4_python_application_colab.ipynb)

Run [Geant4](https://geant4.web.cern.ch) simulations in your browser with
[geant4-python-application](https://github.com/lobis/geant4-python-application),
with nothing to install on your own machine.

Click **Open in Colab** above, then run the cells in order:

1. **Set up conda.** Installs `condacolab`; the Colab runtime restarts once.
2. **Install the package** from [conda-forge](https://github.com/conda-forge/geant4-python-application-feedstock):

   ```bash
   !conda install -c conda-forge geant4-python-application -y
   ```

3. **Run an example.** Clones the repository and runs Geant4's B1 example
   (a tissue-and-bone phantom) in batch mode:

   ```bash
   !git clone https://github.com/lobis/geant4-python-application
   %cd geant4-python-application
   !python examples/geant4-examples/Geant4-11.4.2-examples-python/basic/B1/b1.py --batch -n 10
   ```

## Notes

- Each Colab session is a fresh environment, so no virtual environment is
  needed.
- The first run downloads Geant4's physics data (about 2 GB), which takes a
  few minutes.
- With only 10 events, B1 may report 0 keV; increase `-n` (for example
  `-n 1000`) to see energy deposited in the tissue and bone.
- Colab has no display, so the interactive Qt viewer is not available; keep
  `--batch`.

## Links

- Package: [PyPI](https://pypi.org/project/geant4-python-application/) ·
  [conda-forge](https://github.com/conda-forge/geant4-python-application-feedstock) ·
  [GitHub](https://github.com/lobis/geant4-python-application)
