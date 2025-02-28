# Ultimate Tensile Strength (UTS) Prediction using ML
This project uses Machine Learning (Random Forest Regressor) to predict the Ultimate Tensile Strength (UTS) of a material based on its mechanical properties and material conditions.

Features Used:
- Young's Modulus (E)
- Shear Modulus (G)
- Poisson's Ratio (μ)
- Density (ρ)
- Yield Strength (σₛ)
- Material Conditions: predefined material processing conditions (e.g., Annealed, Quenched, Tempered).

The model also plots an approximate Stress-Strain (σ-ϵ) curve:

The plastic region is approximated using the Hollomon equation: σ=Kϵⁿ; 
The Strain (ϵ) at UTS is approximated as σᵤ/E + (offset); 
The offset is set based on plastic deformation at ranges of Young's Modulus (E) values and pre-processing condition.
The parameters K (strength coefficient) and n (strain-hardening exponent) are derived from the material's True Stress (σ) and True Strain (ϵ) values at yield and UTS.

The fracture region (strain) is estimated by using a fracture strain factor depending on the pre-processing condition and how it affects the ductility of the material. (from 1.0 to 2.0)
The fracture stress is approximated as 0.85 σᵤ (empirical estimation)

Works with a high accuracy for metals like Aluminum, Cast Iron, and Steel.

----

Sample Predicitons:

Tempered Steel: ![tempered](https://github.com/user-attachments/assets/0d12d749-524c-466e-9524-2ca92eb84b48)
Wrought Alumnium: ![wrought aluminum](https://github.com/user-attachments/assets/e8216615-4a06-46dc-8f05-a401358ede18)
