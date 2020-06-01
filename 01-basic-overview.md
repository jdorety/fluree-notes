# Fluree basics

## What is Fluree?

Fluree is an immutable, time-ordered ledger.

Each block in the chain is an atomic update that is cryptographically signed.

Fluree instances can be run individually, or as part of a federated network.

## In the beginning

When a Fluree ledger is initialized, block 1 is created. This genesis block contains a lot of important metadata, including the system collections, which are required for Fluree to work.

Each block in the chain represents a point in time at which an atomic update was performed on the ledger. These updates are stored as specially formatted logs known as ***flakes***. No two flakes are ever the same.

At each block, a database can be created from all of the flakes present up to that block.

## Collections and Predicates

A ***collection*** is analogous to a table in a relational database.

The ***predicates*** are analogous to columns in a relational database.

## Subject - Predicate - Object

Each item in a Fluree db is a ***subject***

The individual data fields in a subject are the ***predicates***. A subject can have an unlimited number of predicates (keeping in mind the 2MB size limit on subjects).

***Objects*** are the values associated with predicates.

Together, these pieces come together to form a structure known as a **triple**, or **RDF triple**. These triples allow Fluree compatablility with other *triple-store* databases.

## Flakes

**Flakes** are modified *RDF triples*. Each flake contains the standard *subject - object - predicate*, as well as an integer `t` that represents the time at which a transaction occurred.

The boolean vaue indicates whether a particular update is valid at that particular time.