# Cleaning Protein Structure Files

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/ImperialCollegeLondon/pdb-cleaning?quickstart=1)

This repository is the starting point for the Cleaning Protein Structure Files project in the ECRI Research Computing and Data Science hackathon. The project instructions are on the [hackathon wiki](https://github.com/ImperialCollegeLondon/prices/wiki/Projects).

## Quickstart

Open a Codespace with the button above, which has everything set up already. Or, with Python 3.10 or later and Git:

```bash
git clone https://github.com/ImperialCollegeLondon/pdb-cleaning.git
cd pdb-cleaning
python -m venv .venv
source .venv/bin/activate
python -m pip install -e ".[dev]"
```

## Data

The folder `data/raw` contains five files downloaded from the [RCSB Protein Data Bank](https://www.rcsb.org) on 19 October 2026. Data from the Protein Data Bank is free to use under the [CC0 licence](https://www.rcsb.org/pages/usage-policy).

| File | Structure |
|---|---|
| `1EJG.pdb` | Crambin, a small plant protein |
| `1D3Z.pdb` | Ubiquitin |
| `4HHB.pdb` | Human deoxyhaemoglobin |
| `2G5C.pdb` | Prephenate dehydrogenase from *Aquifex aeolicus* |
| `2G5C.cif` | The same structure in the newer mmCIF format |

## The PDB Format

A PDB file is a plain text file in which every line is a record of 80 characters, and the first six characters give the record type. The atoms of the structure are in `ATOM` records, and atoms which aren't part of a standard protein or nucleic acid chain, such as water and ligands, are in `HETATM` records. The full description of the format is in the [PDB File Format guide](https://www.wwpdb.org/documentation/file-format-content/format33/v3.3.html), and the atom records are described in [section 9](https://www.wwpdb.org/documentation/file-format-content/format33/sect9.html).
