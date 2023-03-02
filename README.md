# HPC-QC Workflows

Files Explained:

**bell_state.ipynb**

This file is a very introductory program with only two cells, introducing qiskit and how to view your quantum circuits with the .draw() command. The Bell State is created, which entangles two qubits together. 

![Bell State output](/Images/bell-state-example.png)

**getting_started.ipynb**

This file expands on the Bell State notebook. In this file you make a quantum circuit for the Bell State once again, but this time it introduces users to submitting jobs. The source for this code is Qiskit's Youtube video: https://www.youtube.com/watch?v=1kRfHNUbkrg&list=PLOFEBzvs-VvpHs84vFdRVIl3Wlg81j8_x&index=1&t=302s

![Full Bell State](/Images/full-bell-state.png)

![Results](/Images/bell-state-results.png)

**grovers_complete.ipynb**

Final Grover's algorithm used in research paper. Generates a random number between 1 and 15 and creates a Grover Oracle for it.  

![Grover circuit](/Images/grover-circuit.png)

![Grover Results Histogram](/Images/grover-results.png)

![Grover Statevector Results](/Images/grover-statevector.png)

**shors_complete.ipynb** 

Completed Shor's Algorithm file. Generates a random number between 2 and 14 and finds the factors of 15. Images below depict the circuit and diagrams with the expected counts (taking into account error due to noise). 

![Shors circuit for a = 11](/Images/shors-circuit.png)

![Shors results on a simulator](/Images/shors-simulator.png)

![Shors results with a real quantum computer](/Images/shors-qc.png)

**auto_tsp_updated.ipynb**

Final TSP file. In the first part, networkx creates a random TSP map, then a circuit is composed using code from the Qiskit Textbook. To run the program, ensure that you have access to a backend that has enough qubits, as 14 is not available in the free, publicly available IBMQ resource on a real QC (as of July 2022), but it can be run also on a simulator. 

Note: Access to IBMQ resources with higher qubit counts was supplied by Oak Ridge National Lab National Center for Computational Sciences. 

![TSP Circuit (1 of 3)](/Images/tsp-curcuit1.png)

![TSP NetworkX map](/Images/tsp-networkx.png)

![TSP results window](/Images/tsp-results.png)

**auto_tsp_parsl.ipynb**

This last file contains the same code as the previous, auto_TSP_updated.ipynb, however it is split into decorated functions to perform a parsl workflow. This workflow has the capability to combine HPC resources (Andes Linux Cluster) and Quantum Computing cloud resources (IBMQ) into a single workflow, allowing for a greater ease-of-access for researchers in the field. 

Note: This program will download png files of the histograms to your current directory when used, use with caution. It is encouraged to modify the location where the files are downloaded in the code. 
