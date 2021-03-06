- Master node: a node that manages the cluster by running software components which coordinate the distribution of data and tasks among other (slave) nodes for processing. It tracks the status of tasks and monitors the health of the cluster.
- Slave node:
  - Core node: It has software components which runs tasks and stores data in the Hadoop distributed file system (HDFS) on your cluster. They do the heavy lifting with the data.
  - Task node: A slave node that has software components which only run tasks. They are optional.
- Map phase:
  - Mapping is a function that defines the processes which splits the large data file for processing.
  - During the mapping phase, the data is split into 128MB chunks
  - The larger the instance size used in our EMR, the more chunks you can map and process at the same time.
  - If there are more chunks than nodes/mappers, the chunks will queue for processing.
- Reduce phase:
  - Reducing is a function that aggregates the split data back into one data source
  - Reduced data needs to be stored (in a service like S3) as data processed by the EMR cluster is not persistent