# GoogleAnalytics

Programmatic way to dump data from Google Analytics using Python.

## Setup

You need to perform the following steps on the Google console to enable programmatic access to Google Analytics:

1. Go to [Google developer's console](https://console.developers.google.com/iam-admin/projects) to create a new project.
1. Name it say `Google-Analytics`.
1. With `Google-Analytics` selected as the project, go to the top-left corner and select **API Manager** on the menu.
1. Select **API Manager > Dashboard**, select the **ENABLE API** button and then enter **Google Analytics Reporting API**
1. Select **Create Credentials**, select **OAuth client ID**.
1. Select **Configure consent screen** and enter the following:
  1. **Email address:** <Default selection>
  1. **Product name show to users:** Google Analytics
  1. **Homepage URL:** <Leave it blank>
  1. **Product logo URL:** <leave it blank>
  1. **Privacy policy URL:** <leave it blank>
  1. **Terms of service URL:** <leave it blank>
1. On the next page, select **Other** as the application type, and enter Script as the name.
1. Download the OAuth client secret file as rename it to `client_secrets.json`.

Once you have the project and credentials set up, do the following on the client:

1. Install the Google API Python package. Run `pip install google-api-python-client`.
1. Put the downloaded `client_secrets.json` in the project root directory.
1. Go to [Account Explorer](https://ga-dev-tools.appspot.com/account-explorer/) to find the view ID to replace the value of VIEW ID in `config.json.example`.
1. Rename `config.json.example` to `config.json`.

## Reference

* [Hello Analytics Reporting API v4](https://developers.google.com/analytics/devguides/reporting/core/v4/quickstart/installed-py)