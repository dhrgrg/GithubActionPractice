 It downloads previously uploaded artifacts from GitHub artifact storage into the runner filesystem.

  deploy:
    needs: build                        # Imp to mention this since this job depends on build artifacts first
    runs-on: ubuntu-latest
    steps:
      - uses: actions/download-artifact@v4  # Download uploaded artifacts
        with:
          name: build-files

