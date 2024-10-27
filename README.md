
# SeleniumScripts

A collection of Python functions and scripts designed for automating web interactions using Selenium. This repository contains reusable and modular functions for common automation tasks like clicking input fields, entering text, extracting information from pages, and sending messages or images to a Telegram channel.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [Clicking Input Fields](#clicking-input-fields)
  - [Entering Text](#entering-text)
  - [Interacting with Checkboxes and Buttons](#interacting-with-checkboxes-and-buttons)
  - [Extracting Information](#extracting-information)
  - [Sending Messages to Telegram](#sending-messages-to-telegram)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/hitthecodelabs/SeleniumScripts.git
   cd SeleniumScripts
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   Ensure you have **Selenium** and **Requests** installed. Additionally, download the appropriate WebDriver (e.g., ChromeDriver, GeckoDriver) based on your browser.

## Usage

### Clicking Input Fields

- **`click_username_field(driver)`**: Clicks on the username input field.
- **`click_password_field(driver)`**: Clicks on the password input field.

### Entering Text

- **`enter_username_text(driver, username="jeapapan")`**: Enters the given username into the username input field.
- **`enter_password_text(driver, password="gt5hy6JU7.5")`**: Enters the given password into the password input field.

### Interacting with Checkboxes and Buttons

- **`click_remember_me_checkbox(driver)`**: Clicks the 'Remember Me' checkbox.
- **`click_login_button(driver)`**: Clicks the 'LOGIN' button.
- **`click_calendar_link(driver)`**: Clicks on the 'Calendar' link.
- **`click_agenda_button(driver)`**: Clicks on the 'Agenda' button.

### Extracting Information

- **`extract_assignments(driver)`**: Extracts assignments with 'Due Date' information from the calendar agenda.
- **`extract_assignments_with_dates(driver)`**: Extracts assignments along with their respective due dates and times.

### Sending Messages to Telegram

- **`send_message_to_telegram_channel(bot_token, channel_id, message_text)`**: Sends a text message to a Telegram channel using a bot token.
- **`send_image_to_telegram_channel(bot_token, channel_id, image_path, caption=None)`**: Sends an image to a Telegram channel using a bot token.

## Examples

```python
from selenium import webdriver
from SeleniumScripts import click_username_field, enter_username_text, click_login_button

# Set up the Selenium WebDriver
driver = webdriver.Chrome()

# Open a website and perform actions
driver.get("https://example.com/login")

# Click on the username field and enter text
click_username_field(driver)
enter_username_text(driver, "my_username")

# Perform other actions like clicking the password field, entering text, and logging in
# ...
click_login_button(driver)
```

### Sending a Telegram Message

```python
from SeleniumScripts import send_message_to_telegram_channel

# Define your bot token and channel ID
bot_token = "YOUR_TELEGRAM_BOT_TOKEN"
channel_id = "@your_channel_id"

# Send a message
send_message_to_telegram_channel(bot_token, channel_id, "Hello from SeleniumScripts!")
```

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request for bug fixes, improvements, or new features.

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
