Bloomfilter is a quick way to check whether a object is contained in the data structure or not.

## Hashing

A hash is like a fingerprint for data. A hash function takes your data — which can be any length — as an input, and gives you back an identifier of a smaller (usually), fixed (usually) length, which you can use to index or compare or identify the data.

Most hash functions are one-way operations, which is to say you can figure out an identifier from the data, but you typically can’t do the reverse. Reversible hash functions do exist, but they tend to be pretty trivial, and not particularly useful.

### Hash Function
1. Same input must always hash to the same output.
2. Ideally, the output values should be distributed uniformly ---- that is, each possible output should be equally likely.
3. Finally, in most cases (though not always), you want it to be fast.

Greenspun's tenth rule

Timsort, Stoogesort and Smoothsort 

## Bloom Filter
Hashes the object throuth several Hash Functions, marks the position to be one or total number of objects has been hashed to this position regarding to the object.
Bloom filters can very quickly answer variations on the Yes/No question “is this item in the set?”, like “have I seen this item before?”. 

There are two important caveats though. Very rarely:
1. It will say Yes when the answer is actually No (although it will never say No, when the answer is actually Yes). 
2. You also can’t remove an item from a Bloom filter. Like elephants and unrelenting Polish designers, Bloom filters never forget.

For the hash functions that Bloom filters use, collisions in the outputs don’t really matter too much, as long as they’re reasonably rare. It’s more important for the outputs to be evenly and randomly distributed. And, of course, we want our hash functions to be fast.

## Recommendation System
You want to be able to quickly exclude posts that a user has read, so that you don’t suggest those posts again. And a Bloom filter is a good fit for this problem, because it will never let through a post that the user has read, and even though it might exclude a post that they haven’t read, that’s ok because they’ll never know what they don’t see? And it’s very fast?

### Reference:
  * https://blog.medium.com/what-are-bloom-filters-1ec2a50c68ff
