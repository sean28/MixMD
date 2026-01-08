# Molecular Probes Guide (Hybrid Solvent Inserter)

## Table of Contents
- [Principles of Usage Instructions for single probes ](#principles-of-usage-instructions-for-single-probe)
  - [Common Probe Information](#common-probe-information) 
  - [formamide](#formamide)
  - [dmso](#dmso)
  - [meoh](#meoh)
  - [isopropanol](#isopropanol)
  - [acetonitrile](#acetonitrile)
  - [guanidinium](#guanidinium)
  - [acetate](#acetate)
  - [n-methylacetamide](#n-methylacetamide)
  - [benzene](#benzene)
  - [toluene](#toluene)
  - [phenol](#phenol)
  - [indole](#indole)
  - [pyrimidine](#pyrimidine)
- [Conclusion](#conclusion)

---

# Molecular Probes Guide (Hybrid Solvent Inserter)

In mixed-solvent molecular dynamics (MixMD) simulations, a rational combination of different molecular probes greatly enhances the detection of cryptic pockets and potential binding hotspots in biomolecules. This guide summarizes the properties, classifications.

**MixMD System Builder** is a web-based application for generating mixed-solvent molecular simulation systems. It supports protein structure upload, flexible probe selection, box configuration, and automatic topology generation. Users can easily integrate custom molecules and apply optional solvation and ionization, resulting in ready-to-use simulation packages. I redeployed this online tool in my repository and you can use this tool for free by clicking <a href="https://cadd.sean28299.dpdns.org">here</a>. You can also view the original code by clicking <a href="https://drive.google.com/file/d/14qXKdj0SDHBIVM89_n7eVwHnaIBH3cQu/view?usp=sharing">here</a>. Click <a href="https://drive.google.com/file/d/1VWFS5YxMN3nSc_GNgupO-39uSTTEXK_r/view?usp=sharing">here</a> to download the example file for reference. 

**Probe GridMap Builder** is a local web-based software interface designed to analyze molecular dynamics (MD) trajectories in .trr or .nc format, powered by the AMBER cpptraj backend. It enables users to generate grid-based interaction maps between protein structures and solvent probe atoms across dynamic frames. You can use this tool for free by clicking <a href="https://sean28.github.io/Probe-GridMap-Builder/">here</a>. 👉 [Live Demo](https://sean28.github.io/MixMD/probe_gridmap_ui.html)

<div style="text-align: justify"> <br> </div>
---

# Principles of Usage Instructions for Single probe

## Common Probe Information

This table summarizes the molecular weight and density information of 13 commonly used molecular probes.

| Probe | Molecular Weight (g/mol) | Density (g/mL) |
|:---:|:---:|:---:|
| formamide | 45.041 | 1.13 |
| dmso | 78.129 | 1.10 | 
| meoh (methanol) | 32.042 | 0.791 | 
| isopropanol | 60.096 | 0.785 | 
| acetonitrile | 41.053 | 0.786 | 
| guanidinium | 60.080 | 1.260 |
| acetate | 59.044 | 1.0492 | 
| n-methylacetamide | 73.095 | 0.957 | 
| benzene | 78.114 | 0.874 | 
| toluene | 92.141 | 0.867 | 
| phenol | 94.113 | 1.071 | 
| indole | 117.151 | 1.220 | 
| pyrimidine | 80.090 | 1.016 | 

---

### Notes
- **Guanidinium**:  
  Pure guanidinium cation density is unavailable; estimated based on typical guanidinium chloride solution density (~1.26 g/mL). Can detect negatively charged regions on protein surfaces (such as near Asp and Glu residues)

- **Acetate**:  
  As pure acetate ion density is not measurable directly, acetic acid (CH₃COOH) liquid density (~1.0492 g/mL) is used as an approximation. Can detect positively charged regions on protein surfaces (such as near LyS and Arg residues)

---

### Special Notes
---

1. Electric neutral system: If many charged small molecules are added, additional Na * and CI ions must be added in the simulation to balance the overall charge
2. Short range exclusion: A small amount of random dispersion can be added to the initial distribution of probes to prevent excessive stacking
3. Minimize energy: After adding the probe, it is very important to perform a rigorous round of restrained minimization!

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

## meoh 

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

## n-methylacetamide

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

Rational combination of molecular probes significantly improves the efficiency of cryptic pocket and hotspot detection.  
This strategy is a critical step in advanced simulation methods such as MixMD, FEP, and FragMap, providing vital insights for structure-based drug discovery. Scientific selection and combination of molecular probes can significantly improve the efficiency of cryptic pocket detection, providing a solid structural foundation for drug discovery and target validation.

---
