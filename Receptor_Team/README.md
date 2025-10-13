# NK cell receptor cooperativity and cytotoxic-decision making project



> The question to be answered:
> - How the difference between flux and the concentration of the activating receptor influence the quantification of NK cell activation.
> - How the coupling or cooperativity between receptor influences the signalling and decision-making in NK cells.
> - How the inhibitory signalling pathway assist the decision-making and NK cell education.


**The content**
- Mathematical modelling of TCR discrimination: how the cooperativity enhances TCR discrimination (both specificity & sensitivity)

- One example publication on TCR  that we could take a reference

- NK cell cytotoxic decision-making VS TCR discrimination: similarities and difference.

- Current theoretical & experimental work on NK cell decision-making




# 1. The mathematical model and TCR activation

Literature in this category can be found in the subfolder: 
[TCR](./TCR/)

> **Key Fact:** T-cell receptors (TCRs) recognise peptide–MHC (pMHC) complexes and discriminate foreign from self via peptide-dependent binding and signalling thresholds; agonist pMHC generally produce longer-lived interactions and stronger signals than self pMHC.

The following two papers provide a comprehensive overview of mathematical models for TCR activation (in my personal opinion):

<details> 
<summary>Trends in Immunology, 35(4), 153-158.</summary>

Dushek, O., & van der Merwe, P. A. (2014). An induced rebinding model of antigen discrimination. *Trends in Immunology, 35*(4), 153-158. **DOI:** [10.1016/j.it.2014.02.002](https://doi.org/10.1016/j.it.2014.02.002) 

[**PDF**](./TCR/An_induced_rebinding_model_of_antigen_discrimination.pdf)

</details>

<details> 
<summary>Nature Reviews Immunology, 14(9), 619-629.</summary>

Lever, M., Maini, P. K., van der Merwe, P. A., & Dushek, O. (2014). Phenotypic models of T cell activation. *Nature Reviews Immunology, 14*(9), 619-629. **DOI:** [10.1038/nri3728](https://doi.org/10.1038/nri3728)

[**PDF**](./TCR/nri3728.pdf)

</details> 
<br>
<br>

---
Here let's focus on the first one: [Trends in Immunology, 35(4), 153-158.](./TCR/An_induced_rebinding_model_of_antigen_discrimination.pdf)


### **Evolution of TCR Activation Models**

```mermaid
graph TD;
    A[1. Occupancy Model] -->|Adds **Specificity**<br/>via time delay| B[2. Kinetic Proofreading];
    B -->|Adds **Sensitivity**<br/>via signal amplification| C[3. Serial Triggering];
    C -->|Unifies both in a<br/>**2D environment**| D[4. Induced Rebinding Model];

    %% Style the final model to highlight it
    style D fill:#d4edda,stroke:#28a745,stroke-width:3px
```

1.  **Stage 1: Solving for Specificity**
    *   **Initial Model:** The **Occupancy Model**.
    *   **Defect:** This model failed to explain T-cell **specificity**, as it predicted that signaling was simply proportional to ligand affinity.
    *   **Solution:** **Kinetic Proofreading (KP)** was introduced. It proposed a time-delay mechanism (e.g., a series of phosphorylation steps) that filters out short-lived, low-affinity binders, thus ensuring only agonist ligands produce a signal.

2.  **Stage 2: Solving for Sensitivity**
    *   **Defect of KP:** While Kinetic Proofreading explained specificity, it predicted very low **sensitivity**, as the long binding times required would limit the total signal generated.
    *   **Solution:** The **Serial Triggering** model was proposed. It suggested that a single ligand could sequentially engage and trigger multiple TCRs, thereby amplifying the signal and accounting for the high sensitivity of T-cells.

3.  **Stage 3: Unifying in a Realistic Environment**
    *   **Defect of Previous Models:** Both KP and Serial Triggering were abstract concepts that did not fully account for the physical reality of the **2D cell surface**.
    *   **Solution:** The **Induced Rebinding Model** provides a unified framework. It integrates both KP and Serial Triggering within a 2D context, showing that when an agonist ligand unbinds, it is likely to quickly rebind to a nearby TCR. This "induced rebinding" dramatically amplifies the signal from agonists, providing a powerful mechanism that boosts both **specificity and sensitivity** simultaneously.
<br>
<br>

---
<figure>
  <img src="./TCR/figure1.png" alt="Flowchart of TCR model evolution" width="100%">
  <figcaption><b>Figure 1</b>. Induced rebinding of T cell receptors improves antigen discrimination. <b>(A)</b> Schematic illustrating that T cells need to exhibit a response only to ligands with a dissociation time (τ = 1/koff) above a threshold (vertical line) even when only a single ligand is displayed (horizontal line) while not responding to ligands below the threshold even when displayed in large numbers. <b>(B)</b> The fraction of pMHCs that remain bound to the TCR over time for six pMHCs for the dissociation times indicated in units of s (for 3D) or ms (for 2D). Increasing the threshold binding time (vertical line) improves specificity because these lines diverge, but at the cost of sensitivity, because in all cases the fraction of pMHC that remains bound decreases exponentially. <b>(C)</b> Direct calculation of the response curves (analogous to panel A) for the standard kinetic proofreading model and kinetic proofreading with constitutive or induced rebinding for the threshold time indicated. <b>(D)</b> Schematic of kinetic proofreading with induced rebinding. Note that both 3D and reduced 2D dissociation times are shown (top panels). Coloured circles in panels A and C correspond to the six pMHCs indicated in panel B.</figcaption>
</figure>


---

### **Things we can learn from this literature**

- When we characterise our model, we can also focus one the balance of specificity and sensitivity to compare the models under different hypothesis. We can also generate the figures like [Figure 1 (A)](./TCR/figure1.png).

<br>
<br>
<br>
<br>

# 2. An example publication on TCR activation that we can take a reference

