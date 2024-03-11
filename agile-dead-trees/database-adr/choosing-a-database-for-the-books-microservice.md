# Agile Dead Trees: Choosing a database technology for the Books microservice

## Context

The books microservice is responsible for storing the books. The data is very simple but its size can be really big since books can be hundreds and even thousands of pages long.

To improve performance and bandwidth, the books are going to be stored as chapters, and for even better performance, theses chapters can be split into very small chunks of data so, for instance, a user is reading a book as an e-book, there is no need to retrieve the whole chapter, so the queries are going to be really fast.

The options are an SQL or document database, since other types of database make less sense in this scenario. After evaluating the strenghts and weaknesses of eath one, we opted to go with the document database.

## Rationale

The document database was chosen for the following reasons:
    - The data is not relational and not complex enough to justify a relational database.
    - The data is going to be read more that it is going to be written, which is a strong argument for document databases that are optmized for read.
    - Document databases are also widely used for content management.
    - The main limitation is that document databases generally have document size limits, but due to our architecture spliting the books into chapters and the chapters into chunks, this should not be a problem.
    - There is not a need for searching the books as well, only by title and by chapter name at most, so the better indexing of a relational database is not needed.

The document database of choice is going to be MongoDB, due to it being one of the most well stablished document databases available and it has all the features the solution needs and, if need be, it can also store files in a very nice way, with advanced querying capabilities.

## Consequences

By going with a document database, we ensure that the model is scalable vertically and horizontally to ensure that the performance will stay excellent. Aditionally, the team will need to invest time learning the technology.

There are some tradeoffs compared to the relational database, such as the document size limit, but we think that this should not affect us for now.
