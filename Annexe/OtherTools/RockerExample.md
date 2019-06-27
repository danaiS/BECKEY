# Running Example

In this example we demonstrate a scenario where ROCKER does not discover the complete set of minimal keys as claimed. 

More precisely, we provide two test datasets, dataset1.rdf and dataset2.rdf, that contain exactly the same information for 6 people (Person1..Person6). Three different properties are used to describe these people. 

The only difference between the two files is that the properties are not named in the same way. Therefore, the keys discovered in both datasets should be of the same size. This is not the case using Rocker. 

We observe that when ROCKER is executed on dataset1, a key composed of three properties is discovered. On the contrary, when ROCKER is executed on dataset2 a key composed of two properties is discovered. The correct minimal key in this scenario is the key of size two while the other corresponds to a non-minimal key. This example proves that the tool does not always provides minimal keys as claimed in the description of the algorithm in the paper. 

