# Laporan Kerja Praktek DTE FTUI Template

This is a LaTeX template for *Laporan Kerja Praktek* (Internship Report) for the *Departemen Teknik Elektro, Fakultas Teknik, Universitas Indonesia* (DTE FTUI).

This template is a modification of the original **UI Style** thesis template.

---

## Usage

### Editing Variables

The main variables for the report are located in `settings.tex`. You can change the following:
- Author name and student number (`\penulis`, `\npm`)
- Title (`\judul`, `\Judul`, `\judulInggris`)
- Supervisors (`\pembimbingUtama`, `\pembimbingHarian`)
- Dates (`\startMagang`, `\akhirMagang`)
- And other report-specific details.

### Building the Document

#### Overleaf
1. Zip the entire project folder.
2. In your Overleaf dashboard, click "New Project" and select "Upload Project".
3. Select the zipped file.
4. Set the main document to `thesis.tex` in the Overleaf file menu.

#### TeXstudio or VS Code (with LaTeX Workshop)
1. **Prerequisites:**
    - A LaTeX distribution like [MiKTeX](https://miktex.org/) (Windows), [MacTeX](http://www.tug.org/mactex/) (macOS), or [TeX Live](https://www.tug.org/texlive/) (Linux).
    - [Python](https://www.python.org/downloads/) with `pygments` installed for code highlighting: `pip install Pygments`.
2. **Setup:**
    - Open the project folder in your editor.
    - Ensure `thesis.tex` is set as the root/main document.
3. **Build:**
    - Compile the document using a `pdflatex` engine.
    - **Important:** You must enable `--shell-escape` for the `minted` package to work correctly.
    - The typical build sequence is: `pdflatex -> bibtex -> pdflatex -> pdflatex`.

### File Structure
```
.
├── .gitignore               # Specifies files for Git to ignore (e.g., compiled output)
├── Makefile                 # Automates the build process (for command-line users)
├── README.md                # This file, providing an overview of the project
├── acknowledgement.txt      # The acknowledgements section content
├── assets/                  # Directory for images and other non-text assets
│   ├── TandaTangan.png      # Placeholder image for a signature
│   └── pics/                # Directory for pictures used in the document
│       ├── creative_common.png
│       ├── makara.eps
│       └── mark.png
├── istilah.tex              # A glossary of terms
├── pustaka.bib              # Bibliography database in BibTeX format
├── settings.tex             # Main configuration: title, author, dates, etc.
├── src/                     # Source .tex files for the report's content
│   ├── 00-front_matter/     # Chapters for the front matter (abstract, TOC, etc.)
│   │   ├── 01-persetujuan.tex
│   │   ├── 02-orisinalitas.tex
│   │   ├── 03-pengesahan_sidang.tex
│   │   ├── 04-pengantar.tex
│   │   ├── 05-persetujuan_publikasi.tex
│   │   ├── 06-abstrak.tex
│   │   └── 07-abstract.tex
│   ├── 01-body/             # Chapters for the main body of the report
│   │   ├── 01-bab1.tex
│   │   ├── 02-bab2.tex
│   │   ├── 03-bab3.tex
│   │   ├── 04-bab4.tex
│   │   ├── 05-bab5.tex
│   │   ├── 06-bab6.tex
│   │   └── 99-kesimpulan.tex
│   └── 99-back_matter/      # Chapters for the back matter (appendices)
│       └── lampiran.tex
├── template_license.txt     # The license for this template
└── thesis.tex               # The main LaTeX file that assembles the document
```

---

## Original UI Style README

LaTeX configuration for report/thesis/dissertation according to [University Indonesia](http://www.ui.ac.id/) standard. Originally made by Andreas Febrian and available for download [here](http://komunitas.ui.ac.id/pg/file/andreas.febrian/read/12945/template-latex-untuk-laporan-skripsithesisdisertasi)

### Original author & contributors

Author: Andreas Febrian

Contributors:

1. Lia Sadita
2. Andre Tampubolon
3. Erik Dominikus
4. Fahrurrozi Rahman