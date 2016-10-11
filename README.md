# martini_protein_itps
Soluble protein simulated with the Martini force field are mutually
to attractive. In this repository we will collect several approaches
to fix this problem. Neither of the approaches are perfect, all 
of them are an improvement, one of them might be the best.

For questions or comments please contact:
djurredejong _at_ yahoo.com 
-and-
s.j.marrink _at_ rug.nl

There are four solutions:
A. Directly decreases the interactions between proteins, by lowering the LJ epsilon between all protein particles by 0.4 kJ/mol. 

B. Increases the hydration energy of proteins by increasing the Lennard-Jones epsilon of all protein particles with water by 0.35 kJ/mol.

C. Changes the bead types of backbone particles and uncharged sidechain particles of Cysteine, Serine and Lysine to S-types. S-type particles have a smaller LJ sigma (0.42 instead of 0.47 nm) and a LJ epsilon that is reduced to 75%. 

D. Combines aspects of sets B and C: backbone particles of charged and polar (Arg, Lys, Glu, Asp, Asn, Gln) residues are changed to S-type, the hydration energy of charged and polar backbone and side chain particles is increased by 0.35 kJ/mol and the bead type of small side chains (Cys, Thr, Ser) is changed to S-type.

I'll try to create script that can make the changes, especially for sets C and D. If you beat me to it, send me a pull request.
