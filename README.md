
# GitHub App 


GitHub App using 

- Python 3.7
- `gidgethub` 
- `aiohttp`
- `pyjwt` 
- `cryptography`

See requirements.txt.

When the command line script is run, the GitHub App will open an issue in the repo.


## GitHub App Creation


1. Create a [GitHub App](https://github.com/settings/apps/new). Give it the necessary permission. Read and write access is needed to access Issues.

2. Have a user install the app.

3. Record the App ID. It can be found in the App's settings under "About" heading.

4. Generate a private key for the app [here](https://developer.github.com/apps/building-github-apps/authenticating-with-github-apps/#generating-a-private-key)


## Local environment setup


1. Install the dependencies, preferably using a virtual environment. For example:

   ```
   python3.7 -m venv venv
   source venv/bin/activate
   python -m pip install -U pip
   python -m pip install -r requirements.txt
   ```

2. Create the environment variable `GH_APP_ID`. (obtained from GitHub App Creation step 3 ).
   For example:

   ```
   export GH_APP_ID=1235
   ```

3. Create the environment variable `PEM_FILE_PATH```, that is the path to the private key
   file (downloaded in GitHub App Creation step 4). For example::

   ```
   export PEM_FILE_PATH=./my-app.2018-11-11.private-key.pem
   ```

4. Run the command line script:

   ```
   python3 __main__.py
   ```

