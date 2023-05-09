05-05-2023
---
# Ejercicio de deduccion logica

Hector, Habil, Audaz y Galante viven aventuras, quien peleo con quien?

Dos batallan dragones
$(He_D \wedge Ha_D) \vee (He_D \wedge Au_D) \vee (He_D \wedge Ga_D) \vee (Ha_D \wedge Au_D) \vee (Ha_D \wedge Ga_D) \vee (Au_D \wedge Ga_D)$

Uno batalla un gigante
$He_G \vee Ha_G \vee Au_G \vee Ga_G$

Uno batalla un hechicero
$He_H \vee Ha_H \vee Au_H \vee Ga_H$

Cada uno batalla una vez
$(\neg Ha_D \vee \neg Ha_G) \wedge (\neg Ha_D \vee \neg Ha_H) \wedge (\neg Ha_H \vee \neg Ha_G)$
$(\neg He_D \vee \neg He_G) \wedge (\neg He_D \vee \neg He_H) \wedge (\neg He_H \vee \neg He_G)$
$(\neg Au_D \vee \neg Au_G) \wedge (\neg Au_D \vee \neg Au_H) \wedge (\neg Au_H \vee \neg Au_G)$
$(\neg Ga_D \vee \neg Ga_G) \wedge (\neg Ga_D \vee \neg Ga_H) \wedge (\neg Ga_H \vee \neg Ga_G)$

Enunciados
1. $\neg Ga_H \rightarrow He_D$
2. $\neg He_G \rightarrow Ha_G$
3. $\neg Au_G \rightarrow Au_H$

---
1. $Ga_H \vee He_D$
2. $He_G \vee Ha_G$
3. $Au_G \vee Au_H$