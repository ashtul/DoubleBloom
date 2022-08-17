August 17th, 2022
A few days after Filipe's wedding.

`Double Bloom Filter` has twice the hash functions and twice the size a regular `Bloom Filter` with comparable `error-rate` and `number of elements`.

On `insert`, every element uses twice the number of `hash functions` to set on `2*k` bits on. 
During a `full cycle` of `window slide`, half the filter is reset. The reset occurs in small `batches` in `intervals`.
When the Filter has query for an element all `2*k` hash functions values are calculated but only those that haven't been cleared in the last cycle are counted.
Error-rate is similar to that of half filter with `k` hash functions. 