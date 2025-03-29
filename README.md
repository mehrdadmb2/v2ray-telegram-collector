
# V2Ray Telegram Collector 🚀🔧

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/Python-3.7%2B-blue.svg)](https://www.python.org/)
[![GitHub stars](https://img.shields.io/github/stars/mehrdadmb2/v2ray-telegram-collector?style=social)](https://github.com/mehrdadmb2/v2ray-telegram-collector/stargazers)

---

## Overview ✨

**V2Ray Telegram Collector** is an open-source Telegram user-bot designed to automatically collect the latest V2Ray configuration files from specified Telegram channels. It then stores these configurations in a text file and updates this file on GitHub in real-time. This project offers an elegant solution for users who need to subscribe to up-to-date VPN settings with ease.

---

## Features 🌟

- **Automated Config Collection:**  
  Automatically monitors selected Telegram channels to fetch the latest V2Ray configurations.
  
- **Real-Time GitHub Updates:**  
  The collected configurations are stored in a `configs.txt` file which is updated on GitHub with every new config received.
  
- **User-Friendly Subscription:**  
  Share a raw GitHub link for users to subscribe and receive automatic updates in their VPN applications.
  
- **Open-Source & Community Driven:**  
  Contribute, modify, and improve the bot according to your needs!

---

## Table of Contents 📚

- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Installation 🛠️

### Prerequisites

- Python 3.7 or higher
- A Telegram account with access to the desired channels
- GitHub account with a repository ready for updates

### Steps

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/mehrdadmb2/v2ray-telegram-collector.git
   cd v2ray-telegram-collector
   ```

2. **Create and Activate a Virtual Environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate   # For Linux/macOS
   # or
   venv\Scripts\activate      # For Windows
   ```

3. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

---

## Configuration ⚙️

Before running the bot, set up your configuration:

1. **Telegram API Credentials:**  
   Get your `API_ID` and `API_HASH` from [my.telegram.org](https://my.telegram.org) (use VPN if necessary) and update the `config.py` file.

2. **GitHub Token and Repository:**  
   Create a personal access token on GitHub with the required permissions (repo access) and add the following details to `config.py`:
   - `GITHUB_TOKEN`
   - `GITHUB_REPO` (e.g., `mehrdadmb2/v2ray-telegram-collector`)
   - `GITHUB_FILE_PATH` (e.g., `configs.txt`)

3. **Channels to Monitor:**  
   In `main.py`, update the list of channels you wish to monitor by their usernames, e.g., `['@channel_username1', '@channel_username2']`.

---

## Usage 🚀

1. **Start the Bot:**

   ```bash
   python main.py
   ```

2. **How It Works:**  
   - The bot connects to Telegram using your credentials.
   - It monitors the specified channels for messages containing the keyword (e.g., "v2ray").
   - Upon receiving a valid config message, it appends the configuration to a list (ensuring only the latest 12 are kept).
   - The list of configs is then joined and pushed to your GitHub repository automatically.
   - Users can subscribe to the raw GitHub URL (e.g., `https://raw.githubusercontent.com/mehrdadmb2/v2ray-telegram-collector/main/configs.txt`) for up-to-date VPN settings.

3. **Logs:**  
   The terminal will display logs such as "Bot is running..." and "File updated on GitHub" to indicate the bot's operation.

---

## Contributing 🤝

We welcome contributions from the community! If you have suggestions, improvements, or fixes, please feel free to fork the repository and open a pull request.

- **Issues:**  
  Report bugs or feature requests via the [Issues](https://github.com/mehrdadmb2/v2ray-telegram-collector/issues) page.
  
- **Pull Requests:**  
  Ensure your code follows the project style and include relevant documentation with your PR.

---

## License 📄

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## Contact 📫

If you have any questions or need further assistance, feel free to reach out:

- **GitHub:** [mehrdadmb2](https://github.com/mehrdadmb2)
- **Telegram:** [@YourTelegramUsername](https://t.me/IIMehrdadII)

---

Happy Coding! 💻🎉
```
