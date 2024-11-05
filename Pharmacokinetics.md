---
name: Pharmacokinetics
topic: Analysis of Pharmacokinetic Data
maintainer: Bill Denney, Satyaprakash Nayak
email: wdenney@humanpredictions.com, sn248@cornell.edu
version: 2024-11-04
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

# Noncompartmental Analysis (NCA)

NCA is used as method of description of PK with minimal assumptions of the rates
of distribution of the drug through the body. NCA is typically used to describe
the PK of a drug in clinical studies with many samples per subject on the same
and sequential days.

The NCA packages are:

`r pkg("ncappc")`:
A flexible tool that can perform (i) traditional non-compartmental analysis (NCA) and (ii) Simulation-based posterior predictive checks for population pharmacokinetic (PK) and/or pharmacodynamic (PKPD) models using NCA metrics.

`r pkg("NonCompart")`:
Conduct a noncompartmental analysis with industrial strength. Some features are 1) Use of CDISC SDTM terms 2) Automatic or manual slope selection 3) Supporting both 'linear-up linear-down' and 'linear-up log-down' method 4) Interval(partial) AUCs with 'linear' or 'log' interpolation method * Reference: Gabrielsson J, Weiner D. Pharmacokinetic and Pharmacodynamic Data Analysis - Concepts and Applications. 5th ed. 2016. (ISBN:9198299107).

`r pkg("PK")`:
Allows estimation of pharmacokinetic parameters using non-compartmental theory. Both complete sampling and sparse sampling
designs are implemented. The package provides methods for hypothesis testing and confidence intervals related to superiority and
equivalence.

`r pkg("PKNCA")`:
Compute standard Non-Compartmental Analysis (NCA) parameters for typical pharmacokinetic analyses and summarize them.

`r pkg("qpNCA")`:
Computes noncompartmental pharmacokinetic parameters for drug concentration profiles. For each profile, data imputations and adjustments are made as necessary and basic parameters are estimated. Supports single dose, multi-dose, and multi-subject data. Supports steady-state calculations and various routes of drug administration. See ?qpNCA and vignettes. Methodology follows Rowland and Tozer (2011, ISBN:978-0-683-07404-8), Gabrielsson and Weiner (1997, ISBN:978-91-9765-100-4), and Gibaldi and Perrier (1982, ISBN:978-0824710422).

# Workflow tools

The tools in this section connect multiple parts of analysis together, typically
they support some or all parts of data import, review, analysis, and reporting.

`r pkg("ruminate")`:
Exploration of pharmacometrics data involves both general tools (transformation and plotting) and specific techniques (non-compartmental analysis). This kind of exploration is generally accomplished by utilizing different packages. The purpose of 'ruminate' is to create a 'shiny' interface to make these tools more broadly available while creating reproducible results.

# Pharmacometric Modeling

Modeling of PK data typically uses compartmental methods which assume that the drug enters the body either through an intravenous (IV) or extravascular (often oral or subcutaneous, SC) dose. Packages listed below are restricted to packages that have specific interest to PK modeling and not the (many) packages that support modeling that could be used for PK data. The PK modeling and simulation packages are:

`r pkg("bayesnec")`:
Implementation of No-Effect-Concentration estimation that uses 'brms' (see Burkner (2017)<doi:10.18637/jss.v080.i01>; Burkner (2018)<doi:10.32614/RJ-2018-017>; Carpenter 'et al.' (2017)<doi:10.18637/jss.v076.i01> to fit concentration(dose)-response data using Bayesian methods for the purpose of estimating 'ECx' values, but more particularly 'NEC' (see Fox (2010)<doi:10.1016/j.ecoenv.2009.09.012>), 'NSEC' (see Fisher and Fox (2023)<doi:10.1002/etc.5610>), and 'N(S)EC (see Fisher et al. 2023<doi:10.1002/ieam.4809>). A full description of this package can be found in Fisher 'et al.' (2024)<doi:10.18637/jss.v110.i05>. This package expands and supersedes an original version implemented in 'R2jags' (see Su and Yajima (2020)<https://CRAN.R-project.org/package=R2jags>; Fisher et al. (2020)<doi:10.5281/ZENODO.3966864>).

`r pkg("clinPK")`:
Provides equations commonly used in clinical pharmacokinetics and clinical pharmacology, such as equations for dose individualization, compartmental pharmacokinetics, drug exposure, anthropomorphic calculations, clinical chemistry, and conversion of common clinical parameters. Where possible and relevant, it provides multiple published and peer-reviewed equations within the respective R function.

`r pkg("clinDR")`:
Bayesian and ML Emax model fitting, graphics and simulation for clinical dose response. The summary data from the dose response meta-analyses in Thomas, Sweeney, and Somayaji (2014) <doi:10.1080/19466315.2014.924876> and Thomas and Roy (2016) <doi:10.1080/19466315.2016.1256229> Wu, Banerjee, Jin, Menon, Martin, and Heatherington(2017) <doi:10.1177/0962280216684528> are included in the package. The prior distributions for the Bayesian analyses default to the posterior predictive distributions derived from these references.

`r pkg("dr4pl")`:
Models the relationship between dose levels and responses in a pharmacological experiment using the 4 Parameter Logistic model. Traditional packages on dose-response modelling such as 'drc' and 'nplr' often draw errors due to convergence failure especially when data have outliers or non-logistic shapes. This package provides robust estimation methods that are less affected by outliers and other initialization methods that work well for data lacking logistic shapes. We provide the bounds on the parameters of the 4PL model that prevent parameter estimates from diverging or converging to zero and base their justification in a statistical principle. These methods are used as remedies to convergence failure problems. Gadagkar, S. R. and Call, G. B. (2015) <doi:10.1016/j.vascn.2014.08.006> Ritz, C. and Baty, F. and Streibig, J. C. and Gerhard, D. (2015) <doi:10.1371/journal.pone.0146021>.

`r pkg("linpk")`:
Generate concentration-time profiles from linear pharmacokinetic (PK) systems, possibly with first-order absorption or zero-order infusion, possibly with one or more peripheral compartments, and possibly under steady-state conditions. Single or multiple doses may be specified. Secondary (derived) PK parameters (e.g. Cmax, Ctrough, AUC, Tmax, half-life, etc.) are computed.

`r pkg("mrgsolve")`:
Fast simulation from ordinary differential equation (ODE) based models typically employed in quantitative pharmacology and systems biology.

`r pkg("pharmr")`:
Interface to the 'Pharmpy' 'pharmacometrics' library. The 'Reticulate' package is used to interface Python from R.

`r pkg("PKPDsim")`:
Simulate dose regimens for pharmacokinetic-pharmacodynamic (PK-PD) models described by differential equation (DE) systems. Simulation using ADVAN-style analytical equations is also supported (Abuhelwa et al. (2015) <doi:10.1016/j.vascn.2015.03.004>).

`r pkg("pmxcode")`:
Provides a user interface to create or modify pharmacometric models for various modeling and simulation software platforms.

`r pkg("rxode2")`:
Facilities for running simulations from ordinary differential equation ('ODE') models, such as pharmacometrics and other compartmental models. A compilation manager translates the ODE model into C, compiles it, and dynamically loads the object code into R for improved computational efficiency. An event table object facilitates the specification of complex dosing regimens (optional) and sampling schedules. NB: The use of this package requires both C and Fortran compilers, for details on their use with R please see Section 6.3, Appendix A, and Appendix D in the "R Administration and Installation" manual. Also the code is mostly released under GPL. The 'VODE' and 'LSODA' are in the public domain. The information is available in the inst/COPYRIGHTS.

`r pkg("nlmixr2")`:
Fit and compare nonlinear mixed-effects models in differential equations with flexible dosing information commonly seen in pharmacokinetics and pharmacodynamics (Almquist, Leander, and Jirstrand 2015 <doi:10.1007/s10928-015-9409-1>). Differential equation solving is by compiled C code provided in the 'rxode2' package (Wang, Hallow, and James 2015 <doi:10.1002/psp4.12052>).

`r pkg("nmw")`:
This shows how NONMEM(R) software works. NONMEM's classical estimation methods like 'First Order(FO) approximation', 'First Order Conditional Estimation(FOCE)', and 'Laplacian approximation' are explained.

`r pkg("PKconverter")`:
Pharmacokinetics is the study of drug absorption, distribution, metabolism, and excretion. The pharmacokinetics model explains that how the drug concentration change as the drug moves through the different compartments of the body. For pharmacokinetic modeling and analysis, it is essential to understand the basic pharmacokinetic parameters. All parameters are considered, but only some of parameters are used in the model. Therefore, we need to convert the estimated parameters to the other parameters after fitting the specific pharmacokinetic model. This package is developed to help this converting work. For more detailed explanation of pharmacokinetic parameters, see "Gabrielsson and Weiner" (2007), "ISBN-10: 9197651001"; "Benet and Zia-Amirhosseini" (1995) <doi:10.1177/019262339502300203>; "Mould and Upton" (2012) <doi:10.1038/psp.2012.4>; "Mould and Upton" (2013) <doi:10.1038/psp.2013.14>.

`r pkg("pkdata")`:
Prepare pharmacokinetic/pharmacodynamic (PK/PD) data for PK/PD analyses. This package provides functions to standardize infusion and bolus dose data while linking it to drug level or concentration data.

`r pkg("pmxTools")`:
Pharmacometric tools for common data analytical tasks; closed-form solutions for calculating concentrations at given times after dosing based on compartmental PK models (1-compartment, 2-compartment and 3-compartment, covering infusions, zero- and first-order absorption, and lag times, after single doses and at steady state, per Bertrand & Mentre (2008) <http://lixoft.com/wp-content/uploads/2016/03/PKPDlibrary.pdf>); parametric simulation from NONMEM-generated parameter estimates and other output; and parsing, tabulating and plotting results generated by Perl-speaks-NONMEM (PsN).

`r pkg("scaRabee")`:
A port of the Scarabee toolkit originally written as a Matlab-based application. scaRabee provides a framework for simulation and optimization of pharmacokinetic-pharmacodynamic models at the individual and population level. It is built on top of the neldermead package, which provides the direct search algorithm proposed by Nelder and Mead for model optimization.

`r pkg("ubiquity")`:
Complete work flow for the analysis of pharmacokinetic pharmacodynamic (PKPD), physiologically-based pharmacokinetic (PBPK) and systems pharmacology models including: creation of ordinary differential equation-based models, pooled parameter estimation, individual/population based simulations, rule-based simulations for clinical trial design and modeling assays, deployment with a customizable 'Shiny' app, and non-compartmental analysis. System-specific analysis templates can be generated and each element includes integrated reporting with 'PowerPoint' and 'Word'.

`r pkg("UnifiedDoseFinding")`:
In many phase I trials, the design goal is to find the dose associated with a certain target toxicity rate. In some trials, the goal can be to find the dose with a certain weighted sum of rates of various toxicity grades. For others, the goal is to find the dose with a certain mean value of a continuous response. This package provides the setup and calculations needed to run a dose-finding trial with non-binary endpoints and performs simulations to assess design’s operating characteristics under various scenarios. Three dose finding designs are included in this package: unified phase I design (Ivanova et al. (2009) <doi:10.1111/j.1541-0420.2008.01045.x>), Quasi-CRM/Robust-Quasi-CRM (Yuan et al. (2007) <doi:10.1111/j.1541-0420.2006.00666.x>, Pan et al. (2014) <doi:10.1371/journal.pone.0098147>) and generalized BOIN design (Mu et al. (2018) <doi:10.1111/rssc.12263>). The toxicity endpoints can be handled with these functions including equivalent toxicity score (ETS), total toxicity burden (TTB), general continuous toxicity endpoints, with incorporating ordinal grade toxicity information into dose-finding procedure. These functions allow customization of design characteristics to vary sample size, cohort sizes, target dose-limiting toxicity (DLT) rates, discrete or continuous toxicity score, and incorporate safety and/or stopping rules.

`r pkg("wnl")`:
This is a set of minimization tools (maximum likelihood estimation and least square fitting) to solve examples in the Johan Gabrielsson and Dan Weiner's book "Pharmacokinetic and Pharmacodynamic Data Analysis - Concepts and Applications" 5th ed. (ISBN:9198299107). Examples include linear and nonlinear compartmental model, turn-over model, single or multiple dosing bolus/infusion/oral models, allometry, toxicokinetics, reversible metabolism, in-vitro/in-vivo extrapolation, enterohepatic circulation, metabolite modeling, Emax model, inhibitory model, tolerance model, oscillating response model, enantiomer interaction model, effect compartment model, drug-drug interaction model, receptor occupancy model, and rebound phenomena model.

## NONMEM modeling support

The NONMEM package is often used for pharmacometric modeling.  Several packages are specifically available to support NONMEM-related modeling.  Packages that work with NONMEM but also work with other modeling software are described in the general modeling section above.

`r pkg("nonmem2R")`:
Loading NONMEM (NONlinear Mixed-Effect Modeling, <https://www.iconplc.com/solutions/technologies/nonmem/>) and PSN (Perl-speaks-NONMEM, <https://uupharmacometrics.github.io/PsN/>) output files to extract parameter estimates, provide visual predictive check (VPC) and goodness of fit (GOF) plots, and simulate with parameter uncertainty.

`r pkg("nonmem2rx")`:
'NONMEM' has been a tool for running nonlinear mixed effects models since the 80s and is still used today (Bauer 2019 <doi:10.1002/psp4.12404>). This tool allows you to convert 'NONMEM' models to 'rxode2' (Wang, Hallow and James (2016) <doi:10.1002/psp4.12052>) and with simple models 'nlmixr2' syntax (Fidler et al (2019) <doi:10.1002/psp4.12445>). The 'nlmixr2' syntax requires the residual specification to be included and it is not always translated. If available, the 'rxode2' model will read in the 'NONMEM' data and compare the simulation for the population model ('PRED') individual model ('IPRED') and residual model ('IWRES') to immediately show how well the translation is performing. This saves the model development time for people who are creating an 'rxode2' model manually. Additionally, this package reads in all the information to allow simulation with uncertainty (that is the number of observations, the number of subjects, and the covariance matrix) with a 'rxode2' model. This is complementary to the 'babelmixr2' package that translates 'nlmixr2' models to 'NONMEM' and can convert the objects converted from 'nonmem2rx' to a full 'nlmixr2' fit.

`r pkg("nonmemica")`:
Systematically creates and modifies NONMEM(R) control streams. Harvests NONMEM output, builds run logs, creates derivative data, generates diagnostics. NONMEM (ICON Development Solutions <https://www.iconplc.com/>) is software for nonlinear mixed effects modeling. See 'package?nonmemica'.

# Visualization

`r pkg("xgxr")`:
Supports a structured approach for exploring PKPD data <https://opensource.nibr.com/xgx/>. It also contains helper functions for enabling the modeler to follow best R practices (by appending the program name, figure name location, and draft status to each plot). In addition, it enables the modeler to follow best graphical practices (by providing a theme that reduces chart ink, and by providing time-scale, log-scale, and reverse-log-transform-scale functions for more readable axes). Finally, it provides some data checking and summarizing functions for rapidly exploring pharmacokinetics and pharmacodynamics (PKPD) datasets.

`r pkg("xpose4")`:
A model building aid for nonlinear mixed-effects (population) model analysis using NONMEM, facilitating data set checkout, exploration and visualization, model diagnostics, candidate covariate identification and model comparison. The methods are described in Keizer et al. (2013) <doi:10.1038/psp.2013.24>, and Jonsson et al. (1999) <doi:10.1016/s0169-2607(98)00067-4>.

## Visual predictive checks (VPC)

`r pkg("nlmeVPC")`:
Various visual and numerical diagnosis methods for the nonlinear mixed effect model, including visual predictive checks, numerical predictive checks, and coverage plots (Karlsson and Holford, 2008, <https://www.page-meeting.org/?abstract=1434>).

`r pkg("tidyvpc")`:
Perform a Visual Predictive Check (VPC), while accounting for stratification, censoring, and prediction correction. Using piping from 'magrittr', the intuitive syntax gives users a flexible and powerful method to generate VPCs using both traditional binning and a new binless approach Jamsen et al. (2018) <doi:10.1002/psp4.12319> with Additive Quantile Regression (AQR) and Locally Estimated Scatterplot Smoothing (LOESS) prediction correction.

`r pkg("vpc")`:
Visual predictive checks are a commonly used diagnostic plot in pharmacometrics, showing how certain statistics (percentiles) for observed data compare to those same statistics for data simulated from a model. The package can generate VPCs for continuous, categorical, censored, and (repeated) time-to-event data.

# Pharmacokinetics Reporting

Communication of results is as important (or more important) than actually completing an analysis. While many users are currently using
rmarkdown and knitr for general reporting, the features of packages which are important for reporting PK data are:

`r pkg("ncar")`:
Conduct a noncompartmental analysis with industrial strength. Some features are 1) CDISC SDTM terms 2) Automatic or manual slope selection 3) Supporting both 'linear-up linear-down' and 'linear-up log-down' method 4) Interval(partial) AUCs with 'linear' or 'log' interpolation method 5) Produce pdf, rtf, text report files. * Reference: Gabrielsson J, Weiner D. Pharmacokinetic and Pharmacodynamic Data Analysis - Concepts and Applications. 5th ed. 2016. (ISBN:9198299107).

`r pkg("pkr")`:
Conduct a noncompartmental analysis as closely as possible to the most widely used commercial software. Some features are 1) CDISC SDTM terms 2) Automatic slope selection with the same criterion of WinNonlin(R) 3) Supporting both 'linear-up linear-down' and 'linear-up log-down' method 4) Interval(partial) AUCs with 'linear' or 'log' interpolation method * Reference: Gabrielsson J, Weiner D. Pharmacokinetic and Pharmacodynamic Data Analysis - Concepts and Applications. 5th ed. 2016. (ISBN:9198299107).

`r pkg("pmxpartab")`:
Generate nicely formatted HTML tables to display estimation results for pharmacometric models.

`r pkg("xpose")`:
Diagnostics for non-linear mixed-effects (population) models from 'NONMEM' <https://www.iconplc.com/solutions/technologies/nonmem/>. 'xpose' facilitates data import, creation of numerical run summary and provide 'ggplot2'-based graphics for data exploration and model diagnostics.

`r pkg("xpose.nlmixr2")`:
Extension to 'xpose' to support 'nlmixr2'. Provides functions to import 'nlmixr2' fit data into an 'xpose' data object, allowing the use of 'xpose' for 'nlmixr2' model diagnostics.

`r pkg("nlmixr2rpt")`: 
This allows you to generate reporting workflows around 'nlmixr2' analyses with outputs in Word and PowerPoint. You can specify figures, tables and report structure in a user-definable 'YAML' file. Also you can use the internal functions to access the figures and tables to allow their including in other outputs (e.g. R Markdown).

# Datasets or Single Models

Packages that focus on a single pharmacokinetic model or dataset include:

`r pkg("caffsim")`:
Simulate plasma caffeine concentrations using population pharmacokinetic model described in Lee, Kim, Perera, McLachlan and Bae (2015) <doi:10.1007/s00431-015-2581-x>.

# Study Design

Packages related to PK study design include:

`r pkg("BE")`:
Analyze bioequivalence study data with industrial strength. Sample size could be determined for various crossover designs, such as 2x2 design, 2x4 design, 4x4 design, Balaam design, Two-sequence dual design, and William design. Reference: Chow SC, Liu JP. Design and Analysis of Bioavailability and Bioequivalence Studies. 3rd ed. (2009, ISBN:978-1-58488-668-6).

`r pkg("PopED")`:
Optimal experimental designs for both population and individual studies based on nonlinear mixed-effect models. Often this is based on a computation of the Fisher Information Matrix. This package was developed for pharmacometric problems, and examples and predefined models are available for these types of systems. The methods are described in Nyberg et al. (2012) <doi:10.1016/j.cmpb.2012.05.005>, and Foracchia et al. (2004) <doi:10.1016/S0169-2607(03)00073-7>.

`r pkg("posologyr")`:
Optimize drug regimens through model-informed precision dosing, using individual pharmacokinetic (PK) and pharmacokinetic-pharmacodynamic (PK-PD) profiles. By integrating therapeutic drug monitoring (TDM) data with population models, 'posologyr' provides accurate posterior estimates and enables the calculation of personalized dosing regimens. The empirical Bayes estimates are computed following the method described by Kang et al. (2012) <doi:10.4196/kjpp.2012.16.2.97>.

### Links
-   [PKBugs](https://www.mrc-bsu.cam.ac.uk/software/bugs/the-bugs-project-pkbugs/)
-   [WinBUGS](http://winbugs-development.mrc-bsu.cam.ac.uk/)
-   [NONMEM](http://www.iconplc.com/innovation/nonmem/)
-   [STAN](http://mc-stan.org/)
