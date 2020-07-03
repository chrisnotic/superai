# Super.AI API client

The super.AI Python library provides access to the super.AI API via Python and our command line interface (CLI). Full details of what you can use our API for are listed in our [API reference](https://super.ai/reference).

## Installation

In your terminal, run:

```
pip install superai
```

### Requirements

- A super.AI account. You will need to provide your account's API key in order to use this client. 
- The CLI included in this package uses Python 3. On systems that have both Python 2 and Python 3 installed, you may need to replace the calls to `python` and `pip`  with `python3` and `pip3`.
- Dependencies in this package rely on the clang build tools on Mac OS. If you have recently updated or installed XCode, you may be required to run `sudo xcodebuild -license` to begin with.

## Usage

Installing the CLI provides access to the stripe command.

```
superai [command]

# Run `--help` for detailed information about CLI commands
superai [command] --help
```

## CLI commands

`create_jobs`
`list_jobs`
`fetch_job`
`get_job_responses`
`cancel_job`
`download_jobs`

`fetch_batch_job`
`fetch_batches_job`

`create_ground_truth`
`list_ground_truth_data`
`get_ground_truth_data`
`update_ground_truth`
`delete_ground_truth_data`
