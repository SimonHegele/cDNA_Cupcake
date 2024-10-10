# cDNA_Cupcake for SQANTI-SIM

cDNA_Cupcake is a dependency of SQANTI-SIM. However, in cDNA_Cupcakes current state it cannot be used in SQANTI-SIM.

In this fork I try to make cDNA_Cupcake compatible with the way SQANTI-SIM uses it.
The changes I made already allow  installation of SQANTI-SIM. 

## Changes

1. Print-statements adapted to python3 syntax
2. Deprecated dependency sklearn replaced with scikit-learn in the setup.py file
3. Moved sequence folder into the cupcake folder and added cupcake.sequence as a package in the setup.py file

## Remaining problems:

For sqanti-sim.py eval:
When given a transcriptome as .fasta-file SQANTI-SIM fails to generate the corresponding .gtf-files.
For GMAP, deSALT and uLTRA it is the alignment step itself that fails but with Minimap2 the mapping is succesfull.
cDNA_Cupcake then fails to generate the .gtf-file.

## Future work:

In SQANTI3 v5.2.1 cDNA_Cupcake was dropped as a dependency. It might be easier to update SQANTI-SIM to use an up-to-date SQANTI3 version rather than fixing cDNA_Cupcake.
