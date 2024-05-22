### Stellar NFT Smart Contract System Overview

This repository houses a collection of Rust smart contracts tailored for the Stellar Blockchain, with a focus on Non-Fungible Tokens (NFTs). Below is an elaboration on the project's structure and functionalities:

#### Project Structure
- **src folder**: Contains several Rust smart contracts.
- **Cargo.toml**: Rust project configuration file.

#### Contract Functionalities

**admin.rs**
- **has_administrator(env: &Env) -> bool**: Checks for the presence of a system administrator by querying the storage.
- **read_administrator(env: &Env) -> Identifier**: Reads and returns the administrator's identifier from the storage.
- **write_administrator(env: &Env, id: Identifier)**: Writes the provided administrator's identifier to the storage.
- **check_admin(env: &Env, auth: &Signature)**: Verifies if a given authentication signature corresponds to the system's administrator.

**approval.rs**
- **read_approval(env: &Env, id: i128) -> Identifier**: Reads and returns the approval identifier for a specific action.
- **read_approval_all(env: &Env, owner: Identifier, operator: Identifier) -> bool**: Checks if a specific operator has approval from a specific owner for all actions.
- **write_approval(env: &Env, id: i128, operator: Identifier)**: Writes the approval identifier for a specific action.
- **write_approval_all(env: &Env, owner: Identifier, operator: Identifier, approved: bool)**: Writes the approval status for all actions from a specific owner to a specific operator.

**balance.rs**
- **read_balance(env: &Env, owner: Identifier) -> i128**: Reads and returns the balance of a specific owner.
- **write_balance(env: &Env, owner: Identifier, write_type: WriteType)**: Writes the balance of a specific owner based on the provided write_type.
- **read_supply(env: &Env) -> i128**: Reads and returns the total supply.
- **increment_supply(env: &Env)**: Increments the total supply.
- **read_minted(env: &Env, owner: Identifier) -> bool**: Reads and returns whether the specific owner has been minted.
- **write_minted(env: &Env, owner: Identifier)**: Sets the minted status for the specific owner.
- **check_minted(env: &Env, owner: Identifier)**: Checks if the specific owner has already been minted.

**contract.rs**
- This function acts as the main entry point, housing all basic NFT operations from minting to transfer.

**event.rs**
- Publishes various events such as transfers, admin changes, minting, burning, and approvals.

**interface.rs**
- Provides a comprehensive description of contract interfaces.

**lib.rs**
- Implements a modular NFT system suitable for various environments.

**metadata.rs**
- Manages token metadata including names, symbols, and URIs.

**owner.rs**
- Manages token ownership and zero addresses for non-existent owners.

**storage_types.rs**
- Defines contract types for streamlined approval and data key management.

#### Compiling the Contracts
1. Set up Soroban CLI following the instructions [here](https://soroban.stellar.org/docs/getting-started/setup).
2. For Windows users wanting to leverage Linux, refer to this [video guide](https://www.youtube.com/watch?v=PQA5_7m3OjQ&t=2s).
3. After setting up Soroban CLI, execute `soroban contract build`.
4. Upon compilation, locate the generated **‘target’** folder containing the wasm executable.

These contracts offer a solid foundation for NFT management on the Stellar Blockchain, providing flexibility, security, and adherence to industry standards.
