# VAN-Blockchain

## Proof of Work (PoW) Algorithm

- Start with a Nonce Value of 1

- Calculate the SHA256 hash of the squared distance between the nonce of the current block and the nonce of the previous block.

- Check if the first 4 characters of the calculated hash are zeros.

- If the first four characters are not zeros, increment the nonce value by 1 and repeat steps 2 and 3.

- If the first four characters are zeros, stop the process. The nonce value that results in this hash is the one that satisfies the condition, and it will be used for the next block.


## API endpoints

<!-- - `XYZ/mine_block` (GET request): Creates a node for user XYZ and contains SHA256 hash of the previous node. Also contains transaction details stored in that particular block.

- `XYZ/get_chain` (GET request) : Returns the chain and chain length for user XYZ in JSON format.

- `XYZ/is_valid` (GET request) : Returns whether the blockchain is valid. (Checks proof of work for all nodes)

- `XYZ/add_transaction` (POST request) : Add the transaction in the block for user XYZ.

- `XYZ/replace_chain` (GET request) : Replace the chain for the user XYZ with the longest chain to ensure consistency across all chains. (Ensures consensus) -->

- **Mine Block (GET):**
   - Endpoint: `/XYZ/mine_block`
   - Creates a new block for user XYZ, including transaction details, and computes the SHA256 hash of the previous block for linking.

- **Get Chain (GET):**
   - Endpoint: `/XYZ/get_chain`
   - Retrieves the blockchain and its length for user XYZ in JSON format.

- **Check Validity (GET):**
   - Endpoint: `/XYZ/is_valid`
   - Verifies the validity of the blockchain for user XYZ by checking the proof of work for all blocks.
- **Replace Chain (GET):**
   - Endpoint: `/XYZ/replace_chain`
   - Replaces the blockchain for user XYZ with the longest valid chain to ensure consistency and achieve consensus.

- **Add Transaction (POST):**
   - Endpoint: `/XYZ/add_transaction`
   - Parameters: Transaction details in the request body (sender, receiver, amount, etc.)
   - Adds a new transaction to the block for user XYZ.



## Steps to Run Code

- Install Django 2.2.6 : ```pip install django==2.2.6```

- Enter PyChain folder : ```cd PyChain```

- Create user at port XYZ : ```python manage.py runserver XYZ```

- Use any API Client (HTTPie, Postman, etc) to send and visualise responses for the above mentioned API endpoints.

<hr>

### Work Distribution
- Varun Nagpal : 
    - Consensus of nodes
    - Django API endpoints
- Anant Kacholia : 
    - Validation/Addition of transactions
    - Proof of work Algorithm
- Nishchay Nilabh : 
    - Blockchain class structure
    - Django API endpoints


