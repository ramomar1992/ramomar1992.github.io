# Hash Tables

When we hash some kind of data, we transform the data into another type of data that could be used for multiple purposes suck as security and storing data. When we hash something, it is impossible for us to reverse the process and return it to its precious or original state.

Hash tables consist of an array that serve as a mapping table. Each element in the array contains a list of elements known as buckets, which could hold any data type. It is mainly used to store data in the form of key/value pairs.

Each bucket may contain more than one element, but the best hash table whose buckets has at most one element. To reach an optimal hash table we have to build out hashing function that is very unlikely to produce the same hash index for any two data values. In contrast, we can have multiple approaches to optimize the hashtable if that is inevitable. 

Hash table are very efficient in terms of time when we want to look up a special data from the table. The average time complexity for this process is mostly O(1). Therefore it is one of the most efficient data types. However, sometimes we can have tables that hash al the inputted data to the same hash index. This is the worst case scenario that might happen. In this case the searching time complexity will be O(1).

## Structure

### Hashing

Basically, a hash code turns a key into an integer. It’s very important that hash codes are deterministic: their output is determined only by their input. Hash codes should never have randomness to them. The same key should always produce the same hash code.

#### Creating a Hash

A hashtable traditionally is created from an array. I always like the size 1024. this is important for index placement. After you have created your array of the appropriate size, do some sort of logic to turn that “key” into a numeric number value. Here is a possible suggestion:

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.

### Collisions

A collision occurs when more than one key hashes to the same index in an array. As mentioned earlier, a “perfect hash” will never have any collisions. To put this into perspective, the worst possible hash is one that hashes every single key to the same exact index of an array. The more keys you have hashed to a specific index, the more key/value pair combos you can potentially have.

What would happen if two different keys resolved to be the same index of the array? This is called a collision. The hash map needs to be able to handle two keys resolving to the same index.

Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a LinkedList in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. Each index in the array is called a “bucket” because it can store multiple key/value pairs.

## Bucket Sizes

Hash Maps can have any number of buckets. If a hash map has only a few buckets it will be densely full and have many collisions. If a hash map has more buckets it will be more sparsely populated, there will be less collisions, but there may be a lot of extra empty space.

It’s possible to compute the “load factor” of a hash table. The load factor tells us something about how full the hash table is. A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data.