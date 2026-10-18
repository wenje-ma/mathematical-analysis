# Mathematical Analysis

> Mathematical analysis lecture notes (real numbers through Fourier series) with 36 weeks of fully worked homework — the largest repository in the notes series, bilingual (Chinese/English).

## Repository structure

```
mathematical-analysis/
├── cn/
│   ├── notes.md              # Chinese lecture notes (single file, 1198 lines)
│   └── homework/
│       └── week1.md … week36.md (+ supplements)
├── en/
│   ├── notes.md              # Complete English translation (1198 lines, aligned)
│   └── homework/
│       └── week1.md … week36.md (+ supplements)
└── textbooks/
    ├── mathematical-analysis1.pdf    # Textbook Vol. I (513 pp.)
    ├── mathematical-analysis2.pdf    # Textbook Vol. II (439 pp.)
    ├── Zad-01.pdf … Zad-10.pdf       # Ten single-page problem sheets
    └── *_ocr.pdf                     # OCR copies of the above
```

## The notes

`notes.md` is a single file organized as **55 sections** with `##` headings, covering the full univariate and multivariate analysis chain:

- Real numbers · the concept of a function · limits of sequences
- Continuous functions · properties on a closed interval
- The Lagrange mean value theorem · the Taylor formula
- Supremum and infimum · uniform continuity
- The definite integral · double and triple integrals
- Line integrals of the first and second kind · surface integrals
- The Gauss–Green formula and Stokes' formula · introduction to field theory
- Series: positive-term, arbitrary-term, power series, Taylor series
- Improper integrals · integrals depending on a parameter
- The Gamma and Beta functions
- Fourier series: orthogonality, convergence, mean-square approximation, Bessel's inequality

Every statement is a bold-tagged entry (**Definition**, **Theorem**, **Proposition**, **Example**) with mathematics in `$…$` / `$$…$$`.

## The homework

Each `homework/weekN.md` follows the series-wide format:

1. **Toolbox** — a blockquote restating the definitions and theorems needed;
2. **Problems** — the assigned exercises;
3. **Solutions** — complete worked proofs ending with `$\blacksquare$`.

With **36 weeks (55 files including supplements) in each language**, this is the largest homework collection in the series.

## Bilingual layout

- `cn/` — authoritative Chinese version.
- `en/` — complete parallel English translation; files share identical names and line counts.

## The `textbooks/` folder

The PDFs are **external reference material** — the two-volume scanned textbook, ten TeX-typeset problem sheets (`Zad-01`–`Zad-10`), and OCR copies for searchability. Nothing here is compiled from the notes, and there is no build system.

## Related repositories

Other course-notes repositories in the same series: [complex-analysis](https://github.com/wenje-ma/complex-analysis), [real-analysis](https://github.com/wenje-ma/real-analysis), [ordinary-differential-equations](https://github.com/wenje-ma/ordinary-differential-equations), and the full list on the [profile page](https://github.com/wenje-ma).
