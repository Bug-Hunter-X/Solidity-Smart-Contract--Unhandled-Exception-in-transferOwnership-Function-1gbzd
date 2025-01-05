# Solidity Smart Contract Bug: Unhandled Exception in transferOwnership Function

This repository demonstrates a common bug in Solidity smart contracts: an unhandled exception in the `transferOwnership` function.  The bug occurs when the contract attempts to transfer ownership to an invalid address (e.g., the zero address).  This can lead to unexpected behavior or complete failure of the contract.

The bug is demonstrated in `transferOwnershipBug.sol`. The solution, which adds robust input validation, is provided in `transferOwnershipSolution.sol`.

**Bug:** The original `transferOwnership` function does not properly handle the case where `newOwner` is the zero address.  This can lead to an exception and contract failure.

**Solution:** The improved `transferOwnership` function includes a check to ensure `newOwner` is not the zero address before proceeding with the ownership transfer.