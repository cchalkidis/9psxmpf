# A GAP potential for carbon from randomly selected, uncurated structures: comparison with GAP-20

**C. D. Chalkidis, G. Fanourgakis**
Laboratory of Quantum and Computational Chemistry, School of Chemistry, Aristotle University of Thessaloniki

Poster presented at the **9th Panhellenic Conference of Graduate and Undergraduate Chemistry Students**,
Aristotle University of Thessaloniki, 29–30 November 2026 (Topic 5: Computational Chemistry and Artificial Intelligence).

**Landing page:** <https://9psxmpf.chalkidis.eu> (the address behind the QR code on the poster)

---

## At a glance

- **Question.** What accuracy does a machine-learning potential reach when its training structures are
  drawn at random, with no curation?
- **Finding.** With **1,000 random, uncurated structures**, a GAP potential reaches the accuracy of
  **GAP-20**, which was trained on **6,088 curated ones**: a median energy error of **0.0093 eV/atom**
  versus **0.0103 eV/atom**, on the 116 structures that neither model had seen.
- **Cause.** The limit is set by a few high-energy structures with extreme forces; a larger model does not
  fix them, and GAP-20 fails on the same structures.
- **Limitations.** Only 3 high-energy structures are in the evaluation set, and the evaluation structures
  come from the same database as our samples; the 0.90 ratio is therefore an indication of equivalence,
  not proof of it.

## Abstract

*As submitted to the conference. Figure 1 is in the [abstract PDF](pdf/abstract-en.pdf);
a [Greek version](pdf/abstract-el.pdf) is also available.*

Machine learning potentials such as Gaussian Approximation Potentials (GAP; Bartók et al., 2010)
approach quantum-mechanical accuracy at a cost orders of magnitude lower, but they shift their limitation
from the functional form to the data, whose iterative curation demands time and expertise. We examine what
accuracy is obtained without any curation, and what limits it. Training sets of 50 to 2,000 structures
were drawn by stratified random sampling from the same database of 17,525 carbon configurations from which
the published GAP-20 potential was curated (Rowe et al., 2020). We trained 1,040 potentials with the SOAP
descriptor (Bartók et al., 2013), in eight model settings with ten repetitions per size, and evaluated
them on a common set of 203 structures.

The energy error falls by 43% up to about 700 structures and then rises by 6.6% up to 2,000, not through
overfitting but because of rare high-energy structures with extreme forces, which enter larger sets more
often and degrade the fit. A tenfold increase in capacity (from 300 to 3,000 representative points) lowers
the error by 40.5% but not the failure rate on these structures, where GAP-20, too, has an error
33 times larger than on the rest. On the 116 evaluation structures that neither model had seen, the best
potential reaches 0.0093 eV/atom versus 0.0103 for GAP-20, using 1,000 random structures instead of 6,088
curated ones (Figure 1); it is better on ordered structures and worse on disordered ones.

The binding constraint on accuracy therefore lies in the data, not in the model; curation is not a
prerequisite but one of the available levers.

## Contents

| Path | Description |
|---|---|
| `index.html` | The landing page (Greek and English, single file, no build step) |
| `pdf/poster-el.pdf`, `pdf/poster-en.pdf` | The poster, A0 portrait, in Greek and English |
| `pdf/abstract-el.pdf`, `pdf/abstract-en.pdf` | The conference abstract, in Greek and English |
| `figures/` | The poster figures as SVG, one file per language (`-el`, `-en`) |
| `CNAME` | Custom domain for GitHub Pages |

This repository holds the published poster material only. The training and analysis code is part of
the undergraduate thesis on which the poster is based.

## How to cite

> Chalkidis, C. D., & Fanourgakis, G. (2026). *A GAP potential for carbon from randomly selected,
> uncurated structures: Comparison with GAP-20* [Poster presentation]. 9th Panhellenic Conference of
> Graduate and Undergraduate Chemistry Students, Aristotle University of Thessaloniki, Greece.
> https://9psxmpf.chalkidis.eu

## References

- Bartók, A. P., Payne, M. C., Kondor, R., & Csányi, G. (2010). Gaussian approximation potentials:
  The accuracy of quantum mechanics, without the electrons. *Physical Review Letters, 104*(13), 136403.
  https://doi.org/10.1103/PhysRevLett.104.136403
- Bartók, A. P., Kondor, R., & Csányi, G. (2013). On representing chemical environments.
  *Physical Review B, 87*(18), 184115. https://doi.org/10.1103/PhysRevB.87.184115
- Rowe, P., Deringer, V. L., Gasparotto, P., Csányi, G., & Michaelides, A. (2020). An accurate and
  transferable machine learning potential for carbon. *The Journal of Chemical Physics, 153*(3), 034702.
  https://doi.org/10.1063/5.0005084

## Acknowledgements

We thank the IT Center of the Aristotle University of Thessaloniki for the “Aristotle” computing
infrastructure.

## Contact

Christos Chalkidis · contact@chalkidis.eu (or chalchri@chem.auth.gr)

© 2026 C. D. Chalkidis and G. Fanourgakis. All rights reserved.
