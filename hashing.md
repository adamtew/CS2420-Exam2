# Hashing <a name="hashing"></a> [Instructor Notes](https://usu.instructure.com/courses/388377/files/58790856/download?wrap=1)

|Hashing|Concepts|
|---|---|
|[Hash Function](#hash-function)|Hash Function|
|[Collisions](#collisions)|Linear Probing|
||Clustering|
||Quadratic Probing|



## Hash Function <a name="hash-function"></a>


> This function is called a hash function because it “makes hash” of its inputs

A hash function is a function that:  

- This function has no other purpose

~~~cpp
unsigned int  hash(string key)

__Properties of a good hash function:__  

## Collisions <a name="hash-collisions"></a>

>When two values hash to the same array location, this is called a collision

### Linear Probing

> Use a vacant spot in table following HASH(key) – “open” addressing means that we find an unused address and use it. 
- One problem with the “linear probing” is the tendency to form “clusters”

### Clustering
> A cluster is a group of items not containing any open slots

- Primary Clustering
> is the tendency for certain open-addressing hash tables collision resolution schemes to create long sequences of filled slots.

- Secondary Clustering
> when different keys that hash to same locations compete for successive hash locations.

### Quadratic Probing

- Quadratic probing eliminates primary clustering, but not secondary clustering. 
- - Each of the probe sequences visits all the table locations if the size of the table and the size of the increment are relatively prime with respect to each other. 
>Another way to handle collisions is to have each entry in the hash table hold more than one (B) item. 
>Each location in the hash table is a pointer to a linked list of things that hashed to that location. 
- Saves space if records are long  
__Disadvantages:__  
- Links require space   

>Works well, but we have the overhead of pointers. 
>Rehash – create a larger  (or smaller) array.  Rehash all old elements into new array.
> Hash tables are actually surprisingly efficient
 > __solution:__ Use lazy deletions  
 
## Cuckoo Hashing <a name="hash-cuckoo"></a>
>Cuckoo hashing  worst-case constant lookup time. 