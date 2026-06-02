Void Tomography Pipeline
Line-of-sight tomography of cosmic large-scale structure using redshift residuals and void catalogs

🌌 Overview
This repository implements a research pipeline for testing whether photon propagation through cosmic voids produces measurable, path-integrated effects on observed redshift.
The central idea is simple and testable:

Do differences in line-of-sight void traversal correlate with redshift residuals?

If such correlations exist, they provide direct observational evidence that spacetime structure along null trajectories contributes to cosmological observables beyond homogeneous expansion.

🔬 Scientific Motivation
Standard cosmology treats redshift primarily as a function of global expansion. However, in an inhomogeneous universe:

photons traverse large-scale void-dominated regions
expansion and curvature vary along the path
null trajectories sample spacetime differently than matter

This pipeline tests whether these effects produce a detectable, cumulative signal in real data.

🧠 Core Concept
Each line of sight defines a path through cosmic structure.
We compute a void exposure metric:
Evoid=∑iLiE_{\text{void}} = \sum_i L_iEvoid​=i∑​Li​
where LiL_iLi​ is the path length through void iii.
We then test:
Δz  ∝  Evoid\Delta z \;\propto\; E_{\text{void}}Δz∝Evoid​
where:

Δz\Delta zΔz = redshift residual relative to a cosmological model
EvoidE_{\text{void}}Evoid​ = integrated void traversal along the line of sight


📊 Data Sources
The pipeline is designed to work with widely used observational datasets:

Pantheon+ Type Ia Supernovae

spectroscopic redshifts and distance measurements


SDSS / BOSS Void Catalogs

large-scale cosmic void structure (e.g., ZOBOV-based catalogs)



These datasets provide:

independent measurements
large sky coverage
sufficient statistical power for correlation analysis


⚙️ Pipeline Overview
The analysis proceeds in six stages:


Coordinate transformation

Convert SN (RA, Dec, z) → comoving coordinates



Line-of-sight construction

Represent each SN as a null trajectory



Void intersection

Compute intersections between sightlines and void volumes



Exposure calculation

Evaluate path length inside voids



Residual calculation

Compute:

Δz=zobs−zmodel\Delta z = z_{\text{obs}} - z_{\text{model}}Δz=zobs​−zmodel​


Statistical analysis

Correlate Δz\Delta zΔz with void exposure




🧪 Expected Outcomes
The analysis tests three possible scenarios:
✅ Positive correlation

Evidence for path-integrated geometric effects
Supports line-of-sight dependent contributions to redshift

⚠️ Weak correlation

Signal exists but is noise-limited or partially canceled

❌ No correlation

Effect is negligible, isotropic, or not captured by current catalogs

All three outcomes are scientifically meaningful.

📄 Papers
This repository includes a series of working papers developing the theoretical and observational framework:
Foundations

Papers 1–4: MDN theory and geometric derivations

Observational Framework

Paper 5: Depth-sliced measurement
Paper 6: CMB calibration
Paper 7: Tomographic reconstruction

📁 See /papers/ for full preprints.

These documents are working preprints. Formal journal submission is in progress.


🧩 Repository Structure
/papers        → theoretical framework (PDF preprints)
/data          → input datasets (or links)
/src           → analysis modules
/notebooks     → exploratory and visualization workflows


⚠️ Status
Early-stage research pipeline under active development
Current focus:

implement void intersection logic
compute exposure metrics
produce first correlation results


🚀 Getting Started
(Example — to be expanded as code matures)
git clone https://github.com/VoidTomography/void-tomography-pipeline
cd void-tomography-pipeline


🤝 Collaboration
Contributions, ideas, and critical feedback are welcome.
Especially valuable:

improvements to void intersection algorithms
alternative exposure metrics
statistical validation methods
independent dataset integration


📜 License
This project is released under the MIT License.

🧭 Big Picture
This project explores a broader question:

Can spacetime structure be measured directly through null geodesic propagation?

If successful, this approach opens a new observational framework:
Void Tomography of Spacetime
