# Compilation Guide

How to compile `source/main.tex` into a print-ready PDF.

## Method 1: Overleaf (Easiest — Recommended)

No installation needed. Works in any browser.

1. Go to [overleaf.com](https://www.overleaf.com) and create a free account
2. Click **New Project → Blank Project**
3. Delete the default content in `main.tex`
4. Copy the full contents of `source/main.tex` from this repository
5. Paste into the Overleaf editor
6. Click **Recompile**
7. Click **Download PDF**

**Compile time:** ~30 seconds

---

## Method 2: Local LaTeX

**Install a LaTeX distribution first:**

| OS | Distribution | Link |
|----|-------------|------|
| Windows | MiKTeX | [miktex.org](https://miktex.org/download) |
| Mac | MacTeX | [tug.org/mactex](https://www.tug.org/mactex/) |
| Linux | TeX Live | `sudo apt-get install texlive-full` |

**Then compile:**

```bash
cd source/
pdflatex main.tex
pdflatex main.tex  # Run twice for proper formatting
```

Output: `source/main.pdf`

**Compile time:** ~2–5 seconds

---

## Method 3: Pre-Compiled PDF

Download `LA_Bike_Metro_Pocket_Guide.pdf` directly from [Releases](https://github.com/claudchagas/LA-Bike-Metro-Pocket-Guide/releases) and print without compiling.

---

## Troubleshooting

**"Package fontawesome5 not found"**
- Overleaf: reload the page (auto-installs packages)
- Local TeX Live: `tlmgr install fontawesome5`
- Local MiKTeX: open MiKTeX Console → Packages → search fontawesome5 → Install

**Text overlaps or runs off the page**
- Ensure page size is set to **Letter** (not A4) in print settings
- Compile with `pdflatex`, not `xelatex` or `lualatex`

**PDF is blank or incomplete**
- Run `pdflatex main.tex` twice (required for proper rendering)

**Compilation is very slow**
- Delete auxiliary files: `*.aux`, `*.log`, `*.out`
- Try Overleaf instead

---

## Printing

| Setting | Value |
|---------|-------|
| Paper | Letter (8.5" × 11") |
| Weight | 24–28 lb recommended |
| Color | Yes (color printer) |
| Sides | Double-sided, flip on long edge |
| Scale | 100% — do not scale |
| Quality | High |

**To fold into a pocket booklet:**
1. Print all 8 pages double-sided
2. Fold in half lengthwise (hamburger fold)
3. Result: compact 4" × 11" booklet
4. Optional: staple spine for durability