
# list
1. one byte of memory has an address, one integer requires 4 bytes, 32 bits
2. programmer use programming language to talk to memory, address of the block of memory is the address of first byte
3. In C, array created using "malloc", we can use "realloc" to re-size it. Some memory block may be extended if space adjacent to the block is available.

# linked-list
1. one memory block saves value, one memory block saves address for next node
2. address of the hesd node gives us access of the complete list, tail address pointer will save 0/null
