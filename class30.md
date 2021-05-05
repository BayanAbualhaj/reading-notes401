# Hash Table 

![](https://www.tutorialspoint.com/data_structures_algorithms/images/hash_function.jpg)


### What is a Hashtable?

* Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
* Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
* Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.

### Why do we use them?
1. Hold unique values
2. Dictionary
3. Library

### What Are they
Hash tables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.

### Structure

* Hashing:

    Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

* Creating a Hash
    A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:
        * Add or multiply all the ASCII values together.
        * Multiply it by a prime number such as 599.
        * Use modulo to get the remainder of the result, when divided by the total size of the array.
        * Insert into the array at that index.

### Hash function:

* To achieve a good hashing mechanism, It is important to have a good hash function with the following basic requirements:
    1. Easy to compute: It should be easy to compute and must not become an algorithm in itself.

    2. Uniform distribution: It should provide a uniform distribution across the hash table and should not result in clustering.

    3. Less collisions: Collisions occur when pairs of elements are mapped to the same hash value. These should be avoided.

### Double hashing

* Double hashing is similar to linear probing and the only difference is the interval between successive probes. Here, the interval between probes is computed by using two hash functions.

* Let us say that the hashed index for an entry record is an index that is computed by one hashing function and the slot at that index is already occupied. You must start traversing in a specific probing sequence to look for an unoccupied slot.

