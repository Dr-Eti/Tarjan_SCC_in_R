This is an R implementation of Tarjan's algorithm for finding Strongly Connected Components (SCC) in a digraph by Depth-First Search (DFS). 
This specific code uses while loops instead of a recursion - a function calling itself. This is because writing  recursions - as in the original pseudocode - is not straightforward using the R syntax (unlike JavaScript). Also, in this code the search for SCC is coupled with the problem of finding a block-triangular permutation for the adjacency matrix of the associated digraph (works under certain conditions).
Please note that this code was developed from scratch for the purpose of self-study. It is based on my own reading of the original pseudocode and makes no claims with regards to performance.

Useful references 
 1) Original academic paper: Page 157, Tarjan (1972) doi:10.1137/0201010
 2) Deo (1974) Graph Theory. ISBN: 9780486807935 [but focuses on undirected graphs]
 3) wikipedia: https://en.wikipedia.org/wiki/Tarjan%27s_strongly_connected_components_algorithm#The_algorithm_in_pseudocode
 4) Princeton web resources linked to the book "Algorithms 4th ed": https://algs4.cs.princeton.edu/42digraph/
 5) Duff and Reid (1978) doi:10.1145/355780.355785 - FORTRAN code link to block triangularisation. But uses 'go to' statements to jump around...
 6) Strang (1986) Introduction to Applied Mathematics. ISBN 0-9614088-0-4, Ch. 16 (doesn't implement Tarjan but refers to earlier work)
 7) Hume and Plemmons (1981) p 272 in thid Google book https://books.google.co.uk/books?id=pEMsAQAAIAAJ&pg=PA272&lpg=PA272&dq=duff+and+reid+block+triangularization&source=bl&ots=zlTT95Usx-&sig=ACfU3U3GkBU0av0mI459KObNAqyrc-1sTw&hl=en&sa=X&ved=2ahUKEwiWkKnBlKbyAhUSesAKHXmZArcQ6AF6BAgREAM#v=onepage&q=duff%20and%20reid%20block%20triangularization&f=false

Obviously there are plenty of better-performing, readily-available alternatives out there. Examples include built-in functions in Gephi, and igraph. But I am not aware of DFS-based SCC functions written for R that are not wrappers for code written in another language.  Also, I am not aware of implementations that jointly address the problem of finding a block-diagonal permutation of the adjacency matrix (when possible).
