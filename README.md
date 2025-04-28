# Molecular Probe Combination Guide (Hybrid Solvent Inserter)

In mixed-solvent molecular dynamics (MixMD) simulations, a rational combination of different molecular probes greatly enhances the detection of cryptic pockets and potential binding hotspots in biomolecules.

This guide summarizes the properties, classifications, and recommended combinations of commonly used molecular probes for modeling and simulation reference.

---

## Principles of Probe Combination

- Combine polar molecules with hydrophobic molecules
- Combine hydrogen bond donors with hydrogen bond acceptors
- Use complementary charged probes (positive vs. negative)
- Combine small molecules with aromatic probes to cover diverse pocket types

---

## Standard Probe Combination Table

| Pocket Type | Recommended Probe Combination | Reason |
|:--|:--|:--|
| **Polar pockets** | formamide + meoh + n-methylacetamide | Strong hydrogen bond donor (formamide) + moderate polarity (meoh) + peptide backbone mimic (n-methylacetamide) |
| **Hydrophobic pockets** | benzene + toluene + isopropanol | Aromatic hydrophobic probes (benzene, toluene) + small hydrophobic probe (isopropanol) |
| **Aromatic pockets** | indole + benzene + pyrimidine | Large aromatic probe (indole) + small aromatic probe (benzene) + polar aromatic probe (pyrimidine) |
| **Positively charged pockets** | acetate + formamide | Negative charge probe (acetate) + polar hydrogen-bonding probe (formamide) |
| **Negatively charged pockets** | guanidinium + meoh | Positive charge probe (guanidinium) + moderate polarity probe (meoh) |
| **Mixed hydrophobic-polar pockets** | dmso + isopropanol + benzene | Highly polar-apolar compatible probe (dmso) + small hydrophobic probe (isopropanol) + aromatic hydrophobic probe (benzene) |
| **Large hydrophobic cavities** | indole + toluene | Large aromatic scaffold (indole) + hydrophobic filler (toluene) |

---

## Quick Classification for Probe Selection

- **Polar group**: formamide, meoh, n-methylacetamide
- **Hydrophobic group**: benzene, toluene, isopropanol
- **Aromatic group**: indole, benzene, pyrimidine
- **Charged group**: guanidinium (positive), acetate (negative)
- **Universal probe**: dmso (compatible with most environments)

---

## Common Probe Combination Examples

| Use Case | Probe Combination | Purpose |
|:--|:--|:--|
| **Polar environment detection** | formamide + meoh | Capture polar, hydrogen bond-rich regions |
| **Hydrophobic surface detection** | benzene + toluene | Detect hydrophobic patches and hidden pockets |
| **Aromatic stacking detection** | indole + benzene | Capture stacking interactions (e.g., Trp-rich areas) |
| **Charge interaction detection** | guanidinium + acetate | Complementary charge detection for ionic pockets |
| **Mixed pocket detection** | dmso + benzene + isopropanol | Cover both hydrophobic and polar surface features |

---

## Pro Tips (Advanced Strategy)

- Polar probes (formamide, meoh) are ideal for active sites and polar crevices.
- Hydrophobic probes (benzene, toluene) reveal traditional druggable hydrophobic pockets.
- Aromatic probes (indole, pyrimidine) help detect stacking and aromatic-rich regions.
- Charged probes (guanidinium, acetate) can uncover ion binding sites or charge-shielded pockets.
- Universal probe DMSO can be combined with almost any other probes for enhanced coverage.

---

# Conclusion

Rational combination of molecular probes significantly improves the efficiency of cryptic pocket and hotspot detection.  
This strategy is a critical step in advanced simulation methods such as MixMD, FEP, and FragMap, providing vital insights for structure-based drug discovery.

---

# Detailed Usage Instructions for Individual Molecular Probes (for Hybrid Solvent MD)

This section provides detailed descriptions, usage environments, and combination suggestions for 13 commonly used molecular probes in mixed-solvent simulations.

---

## formamide

**Features:**  
- Extremely strong polarity  
- Excellent hydrogen bond donor  
- Small molecule size, easy to penetrate narrow pockets

**Suitable Environments:**  
- Polar active sites  
- Hidden polar crevices or grooves

**Combination Suggestions:**  
- Combine with meoh and n-methylacetamide to enhance detection of polar pockets.

---

## dmso

**Features:**  
- Highly polar and highly soluble  
- Penetrates both hydrophobic and polar regions  
- Compatible with diverse environments

**Suitable Environments:**  
- Mixed hydrophobic-polar surfaces  
- Deeply hidden cryptic pockets

**Combination Suggestions:**  
- Combine with benzene and isopropanol to maximize overall detection coverage.

---

## meoh (methanol)

**Features:**  
- Moderate polarity  
- Excellent hydrogen bond donor and acceptor  
- Small size for fine pocket detection

**Suitable Environments:**  
- Small polar surface pockets  
- Hydration sites or narrow clefts

**Combination Suggestions:**  
- Use with formamide or guanidinium to strengthen polar detection.

---

## isopropanol

**Features:**  
- Moderate hydrophobicity  
- Capable of hydrogen bonding  
- Small and flexible molecule

**Suitable Environments:**  
- Small hydrophobic pockets  
- Mixed polarity regions

**Combination Suggestions:**  
- Pair with benzene or toluene to cover hydrophobic surfaces.

---

## acetonitrile

**Features:**  
- Weak polarity  
- Small size, fast diffusion  
- Limited hydrogen bonding capacity

**Suitable Environments:**  
- Neutral or weakly polar surfaces  
- Gas-phase like hidden cavities

**Combination Suggestions:**  
- Can be used alone or paired with isopropanol for broader coverage.

---

## guanidinium

**Features:**  
- Positively charged probe  
- Strong ability to stabilize ion pairs  
- Excellent hydrogen bond donor

**Suitable Environments:**  
- Surfaces rich in negative charges  
- DNA/RNA binding sites  
- Acidic residue clusters (Glu, Asp)

**Combination Suggestions:**  
- Combine with acetate (negative charge probe) for complementary charge detection.

---

## acetate

**Features:**  
- Negatively charged probe  
- Mimics anionic environments  
- Good hydration properties

**Suitable Environments:**  
- Surfaces rich in positive charges  
- Basic residue clusters (Lys, Arg)

**Combination Suggestions:**  
- Use with guanidinium for complementary charge pair detection.

---

## n-methylacetamide (NMA)

**Features:**  
- Moderate polarity  
- Mimics peptide backbone (CONH)  
- Participates in hydrogen bond networks

**Suitable Environments:**  
- Cryptic sites involved in peptide backbone recognition  
- Protein-protein interface pockets

**Combination Suggestions:**  
- Combine with formamide to enhance hydrogen bond network probing.

---

## benzene

**Features:**  
- Classic hydrophobic aromatic probe  
- Nonpolar  
- Small size, suitable for small cavity filling

**Suitable Environments:**  
- Hydrophobic patches  
- Aromatic stacking regions (Phe, Tyr, Trp clusters)

**Combination Suggestions:**  
- Combine with isopropanol to extend hydrophobic detection.

---

## toluene

**Features:**  
- Strong aromaticity  
- Slightly larger than benzene  
- Stronger hydrophobicity

**Suitable Environments:**  
- Deep hydrophobic pockets  
- Hydrophobic cavities or clefts

**Combination Suggestions:**  
- Combine with benzene and indole to cover cavities of different sizes.

---

## phenol

**Features:**  
- Aromatic molecule with weak polarity (hydroxyl group)  
- Can participate in both hydrophobic and hydrogen bonding interactions

**Suitable Environments:**  
- Polar-hydrophobic interface areas  
- Mildly polar aromatic pockets

**Combination Suggestions:**  
- Combine with benzene and meoh for enhanced interface detection.

---

## indole

**Features:**  
- Large aromatic probe  
- Mimics tryptophan side chains (Trp)  
- Supports stacking, hydrogen bonding, and hydrophobic interactions

**Suitable Environments:**  
- Large aromatic cryptic pockets  
- Deep-core pocket exploration

**Combination Suggestions:**  
- Combine with benzene and toluene for comprehensive aromatic stacking detection.

---

## pyrimidine

**Features:**  
- Nitrogen-containing aromatic ring  
- Moderate polarity, weak hydrogen bond acceptor

**Suitable Environments:**  
- Aromatic-polar interface regions  
- Small-molecule binding site identification

**Combination Suggestions:**  
- Combine with indole and benzene for detailed detection of aromatic stacking or polar stacking regions.

---

# Conclusion

Scientific selection and combination of molecular probes can significantly improve the efficiency of cryptic pocket detection, providing a solid structural foundation for drug discovery and target validation.

---
