# Super.AI API client

The super.AI Python library provides access to the super.AI API via Python and our command line interface (CLI). Full details on our API for are listed in our [API reference](https://super.ai/reference).

In this README, you will find the following sections:

- [Installation](#installation)
- [CLI usage](#cli-usage)
- [CLI commands](#cli-commands)
- [Python usage](#python-usage)

## Installation

In your terminal, run:

```
pip install superai
```

### Requirements

- A super.AI account. You will need to provide your account's API key in order to use this client.
- Python 3.6 or later. On systems that have both Python 2 and Python 3 installed, you may need to replace the call to `pip`  with `pip3`.
- Dependencies in this package rely on the Clang build tools on MacOS. If you have recently updated or installed XCode, you may have to run `sudo xcodebuild -license` prior to installation.

## CLI usage

Installing the API client provides access to the `superai` command.

```
superai [command]

# Run `--help` for detailed information about CLI commands, including required and optional flags.
superai [command] --help
```

### Logging in

In order to use the CLI, you need to pass us your API key. To do so use the following command:

```
superai login --username {username}
```

Replace `{username}` with your super.AI account username.

When prompted, enter your password and press enter. You should see a confirmation like this:

```
Api key {api-key} was set
```

If you created your account through Google Sign-In, you will need to manually set your API key:

1. Find your API key in the super.AI dashboard by hovering over the profile icon in the lower left of the screen, then heading to API keys. You can copy the key by clicking on the copy (insert icon here) button. 
2. Provide your API key to the client by using the following command (replacing `{API-key}` with your actual API key):
      ```
      superai config --api-key {api-key}
      ```

## CLI commands

- `create_jobs`
- `list_jobs`
- `fetch_job`
- `get_job_responses`
- `cancel_job`
- `download_jobs`

- `fetch_batch_job`
- `fetch_batches_job`

- `create_ground_truth`
- `list_ground_truth_data`
- `get_ground_truth_data`
- `update_ground_truth`
- `delete_ground_truth_data`

## Python usage

The client allows you to run Python scripts on your machine to automate your work process. For example, you can use a script like this to create jobs:

```
import superai as ai

client = ai.Client("{api-key}")

client.create_jobs(
    app_id="{project-id}",
    inputs=[{"image_url":"https://cdn.super.ai/cool-bulldog.jpg"},{"image_url":"https://cdn.super.ai/hot-dog-01.jpeg"}]
)
```
