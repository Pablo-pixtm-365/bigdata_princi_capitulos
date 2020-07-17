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


## Chapter 5

1.- What is replication in a few words?
> Replication means keeping a copy of the same data on multiple machines that are connected via a network.

2.- How does leader-based replication work?
> First a replica is defined as leader, this is the one in charge of writing the requests of the clients in their local storage, the other replicas are known as  followers.
> second, once the leader did the writing, the leader sends the data change to all the followers, known as replica or flow change. Literal followers follow the leader in making a local copy of his record.
> Third, clients can read data from the leader or any follower but writes can only be done by the leader.

3.- Mention an advantage and disadvantage of synchronous replication
> Advantage:
This ensures that the follower will have an up-to-date copy of the data that is consistent with the leader. If the leader suddenly fails, we can be sure that the data is still available on the follower.

> Disadvantage:
If the synchronous follower doesn’t respond (because it has crashed, there is a network failure, or for any other reason), the write cannot be processed. The leader must block all writes and wait until Synchronous Replica is available again.

4.- What is the name of the process in which a follower becomes a leader?
> Called failover.

5.- When a replica is a good candidate to be a leader?
> It is the replica with the most updated data changes from the previous leader, this in order to lose less information.

6.- According to the book, what is the divided brain?
> Two nodes both believe they are the leader.

7.- Suppose the company where you work asks you to make a replication record of the data, but you do not have much experience on the subject, what implementation of 
> replication records would you use and why?
Statement-based replication, because it is the simplest case, it is quite compact and there are still DBs that use it by default.

8.- In what situation do you need a consistency of reading?
> When the user sees the data shortly after writing, the new data may not have reached the replica yet, because it was inserted, but it cannot be read because it was not yet loaded into the followers.

9.- Briefly, what does leader-based replication allow?
> allows more than one node to accept writes

10.- Does it rarely make sense to use a multi-leader setup within a single data center? true / false and why?
> True, because the benefits rarely outweigh the added complexity.
