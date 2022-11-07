[![INFORMS Journal on Computing Logo](https://INFORMSJoC.github.io/logos/INFORMS_Journal_on_Computing_Header.jpg)](https://pubsonline.informs.org/journal/ijoc)

This project is distributed in association with the [INFORMS Journal on
Computing](https://pubsonline.informs.org/journal/ijoc) under the [MIT License](LICENSE).

The software and data in this repository are associated with the paper [Diagnostic Tools for Evaluating and Comparing Simulation-Optimization Algorithms](???) by D. J. Eckman, S. G. Henderson, and S. Shashaani. 

## Version

The version used in the paper is

[![Release](v1.0.1)](https://github.com/simopt-admin/simopt/releases/tag/v1.0.1)

## Cite

To cite this software, please cite the [paper](???) and the software, using the following DOI.

[![DOI](???)](???)

Below is the BibTex for citing this version of the code.

```
@article{diagnostictoolsijoc,
  author =        {D. J. Eckman and S. G. Henderson and S. Shashaani},
  publisher =     {INFORMS Journal on Computing},
  title =         {Diagnostic Tools for Evaluating and Comparing Simulation-Optimization Algorithms},
  year =          {2022},
  doi =           {???},
  url =           {???},
}  
```

## Description

SimOpt is a testbed of simulation-optimization problems and solvers. Its purpose is to encourage the development and constructive comparison of simulation-optimization (SO) solvers (algorithms). We are particularly interested in the finite-time performance of solvers, rather than the asymptotic results that one often finds in related literature.

For the purposes of this project, we define simulation as a very general technique for estimating statistical measures of complex systems. A system is modeled as if the probability distributions of the underlying random variables were known. Realizations of these random variables are then drawn randomly from these distributions. Each replication gives one observation of the system response, i.e., an evaluation of the objective function or stochastic constraints. By simulating a system in this fashion for multiple replications and aggregating the responses, one can compute statistics and use them for evaluation and design.

Several papers have discussed the development of SimOpt and experiments run on the testbed:
* [Pasupathy and Henderson (2006)](https://www.informs-sim.org/wsc06papers/028.pdf) explains the original motivation for the testbed.
* [Pasupathy and Henderson (2011)](https://www.informs-sim.org/wsc11papers/363.pdf) describes an earlier interface for MATLAB implementations of problems and solvers.
* [Dong et al. (2017)](https://www.informs-sim.org/wsc17papers/includes/files/179.pdf) conducts an experimental comparison of several solvers in SimOpt and analyzes their relative performance.
* [Eckman et al. (2019)](https://www.informs-sim.org/wsc19papers/374.pdf) describes in detail changes to the architecture of the MATLAB version of SimOpt and the control of random number streams.
* [Eckman et al. (2021)](https://eckman.engr.tamu.edu/wp-content/uploads/sites/233/2021/09/SimOpt-metrics-paper.pdf) introduces the design of experiments for comparing solvers; this design has been implemented in the latest Python version of SimOpt. For detailed description of the terminology used in the library, e.g., factors, macroreplications, post-processing, solvability plots, etc., see this paper.

## Documentation
Full documentation for the source code can be found **[here](https://simopt.readthedocs.io/en/latest/index.html)**.

## Working with the Repository
This repository can be [cloned](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository). Download a copy of the cloned repository to your local machine and navigate to the root directory in your preferred integrated development environment (IDE). You will need to make sure that you have the following dependencies installed: Python 3, `numpy`, `scipy`, `matplotlib`, `pandas`, `seaborn`, and `mrg32k3a`. Run the command ``` python -m pip install numpy scipy matplotlib pandas seaborn mrg32k3a``` to install them from the terminal.

The `demo` folder contains the script `demo_san-sscont-ironorecont_experiment`, which runs multiple solvers on multiple versions of (s, S) inventory, iron ore, and stochastic activiy network problems and produce plots. The resulting data and plots are used for the INFORMS Journal on Computing paper. To reproduce the results, run the command

    python demo/demo_san-sscont-ironorecont_experiment.py

## Ongoing Development

The core development team currently consists of 

- [**David Eckman**](https://eckman.engr.tamu.edu) (Texas A&M University)
- [**Sara Shashaani**](https://shashaani.wordpress.ncsu.edu) (North Carolina State University)
- [**Shane Henderson**](https://people.orie.cornell.edu/shane/) (Cornell University)

This code is being developed on an on-going basis at the authors'
[Github site](https://github.com/simopt-admin/simopt).
Users can contribute problems and solver to SimOpt by using [pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) in GitHub or corresponding with the developers. 


## Acknowledgments
An earlier website for SimOpt, [http://www.simopt.org](http://www.simopt.org), was developed through work supported by the National Science Foundation under grant nos. DMI-0400287, CMMI-0800688 and CMMI-1200315.
Recent work on the development of SimOpt has been supported by the National Science Foundation under grant nos. DGE-1650441, CMMI-1537394, CMMI-1254298, CMMI-1536895, CMMI-2206972, IIS-1247696, and TRIPODS+X DMS-1839346, by the Air Force Office of Scientific Research under grant nos. FA9550-12-1-0200, FA9550-15-1-0038, and FA9550-16-1-0046, and by the Army Research Office under grant no. W911NF-17-1-0094.
Any opinions, findings and conclusions or recommendations expressed in this material are those of the authors and do not necessarily reflect the views of the National Science Foundation (NSF).
