# Shadow4 Scripting Tutorial

Tutorial notebooks presented at the **Bay Area Light Source Joint User Meeting, 2026**, teaching beamline scientists how to take a `shadow4` export from an Oasys canvas and turn it into a parameterized, sweepable script.

## Contents

Three self-contained notebooks, built around toy beamlines of increasing complexity. Each one starts from its own Oasys Python-Script export and reads top to bottom — no cross-imports between notebooks.

| Notebook | Beamline | Teaches |
|---|---|---|
| `01_focusing_mirror.ipynb` | Single focusing mirror | Reading a shadow4 export, `retrace`, `histo2`, a through-focus scan |
| `02_monochromator.ipynb` | Plane mirror + VLS grating (PGM) | The VLS grating angle solve; scanning across photon energy |
| `03_figure_errors.ipynb` | PGM + refocusing mirror | Measured mirror figure errors; exit-slit resolving power |

```
├── 01_focusing_mirror.ipynb
├── 02_monochromator.ipynb
├── 03_figure_errors.ipynb
├── exports/    # raw Oasys Python-Script output, one per notebook
├── figures/    # canvas screenshots, plus one credited external diagram
├── data/       # measured mirror figure-error map used in Notebook 3
└── models/     # the Oasys canvas (.ows) for all three toy beamlines
```

## Setup

To install: 

```bash
git clone https://github.com/whorwhey/shadow4_scripting_tutorial.git
```

If you are also using [uv](https://docs.astral.sh/uv/) as project manageer:

```bash
cd shadow4_scripting_tutorial
uv sync
```

`uv sync` installs `shadow4` (which brings `syned`/`srxraylib` with it), `numpy`, `matplotlib`, and `jupyter`, pinned to the exact versions in `uv.lock`.

If not, you can install the [shadow4](https://github.com/oasys-kit/shadow4/) package manually by:

```bash
pip install shadow4
```
## Contact

- Wei "Francis" He — francisho@lbl.gov
- Dr. Antoine Islegen-Wojdyla — awojdyla@lbl.gov

## Acknowledgements

Beamline parameters are taken from the ALS-U COSMIC-U (7.0.1) optical design.

## License

BSD 3-Clause — see [LICENSE](LICENSE).
