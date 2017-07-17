# Map-Reduce

## Overview
1. Hadoop MapReduce is a software framework for easily writing applications which process vast amounts of data (multi-terabyte data-sets) in-parallel on large clusters (thousands of nodes) of commodity hardware in a reliable, fault-tolerant manner.
2. A __*MapReduce job*__ usually splits the input data-set into independent chunks which are processed by the  __*map tasks*__ in a completely parallel manner. The framework sorts the outputs of the maps, which are then input to the __*reduce tasks*__. The framework takes care of scheduling tasks, monitoring them and re-executes the failed tasks.
3. The MapReduce framework consists of a single __*master ResourceManager*__, one __*slave NodeManager*__ per cluster-node, and __*MRAppMaster*__ per application.

## Input & Output 
1. The MapReduce framework operates exclusively on <key, value> pairs, that is, the framework views the input to the job as a set of <key, value> pairs and produces a set of <key, value> pairs as the output of the job, conceivably of different types.
2. The __key__ and __value__ classes have to be serializable by the framework and hence need to implement the __Writable__ interface. Additionally, the key classes have to implement the __WritableComparable__ interface to facilitate sorting by the framework.
3. Input and Output types of a MapReduce job:
(input) <k1, v1> -> *__map__* -> <k2, v2> -> *__combine__* -> <k2, v2> -> *__reduce__* -> <k3, v3> (output)

## MapReduce - User Interfaces

### Mapper
1. Mapper maps input key/value pairs to a set of intermediate key/value pairs.
