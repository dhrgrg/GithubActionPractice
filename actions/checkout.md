# creating practice of github actions for my learning

uses: actions/checkout@v4
=> Run the official checkout action to download (clone) my repository code into the runner machine.

example:
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: ls -la