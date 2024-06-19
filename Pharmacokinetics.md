---
name: Pharmacokinetics
topic: Analysis of Pharmacokinetic Data
maintainer: Bill Denney
email: wdenney@humanpredictions.com
version: 2022-12-05
source: https://github.com/cran-task-views/Pharmacokinetics/
---

Analysis of pharmacokinetic (PK) data is concerned with defining the
relationship between the dosing regimen and the body's exposure to drug
as indicated by the concentration time curve to determine a dose. To
analyze PK data, there are three categories of packages within CRAN:
noncompartmental analysis (NCA), modeling (typically using compartmental
analysis), and reporting (typically for NCA).

Pharmacokinetics are often collected during clinical trials of new drugs.  For
more information on R packages for clinical trials, see
`r view("ClinicalTrials")`.

# Call for a co-maintainer

CRAN task views hopes that all task views will have multiple maintainers from
diverse backgrounds.  If you are interested in becoming a co-maintainer of this
task view, please contact the current maintainer (listed at the top of the task
view).

# Noncompartmental Analysis (NCA)

NCA is used as method of description of PK with minimal assumptions of the rates
of distribution of the drug through the body. NCA is typically used to describe
the PK of a drug in clinical studies with many samples per subject on the same
and sequential days.

The NCA packages are:

`r pkg("ncappc")`:
Performs traditional NCA and simulation-based posterior predictive
checks for a population PK model using NCA metrics. It targets
summarizing data from model-fit or simulated sources.

`r pkg("NonCompart")`:
Provides basic computational functions for NCA.

`r pkg("PK")`:
Allows estimation of pharmacokinetic parameters using
non-compartmental theory. Both complete sampling and sparse sampling
designs are implemented. The package provides methods for hypothesis
testing and confidence intervals related to superiority and
equivalence.

`r pkg("PKNCA")`:
Computes standard NCA parameters and summarizes them with the goal
of taking in observed clinical data and providing summaries ready
for study reports and regulatory submission.

`r pkg("qpNCA")`:
Noncompartmental Pharmacokinetic Analysis by qPharmetra

# Workflow tools

The tools in this section connect multiple parts of analysis together, typically
they support some or all parts of data import, review, analysis, and reporting.

`r pkg("ruminate")`:
`ruminate` is a pharmacometrics data transformation and analysis tool.
Exploration of pharmacometrics data involves both general tools (transformation
and plotting) and specific techniques (non-compartmental analysis). This kind of
exploration is generally accomplished by utilizing different packages. The
purpose of 'ruminate' is to create a 'shiny' interface to make these tools more
broadly available while creating reproducible results.

# Pharmacometric Modeling

Modeling of PK data typically uses compartmental methods which assume
that the drug enters the body either through an intravenous (IV) or
extravascular (often oral or subcutaneous, SC) dose. Packages listed
below are restricted to packages that have specific interest to PK
modeling and not the (many) packages that support modeling that could be
used for PK data. The PK modeling and simulation packages are:

`r pkg("bayesnec")`:
A Bayesian No-Effect- Concentration (NEC) Algorithm

`r pkg("clinPK")`:
Calculates equations commonly used in clinical pharmacokinetics and
clinical pharmacology, such as equations for dose individualization,
compartmental pharmacokinetics, drug exposure, anthropomorphic
calculations, clinical chemistry, and conversion of common clinical
parameters. Where possible and relevant, it provides multiple
published and peer-reviewed equations within the respective R
function.

`r pkg("clinDR")`:
Bayesian and ML Emax model fitting, graphics and simulation for clinical dose
response.

`r pkg("clustDRM")`:
Functions to identify the pattern of a dose-response curve. Then fit a set of
appropriate models to it according to the identified pattern, followed by model
averaging to estimate the effective dose.

`r pkg("dr4pl")`:
Dose Response Data Analysis using the 4 Parameter Logistic (4pl) Model

`r pkg("linpk")`:
Generate Concentration-Time Profiles from Linear PK Systems

`r pkg("mrgsolve")`:
Facilitates simulation from hierarchical, ordinary differential
equation (ODE) based models typically employed in drug development.

`r pkg("pharmr")`:
Interfaces to the `pharmpy` library for pharmacometric modeling.

`r pkg("PKPDsim")`:
Simulate dose regimens for pharmacokinetic-pharmacodynamic (PK-PD) models
described by differential equation (DE) systems. And, simulation using
ADVAN-style analytical equations is also supported.

`r pkg("pmxcode")`:
Provides a user interface to create or modify pharmacometric models for various
modeling and simulation software platforms.

`r pkg("rxode2")`:
Methods for simulation from drug development  hierarchical ordinary differential
equations (ODE). This is the basis of the `r pkg("nlmixr2")` package and
supersedes the `RxODE` package.

`r pkg("nlmixr2")`:
Nonlinear Mixed Effects Models in Population PK/PD (superseding the `nlmixr`
package)

`r pkg("nmw")`:
Is a package to understand the algorithms of NONMEM.

`r pkg("PKconverter")`:
The Parameter Converter of the Pharmacokinetic Models

`r pkg("pkdata")`:
Creates Pharmacokinetic/Pharmacodynamic (PK/PD) Data

`r pkg("pmxTools")`:
Pharmacometric tools for common data analytical tasks; closed-form
solutions for calculating concentrations at given times after dosing
based on compartmental PK models (1-compartment, 2-compartment and
3-compartment, covering infusions, zero- and first-order absorption,
and lag times, after single doses and at steady state, per Bertrand
& Mentre (2008)); parametric simulation from NONMEM-generated
parameter estimates and other output; and parsing, tabulating and
plotting results generated by Perl-speaks-NONMEM (PsN).

`r pkg("scaRabee")`:
Is an optimization toolkit for pharmacokinetic-pharmacodynamic models. A port of
the Scarabee toolkit originally written as a Matlab-based application. scaRabee
provides a framework for simulation and optimization of
pharmacokinetic-pharmacodynamic models at the individual and population level.
It is built on top of the neldermead package, which provides the direct search
algorithm proposed by Nelder and Mead for model optimization.

`r pkg("ubiquity")`:
PKPD, PBPK, and Systems Pharmacology Modeling Tools.  It is a omplete work flow
for the analysis of pharmacokinetic pharmacodynamic (PKPD),
physiologically-based pharmacokinetic (PBPK) and systems pharmacology models
including: creation of ordinary differential equation-based models, pooled
parameter estimation, individual/population based simulations, rule-based
simulations for clinical trial design and modeling assays, deployment with a
customizable 'Shiny' app, and non-compartmental analysis. System-specific
analysis templates can be generated and each element includes integrated
reporting with 'PowerPoint' and 'Word'.

`r pkg("UnifiedDoseFinding")`:
Dose-Finding Methods for Non-Binary Outcomes

`r pkg("wnl")`:
Minimization Tool for Pharmacokinetic-Pharmacodynamic Data Analysis

## NONMEM modeling support

The NONMEM package is often used for pharmacometric modeling.  Several packages
are specifically available to support NONMEM-related modeling.  Packages that
work with NONMEM but also work with other modeling software are described in the
general modeling section above.

`r pkg("nonmem2R")`:
Loading NONMEM and PSN (Perl-speaks-NONMEM,
<https://uupharmacometrics.github.io/PsN/>) output files to extract parameter
estimates, provide visual predictive check (VPC) and goodness of fit (GOF)
plots, and simulate with parameter uncertainty.

`r pkg("nonmem2rx")`:
'NONMEM' has been a tool for running nonlinear mixed effects models since the
1980s and is still used today (Bauer 2019 <doi:10.1002/psp4.12404>). This tool
allows you to convert 'NONMEM' models to 'rxode2' (Wang, Hallow and James
(2016) <doi:10.1002/psp4.12052>) and with simple models 'nlmixr2' syntax
(Fidler et al (2019) <doi:10.1002/psp4.12445>). The 'nlmixr2' syntax requires
the residual specification to be included and it is not always translated. If
available, the 'rxode2' model will read in the 'NONMEM' data and compare the
simulation for the population model ('PRED') individual model ('IPRED') and
residual model ('IWRES') to immediately show how well the translation is
performing. This saves the model development time for people who are creating
an 'rxode2' model manually. Additionally, this package reads in all the
information to allow simulation with uncertainty (that is the number of
observations, the number of subjects, and the covariance matrix) with a
'rxode2' model. This is complementary to the 'babelmixr2' package that
translates 'nlmixr2' models to 'NONMEM' and can convert the objects converted
from 'nonmem2rx' to a full 'nlmixr2' fit.

`r pkg("nonmemica")`:
Systematically creates and modifies NONMEM(R) control streams. Harvests NONMEM
output, builds run logs, creates derivative data, generates diagnostics.

# Visualization

`r pkg("xgxr")`:
Supports a structured approach for exploring PKPD data. It also contains helper
functions for enabling the modeler to follow best R practices (by appending the
program name, figure name location, and draft status to each plot). In addition,
it enables the modeler to follow best graphical practices (by providing a theme
that reduces chart ink, and by providing time-scale, log-scale, and
reverse-log-transform-scale functions for more readable axes). Finally, it
provides some data checking and summarizing functions for rapidly exploring
pharmacokinetics and pharmacodynamics (PKPD) datasets.

`r pkg("xpose4")`:
A model building aid for nonlinear mixed-effects (population) model analysis
using NONMEM, facilitating data set checkout, exploration and visualization,
model diagnostics, candidate covariate identification and model comparison.

## Visual predictive checks (VPC)

`r pkg("nlmeVPC")`:
Various visual and numerical diagnosis methods for the nonlinear mixed effect
model, including visual predictive checks, numerical predictive checks, and
coverage plots.

`r pkg("tidyvpc")`:
Perform a Visual Predictive Check (VPC), while accounting for stratification,
censoring, and prediction correction. Using piping from 'magrittr', the
intuitive syntax gives users a flexible and powerful method to generate VPCs
using both traditional binning and a new binless approach Jamsen et al. (2018)
<doi:10.1002/psp4.12319> with Additive Quantile Regression (AQR) and Locally
Estimated Scatterplot Smoothing (LOESS) prediction correction.

`r pkg("vpc")`:
Visual predictive checks are a commonly used diagnostic plot in pharmacometrics,
showing how certain statistics (percentiles) for observed data compare to those
same statistics for data simulated from a model. The package can generate VPCs
for continuous, categorical, censored, and (repeated) time-to-event data.

# Pharmacokinetics Reporting

Communication of results is as important (or more important) than
actually completing an analysis. While many users are currently using
rmarkdown and knitr for general reporting, the features of packages
which are important for reporting PK data are:

`r pkg("ncar")`:
Provides NCA for a report writer generating rtf and pdf output.

`r pkg("pkr")`:
Generates NCA data sets compliant to CDISC and other pharmacokinetic
functions for reviewer.

`r pkg("pmxpartab")`:
Create parameter tables for pharmacometric (PMx) analyses. Generate nicely
formatted HTML tables to display estimation results for pharmacometric models.

`r pkg("xpose")`:
Diagnostics for non-linear mixed-effects (population) models from
'NONMEM'. 'xpose' facilitates data import, creation of numerical
run summary and provide 'ggplot2'-based graphics for data
exploration and model diagnostics.

`r pkg("xpose.nlmixr2")`:
Graphical Diagnostics for Pharmacometric Models: Extension to 'nlmixr2'
(superseding the `xpose.nlmixr` package)

`r pkg("nlmixr2rpt")`: Provides automatic reporting of `nlmixr2` models as
word documents and powerpoint documents.

# Datasets or Single Models

Packages that focus on a single pharmacokinetic model or dataset include:

`r pkg("caffsim")`:
Simulate plasma caffeine concentrations using population
pharmacokinetic model described in Lee, Kim, Perera, McLachlan and
Bae (2015)

# Study Design

Packages related to PK study design include:

`r pkg("BE")`:
Analyze bioequivalence study data with industrial strength. Sample size could be
determined for various crossover designs, such as 2x2 design, 2x4 design, 4x4
design, Balaam design, Two-sequence dual design, and William design.

`r pkg("microsamplingDesign")`:
Find optimal microsampling designs for non-compartmental
pharacokinetic analysis using a general simulation methodology. This
methodology consist of (1) specifying a pharmacokinetic model
including variability among animals; (2) generating possible
sampling times; (3) evaluating performance of each time point choice
on simulated data; (4) generating possible schemes given a time
point choice and additional constraints and finally (5) evaluating
scheme performance on simulated data. The default settings differ
from the article of Barnett and others, in the default
pharmacokinetic model used and the parameterization of variability
among animals.

`r pkg("PopED")`:
`PopED` computes optimal experimental designs for both population and individual
studies based on nonlinear mixed-effect models.

`r pkg("posologyr")`:
Individual Dose Optimization using Population Pharmacokinetics Determine
individual pharmacokinetic (and pharmacokinetic-pharmacodynamic) profiles and
use them to personalise drug regimens. You provide the data and a population
pharmacokinetic model, 'posologyr' provides the individual a posteriori estimate
and allows you to determine the optimal dosing.

### Links
-   [PKBugs](https://www.mrc-bsu.cam.ac.uk/software/bugs/the-bugs-project-pkbugs/)
-   [WinBUGS](http://winbugs-development.mrc-bsu.cam.ac.uk/)
-   [NONMEM](http://www.iconplc.com/innovation/nonmem/)
-   [STAN](http://mc-stan.org/)
