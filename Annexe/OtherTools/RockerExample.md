# Running Example

In this example we demonstrate a scenario where ROCKER does not discover the complete set of minimal keys discovered in a dataset. 

More precisely, test1.rdf and test2.rdf contain exactly the same information for 6 people from p1 to p6. We observe that by changing the name of the properties in the first case (test1.rdf) ROCKER discovers one key composed of three properties while in the second case Rocker discovers one keys composed of two properties. In the first case the case discovered does not refer to a minimal key. This prove that the tool provided is not conforming to the description of the algorithm in the paper. 

