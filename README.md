# Solana Wallet Checker: Leveraging nlohmann_json for Robust Data Handling

**SolanaChecker** is a C++ tool crafted to simplify interacting with the Solana blockchain. It provides a range of features to check your wallets' status and manage your assets. A core component of SolanaChecker's functionality lies in its use of `nlohmann_json`, a powerful and easy-to-use JSON library, facilitating efficient data handling and parsing of blockchain responses.

<p align="left">
    <img src="/image/line.webp" />
</p>

## Program Features, Enhanced by `nlohmann_json`

1.  **Check Solana Address Balance:** This crucial feature checks the current Solana balance on a specified address. This allows users to easily track funds. `nlohmann_json` plays a key role in parsing and presenting balance data.

<p align="left">
    <img src="/image/picture.webp" />
</p>

2.  **Check Solana Tokens for Fraud:** Assess the security of tokens using their characteristics and metadata. This includes using `nlohmann_json` to handle the analysis.

<p align="left">
    <img src="/image/pool.webp" />
</p>

3.  **Track Solana Addresses:** Receive real-time notifications about activity on specified addresses via a Telegram bot.

4.  **Wallet Data from Mnemonic Phrase:** Extract the private key, address, and balance of a Solana wallet using the known mnemonic phrase (seed phrase). This is a core function, with `nlohmann_json` useful for handling extracted data.

<p align="left">
    <img src="/image/center.webp" />
</p>

5.  **Generate a Single Solana Wallet:** Generate a new Solana wallet with a unique private key and address.

<p align="left">
    <img src="/image/temp.webp" />
</p>

6.  **Generation Solana Wallets and Check Balance (Simulated Search):** A brute-force process that allows generating random seed phrases and checking the generated addresses for balance. *This is for educational purposes only*. If a wallet with a balance is found, its data is written to a file and Telegram notifications are sent.

<p align="left">
    <img src="/image/shell.webp" />
</p>

## Setting Up Telegram (for Notifications)

Configure the program for Telegram notifications by adding your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) in the 'telegram-settings.txt' file. This allows the bot to send notifications on wallet activity.

## Getting Started: Download or Build

Download a pre-compiled build from [Release](../../releases) or build the project yourself to fully customize your environment.

## Building the Project & the Importance of `nlohmann_json`

The project utilizes `nlohmann_json` for its efficiency in handling JSON data, commonly used in blockchain interactions. Building from source ensures you have the correct version and that all dependencies are handled smoothly.

### Installing Dependencies with vcpkg:

1.  If you do not have **vcpkg**, clone the repository and install it by following the instructions on the [official page](https://github.com/microsoft/vcpkg).

2.  Add vcpkg to your system PATH environment variable.

3.  Run the following commands in your terminal:

    -   Install **OpenSSL**:
        ```bash
        vcpkg install openssl
        ```

    -   Install **nlohmann-json**:
        ```bash
        vcpkg install nlohmann-json
        ```

    -   Install **Crypto++**:
        ```bash
        vcpkg install cryptopp
        ```

    -   Install **libsodium**:
        ```bash
        vcpkg install libsodium
        ```

4.  After this step, you are ready to build the project.

### Building via Visual Studio:

1.  Open the project solution in Visual Studio.
2.  Make sure **vcpkg** is correctly integrated with your environment.
3.  Click **Build** -> **Build Solution**.
4.  The executable is located in the `bin` folder.

### Building with Another C++ Compiler:

1.  Ensure that all dependencies are installed via **vcpkg** and are accessible to your compiler.
2.  Compile the project using the following command (adapt as necessary):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line

Use the command-line arguments to use the program's functionality:

1.  **-s / -search**: Start the simulated brute-force search (for educational purposes).
2.  **-t / -track (ADDRESS)**: Start tracking the specified address.
3.  **-g / -gen (NUMBER)**: Generate the specified number of Solana wallets.
4.  **-m / -mnemonic (MNEMONIC)**: Display wallet information using the seed phrase.
5.  **-b / -balance (ADDRESS)**: Display the balance of the specified address.

## Notes

-   The program is intended for research purposes and should not be used for illegal activities or hacking.
-   All operations with cryptocurrencies may carry risks.
-   Use `nlohmann_json` safely and responsibly.

## License

This project is licensed under the [MIT License](/LICENSE).

Update: URL refresh