# PRAS WINDOWS APPLICATION

On June 15, 2024, an easy-to-use Windows Desktop Application version of the PRAS server was developed. The download link for the EXE file is available through the website https://www.protein-science.com/

While the web application interface performs only the tasks described in the PRAS paper, the desktop counterpart, which I built in 2024 has extended features. The extended features include tools to build model structures (such as constructing a model of a protein in a pure solvent or mixed solvent, generating pure or mixed solutions, etc.), tools to build crystalline nanostructures (spherical or cylindrical silica nanoparticles) and tools to perform Brownian Dynamics (BD) Simulations of colloidal gels.

# INSTALLATION

The program has been tested on Windows 10 and 11 64-bit operating systems. The program follows a standard Windows installation process. To install the software, double-click the installation file. A shortcut is automatically created on the desktop upon completion. To uninstall the software, navigate to Control Panel -> Programs and Features, then double-click to uninstall.

# USAGE
## Protein Repair
It should be stated that this desktop app integrates the fast and accurate sidechain packer (FASPR) program from which it obtains a flexible dihedral angle (chi) if needed to fix the missing heavy atoms. The app will only warn the user that it is using the default chi for the repair when an mmCIF file that FSPR cannot read is uploaded. This behavior is consistent with the online server. The user should refer to the PRAS paper (https://pubs.acs.org/doi/10.1021/acs.jcim.2c00571) to understand why PRAS uses chi generated by FASPR for protein repair. Therefore, the desktop app generates the same result as the online PRAS server. The user can investigate this and if there are differences, do not hesitate to contact me.
  
The six radio buttons seen in the figure below are unchecked and represent the default behavior. Therefore, to add hydrogen atoms is TRUE, to assign secondary structure elements (SSE) is TRUE, to plot four Ramachandran types is TRUE, to keep ligands is FALSE, to consider Histidine protonation at the pH of 7 is FALSE (HIS is neutral in this case), to retain the temperature factor is FALSE, to use atoms with the highest occupancy is TRUE and the chain to process is ALL. The user is required to set the working directory. If the PDB structure file to be repaired is stored locally on the user’s computer, it must be located in the working directory. The user must have permission to write in the working directory. For this reason, it is suggested to use common directories like the Downloads or Desktop folder. When using the PDB ID, the program downloads the file automatically from the protein data bank and stores it in the user’s working directory before proceeding with the repair (the user must be connected to the internet when using the PDB ID).

![Protein Repair dashboard](https://github.com/osita-sunday-nnyigide/PRAS_Server_Windows_App/blob/main/protein%20repair.png)

## Model Solution
Initially, this tool was designed to generate randomly placed particles in a box for BD simulations. However, with the intention to implement Langevin dynamics, Molecular dynamics, and Molecular docking tools, I expanded its functionality to generate various model systems that I may study or simulate in the future. Currently, the tool allows users to build model systems with up to three molecule types. Examples of model systems generated by this tool is shown in the figure below. A user manual detailing the usage is included with the destribution

![Protein Repair dashboard](https://github.com/osita-sunday-nnyigide/PRAS_Server_Windows_App/blob/main/model%20solutions.png)
