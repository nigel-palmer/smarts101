# SMARTS101

An interactive SMARTS pattern tester for chemistry.

Live demo: https://nigel-palmer.github.io/smarts101/

## Features

- **Real-time SMARTS matching** against a list of SMILES molecules
- **2D structure preview** of the SMARTS pattern itself
- **Substructure highlighting** — matched atoms and bonds are highlighted in each molecule image
- **Atom map labels** — `:N` labels in the SMARTS are annotated directly on the matched atoms, with a per-molecule legend showing which element each label captured
- **Colour-coded SMILES input** — each line turns green (match) or red (no match) as you type
- **Clickable SMARTS reference** — 11 categories covering atoms, bonds, ring membership, charge, logical operators, functional groups, and common ring patterns; click any token to insert it at the cursor

## Usage

Open `index.html` in a browser — no build step, no server required.

Everything runs client-side via [RDKit.js](https://github.com/rdkit/rdkit-js), loaded from the unpkg CDN.

## Hosting on GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Set source to the `main` branch, root folder (`/`).
4. Your site will be available at `https://<username>.github.io/<repo>/`.

## SMARTS quick reference

| Syntax | Meaning |
|---|---|
| `C` | Aliphatic carbon |
| `c` | Aromatic carbon |
| `[#6]` | Any carbon (by atomic number) |
| `[OH]` | Hydroxyl group |
| `[C:1]` | Carbon with atom map label 1 |
| `~` | Any bond |
| `!` | NOT |
| `,` | OR |
| `[R]` | Atom in a ring |
| `[D3]` | Atom with degree 3 |

See the in-app reference panel for the full list.

## Dependencies

- [RDKit.js](https://github.com/rdkit/rdkit-js) — cheminformatics in the browser (loaded via CDN)

## License

[GNU General Public License v3.0](LICENSE)
