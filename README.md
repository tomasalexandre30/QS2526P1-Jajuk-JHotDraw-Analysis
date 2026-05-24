<div align="center">

# A Comparative Study of Jajuk and JHotDraw 5.2

![Java](https://img.shields.io/badge/Java-Legacy-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![inFusion](https://img.shields.io/badge/inFusion-Analysis-6C3483?style=for-the-badge)
![SonarQube](https://img.shields.io/badge/SonarQube-IDE-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white)
![MetricsTree](https://img.shields.io/badge/MetricsTree-Metrics-2ECC71?style=for-the-badge)

### Quality & Software Engineering (2025/26) — NOVA School of Science & Technology

*A **reverse engineering analysis** of two Java-based open-source systems, comparing their structural quality, code smells, coupling, inheritance and duplication profiles.*

</div>

---

## About the Report

This report presents a reverse engineering study of **Jajuk 11.0** and **JHotDraw 5.2**, two Java-based open-source systems with distinct purposes and design philosophies. Using tools such as **inFusion**, **MetricsTree**, and **SonarQube for IDE**, the analysis examines each system through the lens of the Overview Pyramid and progressively dives into size, complexity, coupling, inheritance and code duplication.

The two systems reveal markedly different quality profiles — Jajuk shows significant structural problems accumulated over years of development, while JHotDraw 5.2 demonstrates a more disciplined object-oriented design.

> 📄 Full analysis available in the report:
>
> **[Access the Full Report](QS2526p1_TAlexandre73213_NIachimovschi73391_Jajuk.pdf)**

---

## Systems Analysed

| System | Version | Type | Classes | LOC |
|--------|---------|------|---------|-----|
| **Jajuk** | 11.0 "Deepest Blue" | Desktop media player | 564 | 47 438 |
| **JHotDraw** | 5.2 | Reusable drawing framework | 186 | 7 712 |

---

## Key Findings

### Jajuk

- **27 God Classes** and **24 Data Classes** — widespread lack of encapsulation and over-responsible classes
- **4 Brain Classes** and **73 Shotgun Surgery** cases — concentrated complexity and high change propagation
- CBO values consistently exceeding 100, with `CoverView` reaching **CBO = 100, WMC = 229**
- **271 duplication issues** across 126 files — systemic absence of constant extraction
- **35 cyclic package dependencies** — deep architectural problems

### JHotDraw 5.2

- **0 God Classes**, only **2 Data Classes** — cleaner separation of responsibilities
- Deeper inheritance hierarchies (HIT = 0.30 vs 0.14) — intentional extensibility-driven design
- Max CBO of **73**, max WMC of **108** — considerably more contained than Jajuk
- Only **7 duplication issues** across 2 files
- Main concern: **80 Feature Envy** methods and high NOM/NOC = 7.47

---

## Comparative Summary

| Metric / Indicator | Jajuk | JHotDraw 5.2 |
|--------------------|-------|--------------|
| Classes | 564 | 186 |
| Lines of Code | 47 438 | 7 712 |
| Max WMC | 229 | 108 |
| Max CBO | 104 | 73 |
| God Classes | 27 | 0 |
| Data Classes | 24 | 2 |
| Shotgun Surgery | 73 | 9 |
| Cyclic Dependencies | 35 | 0 |
| Duplication Issues | 271 | 7 |
| Files with Duplication | 126 | 2 |

---

## Tools Used

| Tool | Purpose |
|------|---------|
| **inFusion** | Overview Pyramid, code disharmonies (God Class, Feature Envy, etc.) |
| **MetricsTree** | NOM, WMC, CBO, DIT distribution charts and treemaps |
| **SonarQube for IDE** | Code duplication detection |
| **IntelliJ IDEA** | Project setup and static analysis environment |

---

## Authors

This report was developed as part of the **Quality & Software Engineering** course in the **MSc in Computer Engineering** program at **NOVA School of Science and Technology**.

| Student | Number |
|---------|--------|
| Tomás Alexandre | 73213 |
| Nicolae Iachimovschi | 73381 |

> **Course:** Quality & Software Engineering (2025/26) | **NOVA School of Science & Technology**
