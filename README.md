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
4. Set the main document to `laporan-kp.tex` in the Overleaf file menu.

#### TeXstudio or VS Code (with LaTeX Workshop)

1. **Prerequisites:**
    - TeX Live, installation guide [here](https://www.tug.org/texlive/windows.html).
    - LaTeX Workshop extension for VS Code.
2. **Setup:**
    - Open the project folder in your editor.
    - Ensure `laporan-kp.tex` is set as the root/main document.
3. **Build:**
    - Compile the document using a `pdflatex` engine.
    - **Important:** You must enable `--shell-escape` for the `minted` package to work correctly.
    - The typical build sequence is: `pdflatex -> bibtex -> pdflatex -> pdflatex`.

### File Structure

```plaintext
.
├── .gitignore                           # Specifies files for Git to ignore (e.g., compiled output)
├── Makefile                             # Build automation with latexmk for PDF generation
├── README.md                            # This file, providing an overview of the project
├── acknowledgement.txt                  # Template acknowledgements and contributor information
├── assets/                              # Directory for images and other non-text assets
│   ├── TandaTangan.png                  # Signature image placeholder
│   └── pics/                            # Directory for pictures used in the document
│       ├── creative_common.png
│       ├── makara.eps                   # UI logo in EPS format
│       └── mark.png
├── istilah.tex                          # Definitions of terms to be italicized or bolded (by Andreas Febrian)
├── pustaka.bib                          # Bibliography database in BibTeX format
├── settings.tex                         # Document information configuration (title, author, dates, etc.)
├── src/                                 # Source .tex files for the report's content
│   ├── 00-front_matter/                 # Front matter pages
│   │   ├── 01-persetujuan.tex           # Halaman Pengesahan (Approval page)
│   │   ├── 02-orisinalitas.tex          # Halaman Pernyataan Orisinalitas (Originality statement)
│   │   ├── 03-pengesahan_sidang.tex     # Halaman Pengesahan Laporan Kerja Praktik (Internship approval)
│   │   ├── 04-pengantar.tex             # Kata Pengantar (Preface) - content included
│   │   ├── 05-persetujuan_publikasi.tex # Halaman Persetujuan Publikasi (Publication consent)
│   │   ├── 06-abstrak.tex               # Abstrak (Indonesian abstract)
│   │   └── 07-abstract.tex              # Abstract (English abstract)
│   ├── 01-body/                         # Main content chapters
│   │   ├── 01-bab1.tex                  # Chapter 1 (includes background section)
│   │   ├── 02-bab2.tex                  # Chapter 2
│   │   ├── 03-bab3.tex                  # Chapter 3
│   │   ├── 04-bab4.tex                  # Chapter 4
│   │   ├── 05-bab5.tex                  # Chapter 5
│   │   ├── 06-bab6.tex                  # Chapter 6
│   │   └── 99-kesimpulan.tex            # Kesimpulan dan Saran (Conclusions and suggestions)
│   └── 99-back_matter/                  # Back matter
│       └── lampiran.tex                 # Appendices
├── template_license.txt                 # Creative Commons license for this template
└── laporan-kp.tex                           # Main LaTeX file - Template Laporan Kerja Praktek
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

