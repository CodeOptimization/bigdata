# Map-Reduce
## Overview
1. Hadoop MapReduce is a software framework for easily writing applications which process vast amounts of data (multi-terabyte data-sets) in-parallel on large clusters (thousands of nodes) of commodity hardware in a reliable, fault-tolerant manner.
2. A __*MapReduce job*__ usually splits the input data-set into independent chunks which are processed by the  __*map tasks*__ in a completely parallel manner. The framework sorts the outputs of the maps, which are then input to the __*reduce tasks*__. The framework takes care of scheduling tasks, monitoring them and re-executes the failed tasks.
3. The MapReduce framework consists of a single __*master ResourceManager*__, one __*slave NodeManager*__ per cluster-node, and __*MRAppMaster*__ per application.
