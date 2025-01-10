name: Run Telegram Music Bot

on:
  workflow_dispatch:  # Manually trigger the workflow

jobs:
  run-bot:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.9'

      - name: Install dependencies
        run: |
          pip install -r requirements.txt

      - name: Run the bot
        run: |
          python src/bot.py  # Replace with the correct path to your bot's main file
          
