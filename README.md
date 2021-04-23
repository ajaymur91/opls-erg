# Cached from https://bitbucket.org/comcon1/oplsaa-erg_ff
The above link is currently down. This is a cached version retrieved from old backups. The following details are obtained from http://erg.biophys.msu.ru/tiki/tiki-index.php?page=OPLS-AA+extension.

#If useful cite the original authors:

One should carefully cite the force field with the revision number because it is required for reproducibility. Here is the example citation:

OPLS-AA ERG extension, revision jun16, TPPMKTOP project. https://bitbucket.org/comcon1/oplsaa-erg_ff/commits/tag/jun16


# OPLS-AA extension
Our force field extension is developed on the basis of the OPLS-AA force field distributed with GROMACS since v. 3.14. This version of the force field corresponds to the 2001 year OPLS-AA version. Further OPLS-AA development was only held in the closed-source projects and thus is not incorporated in our project. The OPLS-AA extension is under constant development and we encourage the users to contribute according to the OPLS-AA contribution protocol.

# Force field repository

The latest version of the OPLS-AA extension can be downloaded from the repository:

https://bitbucket.org/comcon1/oplsaa-erg_ff.

By default you get an access to the developmental version of the force field:

hg clone https://bitbucket.org/comcon1/oplsaa-erg_ff ./opls-erg.ff

To access the last stable version of the extended force field checkout from stable tag:

hg clone https://bitbucket.org/comcon1/oplsaa-erg_ff -r stable ./opls-erg.ff

To contribute to this repository one should read OPLS-AA contribution protocol.

# Development principles

Partial charges are assigned according to the ab inito point electrostatic potential computed using basis set not less than 6-31G** (or using a Dunning equivalent cc-pVDZ) for neutral molecules and cations. Diffuse functions are used for anionic molecules. DFT or MP2 theory are used for electron correlation. Electrostatic potential is computed on CHELPG surface points and then fitted with RESP algorithm.

VdW parameters are developed by titration of σ and ε parameters of the Lennard-Jones potential function in order to reproduce vaporization energy and density of the organic liquid.

Dihedral potential parameters are attributed by comparison of the results of relaxed surface scan calculations in MD simulation and using ab initio methods. The step-by-step algorithm is provided on the simple example.

We also incorporate any published parameters if we find them reliable and obtained in agreement with our principles of development.

# Updates of the version June-2016

New atom types for lipopolysaccharide O-antigen (many carbohydrate residues) [CPC 2016; 10.1002/cphc.201600524]
PF6 parameters added according to [JPCB, 117(48), pp.15176–15183]
Parameters for some ionic liquids added from [JTCT 5(4):1038]
BF4 parameters added from [JPCB: 2002, 106, 13344]
Thiophene sulfur parameters developed [see details in rev No. 40]
New residue topology for 3'-hydroxyechinenone (HEQ) based on standard OPLS-AA atomtypes and diene dihedral types [CR&M 6(5):761, rus.]
New residue topology for phycocyanobiline (CYC) based on the OPLS-AA nucleotide atom types (for adequate dihedral types) [JBMS&D 34(3):489]


