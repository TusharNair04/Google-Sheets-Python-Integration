
# Google Sheets API Data Fetcher

This Python script demonstrates how to authenticate with the Google Sheets API, fetch data from a specific spreadsheet, and load it into a pandas DataFrame.

## Features

- Fetches data from a specified range within a Google Sheet.
- Uses OAuth2 for authentication, supporting both token refresh and new token generation.
- Loads data directly into a pandas DataFrame, ready for data analysis or processing.

## Prerequisites

- Python 3.x
- A Google Cloud Platform project with the Sheets API enabled.
- OAuth 2.0 Client IDs configured and downloaded as a JSON file.

## Dependencies

Install the necessary Python libraries using pip:

```bash
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib pandas
```

## Configuration

1. **OAuth 2.0 Client JSON**:
   - Download your OAuth 2.0 Client JSON file from the Google Cloud Console and place it in your project directory.
   - Update `path_to_OAUTH_JSON_FILE` with the path to this file.

2. **Spreadsheet ID**:
   - Find the ID of the spreadsheet you want to access; it's the long string in the spreadsheet's URL.
   - Replace `YOUR_SPREADSHEET_ID` with your actual spreadsheet ID.

## Token Generation

- On the first run, the script will open a new browser window asking you to log in with your Google account and authorize access.
- After granting access, a `token.json` file is generated and saved in your project directory. This token will be reused in future script executions for authentication.

## Usage

- Ensure the `credential_path` and `spreadsheet_id` are correctly set in the script.
- Run the script. It will authenticate, fetch the data, and load it into a DataFrame.

## Customization

- Modify the `range` parameter in the `service.spreadsheets().values().get()` method call to fetch data from different sheets or ranges within your spreadsheet.

## Contributing

Feel free to fork the repository and submit pull requests to improve the script or extend its functionality.
