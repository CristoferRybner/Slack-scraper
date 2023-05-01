# Slack LinkedIn Scraper

This script extracts LinkedIn profile links shared by users in a specific Slack channel and saves the data to a CSV file. The CSV file will contain the name of the person and their LinkedIn profile link.

## Requirements

- Python 3.6+
- `slack_sdk` package
- A Slack bot token

## Installation

1. Make sure you have Python 3.6 or newer installed on your system. You can download it from https://www.python.org/downloads/.

2. Install the required package `slack_sdk` by running:

```bash
pip install slack_sdk
```

## Configuration

1. Create a new Slack bot or use an existing one, and obtain the bot token. To create a new bot, follow the instructions in the official Slack API documentation: https://api.slack.com/bot-users.

2. Set the `SLACK_BOT_TOKEN` environment variable with your bot token. You can do this in your terminal or add it to your environment variables.

For example, in the terminal (replace `your_bot_token` with your actual token):

```bash
export SLACK_BOT_TOKEN="your_bot_token"
```

3. Open the script and replace the `channel_name` variable with the name of the Slack channel you want to scrape.

```python
channel_name = "your_channel_name"  # Replace with the name of the channel
```

## Usage

1. Make sure the bot is a member of the channel you want to scrape.

2. Run the script using the following command:

```bash
python slack_linkedin_scraper.py
```

3. The script will fetch messages from the specified channel, parse the messages for LinkedIn profile links, and save the extracted data in a CSV file named `linkedin_data.csv`. The CSV file will be located in the same directory as the script.

## Troubleshooting

If you encounter any issues, check the following:

- Ensure that the bot token is set correctly in the environment variable.
- Make sure the bot is a member of the channel you want to scrape.
- Check the specified channel name in the script to ensure it matches the actual channel name.

If you still encounter issues, check the error messages for more details and refer to the Slack API documentation for additional guidance: https://api.slack.com/.
