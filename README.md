```markdown
# Solana Counter App

This repository contains a Solana-based counter application built using the following technologies:

- **Solana Wallet Adapter** ([@anza-xyz/wallet-adapter](https://github.com/anza-xyz/wallet-adapter))
- **Vite**: For fast and modern front-end development.
- **Anchor**: A framework for building Solana smart contracts.

## Features

- Connect to Solana wallets using Wallet Adapter.
- Read and write transactions on the Solana blockchain.
- Anchor-based backend for managing the counter state.
- Simple, modern front-end with React and Vite.

---

## Getting Started

### Prerequisites

Ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (version 16 or higher recommended)
- [Yarn](https://yarnpkg.com/)
- [Solana CLI](https://docs.solana.com/cli/install-solana-cli)
- Anchor CLI ([Installation Guide](https://book.anchor-lang.com/chapter_2/installation.html))

---

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/solana-counter-app.git
   cd solana-counter-app
   ```

2. Install dependencies:
   ```bash
   yarn install
   ```

---

### Environment Setup

1. Create a `.env` file in the root directory and add the following variables:
   ```env
   VITE_SOLANA_NETWORK=devnet
   VITE_SOLANA_RPC_ENDPOINT=https://api.devnet.solana.com
   ```

2. Replace `VITE_SOLANA_NETWORK` and `VITE_SOLANA_RPC_ENDPOINT` with your desired network and RPC endpoint if needed.

---

### Running the App

1. **Start the local development server**:
   ```bash
   yarn dev
   ```

2. Open your browser and navigate to `http://localhost:5173`.

---

### Smart Contract Deployment

1. Navigate to the Anchor project directory:
   ```bash
   cd anchor
   ```

2. Build the smart contract:
   ```bash
   anchor build
   ```

3. Deploy the smart contract to the Solana devnet:
   ```bash
   anchor deploy
   ```

4. Copy the program ID from the deployment output and update your client code if required.

---

### Folder Structure

```plaintext
.
├── anchor/                     # Smart contract code (Anchor framework)
├── src/                        # Frontend source code
│   ├── App.tsx                 # Main application component
│   ├── _app.tsx                # Wallet wrapper
│   ├── main.tsx                # Entry point
│   └── index.css               # Global styles
├── package.json                # Project dependencies and scripts
├── tsconfig.json               # TypeScript configuration
└── vite.config.ts              # Vite configuration
```

---

### Key Libraries Used

1. **[@anza-xyz/wallet-adapter](https://github.com/anza-xyz/wallet-adapter)**:
   - Handles wallet connections and provides a user-friendly interface for Solana wallets.

2. **Anchor Framework**:
   - Simplifies the development of Solana smart contracts.

3. **Vite**:
   - A modern build tool for lightning-fast development.

---

### Commands

- **Start Development Server**:
  ```bash
  yarn dev
  ```

- **Build Frontend**:
  ```bash
  yarn build
  ```

- **Deploy Smart Contract**:
  ```bash
  anchor deploy
  ```

---

### Troubleshooting

- Ensure your `solana config get` points to the correct cluster (`devnet`, `testnet`, or `mainnet-beta`).
- If wallet connection fails, verify your network and RPC endpoint settings in `.env`.

---

### Contributing

Contributions are welcome! Please fork the repository, make your changes, and submit a pull request.

---

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
```
