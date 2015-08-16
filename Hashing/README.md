# Hashing

## Hash Table

A **hash table** is a data structure which implements the dictionary ADT using a table of size M and a hash function h(k) which maps each key k (which may be of any type) to value in the range 0,1,...,M-1

The set of all possible input keys k is called the **universe** of keys and is donoted by U. The actual set of keys inserted into the table is not necessarily equal to U.

### Load Factor

way to measure hash table

The **load factor** of a hash table of size M containing n keys is

![loadfactor](http://i.imgur.com/yL5fhQP.png)

**Rule of thumb**: Choose the table size to keep a <= 0.6

### Collisions

A **collision** in a hasing scheme is a pair of keys k1, k2 in U such that

h(k1) = h(k2)

Since collisions are unavoidable, hash tables must include a **collision resolution** scheme to acoommodate keys with equal hash values.

## Chaining

### Separate Chaining

Instead of storing keys in the table itself, keys are stored in linked lists attached to each index of the talbe. This permits one index of the table to contain multiple keys.

![sc](http://i.imgur.com/RRPwSyE.png)

*e.g. **clustering** in a hash table*

![clustering](http://i.imgur.com/9CTWVL2.png)

## Open Addressing

**Open Addressing** collision resolution schemes store every key in a table inex, using a **probing scheme** to find an available index when a collision occurs

### Linear Probing

starts at the hash value h(k), then checks successive indices until an empty space is found.
The **probe sequence** is

    h(k), h(k)+1, h(k)+2, h(k)+3,...

where all value are taken modulo the table size M. The index checked at step i is

    (h(k) + i) mod M

### Quadratic Probing

using the probe sequence

    h(k)+0^2, h(k)+1^2, h(k)+2^2, ...

The index checked at step i is

    (h(k) + i^2) mod M

### Double Hashing

uses two hash functions h1(k) and h2(k), where h2(k) != 0 for any k. The probe sequence is

    h1(k)+h2(k), h1(k)+2h2(k), h1(k)+3h2(k),...

The index checked at step i is

    (h1(k) + ih2(k)) mod M
