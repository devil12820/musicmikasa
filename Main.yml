name: Deploy Telegram Music Bot

on:
  push:
    branches:
      - main
  workflow_dispatch:

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Code
        uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: "3.10"

      - name: Install Dependencies
        run: |
          pip install -r requirements.txt

      - name: Run Bot
        env:
          API_ID: ${{ secrets.API_ID }}
          API_HASH: ${{ secrets.API_HASH }}
          BOT_TOKEN: ${{ secrets.BOT_TOKEN }}
          MONGO_DB_URI: ${{ secrets.MONGO_DB_URI }}
          OWNER_ID: ${{ secrets.OWNER_ID }}
          STRING_SESSION: ${{ secrets.STRING_SESSION }}
        run: |
          python main.py
          
