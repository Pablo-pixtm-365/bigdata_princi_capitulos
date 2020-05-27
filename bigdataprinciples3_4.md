## Chapter 3:
1.-What tool can be used to define static and flexible schematics?
> Apache Thrift

2.- What can an individual identify with on a site like superwebanalytics.com?
> by a user ID or a browser cookie

3.- How to store all data together?
> It is achieved by wrapping each property and border type in a DataDanit union.

4.- The pedigree contains the timestamp of the information, but could it too?
> contain debugging information or the source of the data.

5.- Do serialization frames just check?
> that all required fields are present and of the expected type

## Chapter 4:
1.- What to consider for data storage requirements?
> how your data will be written and how it will be read.

2.- Why is parallel support a requirement for master dataset?
> to handle large amounts of data in a scalable way.

3.- What is the most common type of distributed database for the master dataset?
> A key / value store.

4.- What is the biggest problem is that a key / value store? And what causes it?
> random reads, random writes, and all the machinery behind making those work.
> increase in storage costs and will reduce performance when reading and writing data.

5.- What is the problem with a normal file system?
> is that it exists on a single machine, so it can only scale to the storage limits and processing power of that machine.

6.- Difference between a normal and a distributed file system?
> The first one only distributes the storage in one machine and has limits, on the other hand, the distributed as its name says, the > storage is distributed to a group of machines.

7.- What is important about distributed file system from the user's perspective?
> Files are spread across multiple machines for scalability and also to enable par-allel processing.
> File blocks are replicated across multiple nodes for fault tolerance.

8.- What is the vertical partition?
> partition your data so that a function only accesses relevant data for its calculation
9.-
