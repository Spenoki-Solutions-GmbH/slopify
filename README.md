# Chaplin

Your AI non-agent.

A wrapper around [siesta scripts](https://github.com/ihucos/siesta) to automate workflows.

## Open Source
Be carefull to not push company data in here.

## Implemented subcommands

| | |
| -------- | ------- |
| pick-ticket  | Implement a ticket in Jira    |
| pick-comment | Change local files to comply with request in GitHub comment     |
| ...    | ...add more here...    |

## Install
### 1. Clone this repo
```
git clone git@github.com:Spenoki-Solutions-GmbH/chaplin.git
```

### 2. Add to `$PATH`
```
export PATH="/path/to/chaplin/bin:$PATH"
```
### 3. Dependencies
* Setup: [jira-cli](https://github.com/ankitpokhrel/jira-cli)
* Setup: [GitHub CLI](https://cli.github.com/)
* Setup: [Ollama](https://ollama.com/download)
* Install siesta: `pip3 install git+https://github.com/ihucos/siesta.git`
* Run: `brew install fzf jq`

### 4. Configure
```ini
# ~/.chaplin.ini
[jira]
org=jira_org_name

[jira_labels]
label1=owner/repo1
label2=owner/repo2
```
Just hit me on chat and I send you the file.

## Example usage
```
chaplin pick-ticket
```

## Development Guidelines
* Apply the "Rule of three". Copy and paste three times before refactoring.
* Use the smallest model fit for the job.
* Use local models when practicable.
* Balance development speed, completion quality and model size.
* Use clear common sense prompts that solve one task at a time.
* Proper prompt formating does matter.
* This is a general but opiniated solution.
