# readme
it is a Blockchain-based application designed to manage property transactions using digital currency. This system facilitates secure and transparent property trading through blockchain technology, ensuring data integrity with cryptographic methods like hash functions and Merkle trees.

Modules and Their Functionalities
1. block.py: Blockchain Management

Class BlockChain:
Manages the entire blockchain, maintaining a list of blocks and transactions.

- new_block(self, previous_hash=None, transaction=None):
Creates a new block with transactions, assigns a Merkle root, and computes the block's hash.
previous_hash: The hash of the previous block in the chain.
transaction: Optional transaction details to include in the block.

- hash(block):
Computes and returns a SHA-256 hash of the block.
block: The block data to hash.

- last_block(self):
Returns the most recent block in the blockchain.

- get_block(self, index):
Retrieves a block by its index in the chain.

- get_chain(self):
Returns the entire blockchain as a list of blocks.

2. hmac_.py: Security

Contains utilities to implement HMAC for securing transactions. It provides functions to generate and verify HMACs ensuring the authenticity and integrity of messages.

3. main.py: Main Application Entry

Serves as the entry point for running the application.
Initializes the blockchain and handles user interactions such as registering users, adding properties, and processing transactions.

4. merkle_tree.py: Merkle Tree Implementation

- Class MerkleTree:
Implements a Merkle tree to summarize and verify transaction data efficiently.

- getRootHash():
Calculates and returns the root hash of the Merkle tree, representing a summary of all transactions.

5. models.py: Data Models

- Class User:
Represents a user in the system with attributes like username, password, assets, and digital wealth.

- add_property(self, property):
Registers a new property to the user's list of assets.

- remove_property(self, property):
Removes a property from the user's assets and adjusts their digital wealth accordingly.

- Class Transaction:
Handles the logic for buying and selling properties between users.

- to_string(self):
Returns a string representation of the transaction details.

- Class Property:
Represents a property with attributes like name, owner, and value.

- register(self, owner):
Assigns an owner to the property and registers it in the blockchain.
