# BuildingBlocks

m = message

H(m) = message digest

SHA-256 hash function (used by bitcoin) :
- breaks message down to blocks of 512 bits in size;
- pad the message so that it's length is an exact multiple of the 512 bit block size;
- compression function => 256 bits (single iteration)

linked list (build with hash pointers)
- blocks with data, and a point to the previous block
- tamper evident log

Merkel tree
- made with binary search built with hash pointers
- log time membership proofs
- as long as data is acyclic (must be directed acyclic)

** show O(log n) items

Digital signature scheme:
- valid messages are varifiable
- attacker has negligible chance of forging a signature successfully (regardless of what algorithm they use)
- ECDSA used by bitcoin (eliptical curve digital signature algorithm)

** sign a hash pointer: signature covers the whole structure;

good source of randomness (bad randomness = insecure signature)

limit on message size

Double Spend attack
(the main design challenge in digital currency)

transaction type
- createCoins
- payCoins

payCoins transaction is valid if
0. the consumed coins are valid
1. the consumed coins were not already consumed (double spend)
2. total value out = total value in
3. signed by owners of all consumed coins

Coins are immutable:
- never changed
- never subdivided
- never combined
** created in one transaction and consumed in another transaction;





























