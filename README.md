# Longitudinal Inference Without Longitudinal Data

### A Copula Based Framework for Modeling Dependence and Growth in Educational Assessment

**Damian W. Betebenner** (National Center for the Improvement of Educational Assessment)

Presented at the NCIEA Colloquium, May 2026, Jackson Hole, WY.

## View the Presentation

The slides are hosted via GitHub Pages at:
**[https://dbetebenner.github.io/NCIEA_2026_Colloquium/](https://dbetebenner.github.io/NCIEA_2026_Colloquium/)**

## Repository Contents

    docs/
      index.html                     # Reveal.js presentation (rendered via Quarto)
      assets/
        In_Order_We_Trust.pdf        # Linked PDF (QR target on the references slide)
        apps/
          liwld/                     # Embedded D3 interactive (LIwLD explainer)
            index.html
            assets/                  # Hashed JS+CSS bundle, KaTeX fonts (~3.8 MB)
            data/scenarios/          # Precomputed Phase-A analytic payload

Most assets (figures, fonts, slide CSS/JS) are embedded directly in `index.html`
via Quarto's `embed-resources: true`. The LIwLD interactive is the one
exception: it lives at `docs/assets/apps/liwld/` and is loaded into a slide via
iframe so the React/D3 application and its precomputed bundle can be served as
separate files.

## About the Presentation

This presentation, adapted from a technical talk delivered at the 2026 NCME Annual Meeting, introduces a copula-based framework that makes group-level growth inference possible without student-level longitudinal linkage. The slides frame the methodology for NCIEA staff around four connections to the Center's work: (1) extending Student Growth Percentiles (SGP) to settings without linked data, (2) unlocking growth inference for NAEP, TIMSS, PISA, and cross-state comparisons, (3) strengthening the measurement foundation for fair score use through an ordinally defensible coordinate system, and (4) improving practical monitoring and decision support through a Statistical Process Control (SPC) lens.

Using Sklar's Theorem, Braun's Trajectory Analysis of Matched Percentiles (TAMP) is recovered as the comonotonic copula, and Student Growth Percentiles (SGPc) arise as conditional quantiles — the transition kernel $\partial C / \partial u$ — under a general copula model. A sensitivity analysis across 966 longitudinal conditions, 4 datasets, and 4 content areas establishes the $t$-copula as a robust canonical choice (selected in 64% of cases by AIC). A minimum-distance fitting procedure over the Beta family recovers subgroup mean SGPc from cross-sectional marginals alone, with validation showing $r = 0.995$ and MAE $= 0.40$ SGPc points against linked ground truth. The precision cost of foregoing linkage (CI widening of $\sim 2.5\times$) is quantifiable and manageable for large-scale assessment programs such as NAEP, TIMSS, and PISA.

Technical derivations, the sensitivity analysis, accuracy and precision results, and three extension discussions (implications for psychometrics, causal inference, and statistical process control) are included as supplemental appendix material.
