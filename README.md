# Eclipse-Bitz-MIning
### Eclipse $BITZ Mining: A Step-by-Step Guide

This guide will walk you through the process of setting up $BITZ mining on Eclipse, using your CPU (not GPU). Whether you're running this on a local machine, a VPS, or an Ubuntu instance, the steps will be the same.

### Prerequisites:
- **Rust**: For installing and running Bitz CLI.
- **Solana CLI**: To interact with the Solana blockchain.
- **$ETH**: A minimum of 0.005 ETH (approximately $10) is required for mining.

---

### 1. Install Rust

To begin, you need to install Rust. Run the following command to do so:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Follow the prompts during installation. Once it's done, update your environment by running:

```bash
source $HOME/.cargo/env
```

---

### 2. Install Solana CLI

Next, install the Solana CLI by running this command:

```bash
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```

---

### 3. Create a Wallet (Keypair)

Now, create a new Solana wallet by running:

```bash
solana-keygen new
```

You'll be asked to set a passphrase for better security (or you can skip by pressing enter).

This will generate a new keypair at the default path: `~/.config/solana/id.json`.

Make sure to **save your public key and mnemonic** (the secret phrase shown after creation) as they will be crucial for accessing your wallet.

---

### 4. Install Bitz CLI

Now that Rust is installed, you can install Bitz CLI with the following command:

```bash
cargo install bitz
```

---

### 5. Change RPC URL

Set the Solana RPC URL to the Eclipse network by running:

```bash
solana config set --url https://mainnetbeta-rpc.eclipse.xyz/
```

---

### 6. Open Screen Session

To keep your mining process running in the background, open a new screen session:

```bash
screen -S eclipse
```

---

### 7. Start eMining

To begin mining, run the following command:

```bash
bitz collect
```

**Note**: You will need at least **0.005 ETH (approximately $10)** on Eclipse to start mining. You can send the ETH to your public key to fund your account.

---

### Other Useful Commands:

- **Claim your Bitz**:  
  ```bash
  bitz claim
  ```

- **Check your balance**:  
  ```bash
  bitz account
  ```

- **Configure CPU usage**:  
  Change the number of CPU cores to be used by running:  
  ```bash
  bitz collect --cores 8
  ```
  (Replace "8" with the number of cores you want to allocate for mining).

- **View all commands**:  
  ```bash
  bitz -h
  ```

---

### 8. Import to Backpack

To import your Solana wallet into Backpack, follow these steps:

1. Get the path of your Keypair by running:
   ```bash
   solana config get
   ```

2. Copy the path of the Keypair.

3. View your keypair in array format:
   ```bash
   cat <Keypair path>
   ```

4. Copy the array of numbers and import them into Backpack under the "private key" section.

---

### Conclusion

You are now set up to start mining $BITZ on Eclipse! This setup uses CPU power, so you don’t need a GPU to participate. With a small initial investment of 0.005 ETH ($10), you can begin collecting Bitz and see your rewards grow over time.

Feel free to reach out if you encounter any issues during setup or have further questions. Happy mining!
