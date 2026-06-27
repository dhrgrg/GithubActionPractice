uses: actions/upload-artifact@v4
Take files generated during this workflow and store them in GitHub as artifacts so they can be downloaded later or used by another job.

Example:
steps:
  - uses: actions/checkout@v4

  - run: |
      mkdir output
      echo "hello" > output/result.txt

  - uses: actions/upload-artifact@v4
    with:
      name: build-output  # The name of the downloadable zip
      path: output/       # The folder or file you want to upload