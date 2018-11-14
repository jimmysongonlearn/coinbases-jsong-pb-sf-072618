
# Coinbase Transaction

All transactions on the Bitcoin network are not created equally. A coinbase transaction is a unique type of Bitcoin transaction that can only be created by a miner. This type of transaction has no inputs, and there is one created with each new block that is mined on the network. In other words, this is the transaction that rewards a miner with the block reward for their work. Any transaction fees collected by the miner are also sent in this transaction. [Credit](https://blog.cex.io/bitcoin-dictionary/coinbase-transaction-12088)

### Test Driven Example


```python
from io import BytesIO
from tx import Tx
from helper import little_endian_to_int

class Tx(Tx):
    
    def is_coinbase(self):
        '''Returns whether this transaction is a coinbase transaction or not'''
        # check that there is exactly 1 input
        # grab the first input
        # check that first input prev_tx is b'\x00' * 32 bytes
        # check that first input prev_index is 0xffffffff
        pass
```
