# blockchain-sql
Reads the raw bitcoin blockchain .DAT files and creates an SQL database

The source files include SQLite3 and a dirent implementation for Windows.

This code compiles on OpenBSD and Windows (using Visual Studio 2015).

To compile on a unix like OS:

gcc bcrdr2.c sha256.c ripe160.c sqlite3.c -o bcrdr2

To run:

./bcrdr2 <block directory> <output db>

E.G.:

./bcrdr2 ~/.bitcoin/blocks out.db

This version of the code fixes the "Too many open files" and the segfault when reading the last block in the chain.
