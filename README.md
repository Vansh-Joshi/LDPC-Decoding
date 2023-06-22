# LDPC-Decoding
This is a team project that gives an efficient algorithm performing LDPC decoding for BEC. It has working codes for both Soft and Hard Decision Decoding.

## Team: 3
- Vansh Joshi - Khushi Shah - Parth Parmar


Low Density Parity Check decoding is used often in the communication thoery for the transmission of encoded messages. Low Density Parity Code implies that the number of variable nodes connected to the check nodes is very less compared to the total length of the transmitted message.
Using [Tanner graph](https://en.wikipedia.org/wiki/Tanner_graph), the decoding algorithm can be understood easily. We have implemented the decoding algorithm in MATLAB using hash and maps.
To get the accurate result, we have performed Monte Carlo simulations over the experiment and final expected probability has been calculated. 
## Time-Space Complexity
The overall **time complexity** of the solution will be O((number of simulations)(dc)(CN)(max_it)) for particular erasure probability where 
dc = degree of checknode
CN = total number of checknodes.
max_it=maximum iterations done.
The overall **space complexity** of the algorithm will be O( (dc)(CN) ). This space is because of the storing of the CN and VN map(Working has been explained in the soft decision code).

## DSA- concepts used
- Graph Traversal
- Hashtable/Unordered map

For the sake of simplicity , the current code can perform decoding for all-zero message only. This can be upgraded for decoding of any message.

## Contents
- AnalyticalFormula -> Theoritically calculates the expected probability of the LDPC decoder
- HardDecisionDecoder-> Performs LDPC decoding using Hard Decision decoding technique
- SoftDecisionDecoder-> Performs LDPC decoding using Soft Decision decoding technique
- HMatrix2 -> Large example matrix  (Make sure to delete the small preloaded example matrix)
- Hmat2_analytical_algorithm_convergence -> Matlab figure of the comparison between our simulator and theoritical answer over different probabilities.

## Future Working
- Optimising space complexity without the increase in time-complexity of the solution i.e not using separate VN_map and CN_map for reference.
- Using same code with some modification to make it an LDPC decoder for BSC as well.


