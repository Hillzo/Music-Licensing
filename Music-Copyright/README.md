# Music Royalty Distribution Smart Contract

## Overview

This smart contract is designed to manage music royalty distributions on the Stacks blockchain, providing a transparent and automated system for tracking and distributing royalties to music rights holders.

## Features

### Key Functionalities
- Register new music tracks
- Set royalty allocations for rights holders
- Process royalty payments
- Manage track status
- Transfer contract ownership

### Core Components
- Music Catalog: Tracks details about registered songs
- Royalty Allocations: Manages percentage-based royalty distribution
- Validation Mechanisms: Ensures data integrity and security

## Error Handling

The contract includes comprehensive error handling with specific error codes:
- `ERR-UNAUTHORIZED-ACCESS (u100)`: Unauthorized contract interactions
- `ERR-INVALID-ROYALTY-PERCENTAGE (u101)`: Invalid royalty percentage
- `ERR-DUPLICATE-SONG-ENTRY (u102)`: Attempted duplicate song registration
- `ERR-SONG-NOT-FOUND (u103)`: Song not in catalog
- `ERR-INSUFFICIENT-PAYMENT (u104)`: Insufficient funds for royalty payment
- `ERR-INVALID-RECIPIENT (u105)`: Invalid royalty recipient
- `ERR-PAYMENT-DISTRIBUTION-FAILED (u106)`: Royalty distribution failure

## Contract Functions

### Administrative Functions
- `register-track`: Add a new music track to the catalog
- `set-royalty-allocation`: Define royalty percentages for rights holders
- `update-track-status`: Activate or deactivate tracks
- `transfer-ownership`: Change contract administrator

### Payment Functions
- `process-royalty-payment`: Distribute royalties among rights holders
- Supports automatic percentage-based royalty distribution

## Usage Requirements

### Prerequisites
- Contract owner must register tracks
- Royalty allocations must be set before processing payments
- Payments distributed proportionally based on predefined percentages

### Validation Checks
- Royalty percentages must be between 0-100%
- String inputs have length restrictions
- Rights holders cannot be the contract owner or transaction sender

## Security Considerations
- Owner-only administrative functions
- Strict validation of input parameters
- Prevents unauthorized access and manipulation

## Example Workflow
1. Contract owner registers a track
2. Set royalty allocations for artists, producers, etc.
3. Receive royalty payments
4. Automatically distribute funds to rights holders

## Deployment
- Deployed on the Stacks blockchain
- Requires STX for transaction fees
- Initial contract owner is the transaction sender

## Limitations
- Maximum song title length: 50 characters
- Maximum participant role length: 20 characters
- Requires manual royalty allocation setup

## Development
- Developed in Clarity language
- Designed for transparency and automated royalty management