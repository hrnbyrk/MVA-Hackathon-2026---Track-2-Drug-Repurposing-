# MVA-Hackathon-2026---Track-2-Drug-Repurposing-
Computational drug repurposing and mechanistic intervention pipeline for MVA1 (BUB1B deficiency) developed by team aragorn1 for Track 2 of the MVA Hackathon 2026
# 💊 MVA-Hackathon-2026-Track2: Drug Repurposing & Pharmacological Rescue Framework

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Data License: CC BY 4.0](https://img.shields.io/badge/Data%20License-CC%20BY%204.0-blue.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Team: aragorn1](https://img.shields.io/badge/Team-aragorn1-orange.svg)]()

Computational drug repurposing and mechanistic intervention pipeline developed by team **aragorn1** for **Track 2 (Drug Repurposing)** of the "Rare Disease, Real Kid: MVA Hackathon 2026".

---

## 🧬 Project Overview & Biological Rationale

Mosaic Variegated Aneuploidy Type 1 (MVA1) is a severe ultra-rare autosomal recessive disorder driven by mutations in the **BUB1B** gene, which encodes the **BubR1** protein. 

In the cell cycle, BubR1 acts as the core effector of the **Spindle Assembly Checkpoint (SAC)** mechanism during the M phase, functioning as a critical "brake" (anaphase inhibitor and pseudo-substrate) that halts the transition from metaphase to anaphase until all chromosomes achieve proper bipolar attachment[cite: 1, 2, 4].

### ⚠️ Pathological Mechanism of BUB1B Dysfunction
1. **Checkpoint Failure:** Mutations in *BUB1B* lead to a deficiency or functional loss of BubR1, disabling the Mitotic Checkpoint Complex (MCC) assembly[cite: 1].
2. **Premature APC/C Activation:** Free from BubR1 inhibition, **Cdc20** prematurely activates the Anaphase-Promoting Complex/Cyclosome (**APC/C-Cdc20**)[cite: 1, 3].
3. **Cohesin Cleavage & Aneuploidy:** Ubiquitin-mediated proteolysis destroys Securin (PTTG), releasing active **Separin (Esp1)**, which prematurely cleaves the Cohesin complex[cite: 1]. This results in **Premature Chromatid Separation (PCS)** and widespread mosaic aneuploidy[cite: 2, 3].
4. **Clinical Consequences:** Especially in neural progenitor cells, shortened mitosis and massive cell death manifest as severe microcephaly, developmental delay, epileptic seizures, and a high risk of embryonal malignancies (Wilms tumor, rhabdomyosarcoma, leukemia).

---

## 🎯 Therapeutic Strategy & Interventions by Team **aragorn1**

Adapting standard metabolic disorder management principles (such as substrate reduction therapy and pharmacological chaperones) to cell-cycle pathobiology, our team focused on two key axes:

### 1. Substrate Reduction & Hyperactive Complex Inhibition (Targeting Cdc20-APC/C)
Since *BUB1B* deficiency leads to an overactive **APC/C-Cdc20** axis, suppressing free Cdc20 activity extends mitotic timing and rescues the phenotype:
* **Direct Cdc20 Inhibitors (Preclinical & Reference):** *Apcin* (competes at the D-box pocket), *proTAME* (disrupts APC/C binding), and *CP5V (PROTAC)* (targets Cdc20 for degradation).
* **FDA-Approved Drug Repurposing Candidates:**
  * **Labetalol:** Identified via structure-based virtual screening, molecular docking, and molecular dynamics (MD) simulations as a high-affinity binder to the active pocket of CDC20.
  * **Nebivolol:** Suppresses hyperactive cell cycle/CDC20 networks in integrated transcriptomic analyses.
  * **Lidocaine:** Competitively binds to the active site of Cdc20 and downregulates *CDC20* expression to delay early mitotic exit.

### 2. Pharmacological Chaperone & Protein Stabilization (Targeting BubR1)
* **Niacin (NAD+ / SIRT2 Axis):** BubR1 is targeted for proteasomal degradation when acetylated at position K668. The NAD+-dependent SIRT2 deacetylase enzyme deacetylates BubR1, protecting it from degradation and extending its half-life. This represents a safe pediatric approach to strengthen the natural MCC brake by stabilizing residual mutant BubR1 protein[cite: 3].

---

## 🔬 Databases & Knowledge Bases Utilized

Our pathway characterization and drug discovery workflow integrated multi-omics and biomedical literature databases:
* **KEGG Pathways (hsa04110 - Cell Cycle):** Mapped the precise locus of BubR1 and its downstream cascade (`APC/C`, `Securin`, `Separin`, `Cohesin`)[cite: 1].
* **OMIM (Online Mendelian Inheritance in Man - #257300):** Correlated *BUB1B* genotypes with MVA1 clinical phenotypes (microcephaly, cancer predisposition).
* **Gene Ontology (GO):** Analyzed cellular components (kinetochore, spindle checkpoint complex) and molecular functions (serine/threonine kinase activity, ubiquitin-protein ligase inhibitor activity).
* **PubMed & PMC:** Extracted literature evidence on mitotic checkpoint kinetics, small-molecule inhibitors, and clinical case reappraisals.
* **DrugBank & ChEMBL:** Queried physicochemical properties and binding affinities for FDA-approved repurposing candidates (Labetalol, Lidocaine, Niacin).

---

## 🛠️ Technical Specifications & Pipeline

- **Language/Environment:** R / Python hybrid workflow (RStudio, Bioconductor, `reticulate`).
- **Computational Tools:** Molecular docking scoring functions, binding free energy calculations, and structural bioinformatics packages.

---

## 📄 License & Compliance

- **License:** This repository's code is licensed under the [MIT License](LICENSE).
- **Data Usage:** Underlying clinical and genomic data provided by Sage Bionetworks and the MVA Society is licensed under **CC BY 4.0**.
- **Ethics & Privacy:** All operations comply with WCG IRB protocol (#20252010). Raw data files are managed securely and scheduled for deletion post-hackathon.
