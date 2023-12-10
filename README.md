# Weather Logger

This repository contains a Python script (main.py) that retrieves weather information for Burlingame, CA, using the Talk Python Weather API. The script is scheduled to run daily at midnight using GitHub Actions. The obtained weather data is logged to a file (status.log), and the log is committed and pushed to the main branch.

## Requirements

Ensure you have the required Python packages installed by running:

```bash
pip install -r requirements.txt
```

## Configuration

(Optional) Before running the script, make sure to set up the following environment variable:

- SOME_SECRET: A secret token required for the script. You can set this as a GitHub secret.

## GitHub Actions

The GitHub Actions workflow is defined in `.github/workflows/actions.yml`. It is scheduled to run the script daily at midnight. The workflow includes the following steps:

1. Checkout repository content.
2. Set up Python environment.
3. Install required Python packages.
4. Execute the Python script (main.py), providing the SOME_SECRET environment variable.
5. Commit any changes to the repository.
6. Push the changes to the main branch.
