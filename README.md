# Operator-coupled Poisson NMF for unpaired binned spectra

Code and numerical results for *Operator-coupled Poisson NMF with acquisition-coverage diagnostics for unpaired binned spectra*.

## Setup

```bash
conda env create -f environment.yml
conda activate unpaired-binned-spectra-nmf
```

The experiments use twelve MassBank MS/MS records and the [olive–sunflower oil Raman dataset](https://doi.org/10.57745/DOGT0E). Download the Raman CSV from the dataset page, then run:

```bash
python prepare_data.py --raman PATH_TO_DOWNLOADED_CSV
```

The command downloads the specified MassBank records and checks both data sources. Source details are in [DATA_SOURCES.md](DATA_SOURCES.md). Third-party spectra are not included in this repository.

## Experiments

Run from the repository root:

```bash
python run_experiments.py --group core
python run_experiments.py --group revision
```

Use `--dry-run` to list the commands. The corresponding numerical results and script paths are listed in [reported_results](reported_results/README.md). The code is released under the MIT licence; source datasets retain their own terms.
