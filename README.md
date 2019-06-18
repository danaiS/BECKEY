# BECKEY

## Description
 BECKEY is a semantic agnostic approach that discovers keys for three different semantics proposed in the context of the Semantic Web (S-key, F-key and SF-key semantics). More precisely, BECKEY discovers the complete set of minimal keys for a given semantic. This approach is able to discover keys under the presence oferroneous data or duplicates (i.e., almost keys). 

## Input Parameters 
BECKEY takes as input five parameters:
- `File_FullPath` : the full path of the file where the keys are going to be discovered
- `n` : the number of exceptions (n will lead to the discovery of n-non keys and then the extraction of (n-1)-almost keys
)
- `Semantic` : the semantic of the discovered keys (one of the following options: Skeys, Fkeys or SFkeys) 
- `Support` : the minimum support of the discovered keys (set to 0 to discover the complete set of keys)
- `TimeLimit` : the maximum time that BECKEY is going to be executed - if the discovery does not terminate before the end of the maximum time limit no keys are going to be discovered  (OPTIONAL)

## Input File Format 
The file has to be in a n-triple format.For example: 

\<michael_phelps\> \<db:birthdate\> "1985-06-30".

Or

michael_phelps db:birthdate  1985-06-30  (separated by tabs)



## Running BECKEY in the command line
Download BECKEY.jar and run the following command: 

```java -jar jar_fullpath/BECKEY.jar File_FullPath n Semantic Support TimeLimit ```

## Running Examples in the command line
In the following example, BECKEY is going to discover all the sure 0-almost S-keys (0 exceptions allowed), with a minimum support of 10 and a maximum time limit of 60 minutes (the process ):

```java -jar  /keyDiscovery/BECKEY.jar /keyDiscovery/Class/DB_Actor.rdf 1 Skeys 10 60```

Similarly, in this example, BECKEY is going to discover all the 0-almost S-keys (0 exceptions allowed), with a minimum support of 10 and it will run until the set of keys is discovered (no time limit applied):

```java -jar  /keyDiscovery/BECKEY.jar /keyDiscovery/Class/DB_Actor.rdf 1 Skeys 10 ```

## Output
BECKEY provides two files:
- One file containing the keys discovered in a dataset (along with the non-keys). The execution time of the BECKEY is provided in this file.
- One file containing the support for each discovered key.

