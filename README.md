# Slopify

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
git clone git@github.com:Spenoki-Solutions-GmbH/slopify.git
```

### 2. Add to `$PATH`
```
export PATH="/path/to/slopify/bin:$PATH"
```
### 3. Dependencies
* Setup: [jira-cli](https://github.com/ankitpokhrel/jira-cli)
* Setup: [GitHub CLI](https://cli.github.com/)
* Setup: [Ollama](https://ollama.com/download)
* Install siesta: `pip3 install git+https://github.com/ihucos/siesta.git`
* Run: `brew install fzf jq`

### 4. Configure
```ini
# ~/.slopify.ini
[jira]
org=jira_org_name

[jira_labels]
label1=owner/repo1
label2=owner/repo2
```
Just hit me on chat and I send you the file.

## Example usage
```
slopify pick-ticket
```

## A case for non-agentic workflows

### Security
* Code can be audited
* No literally random arbitrary shell command execution (A traditional no-go in software development)

### Simplicity
* No sandboxing needed
* "Its just a few lines"
  
### Enviromental impact / Costs
* Forseable costs. A fixed number of API calls to the big models.
* Certain tasks can be handled locally.
* Hand-

### Control
* Error cases can be handled robustly.
* Precisely curate the context to the LLMs -> Better performance.
* Plan beforehand the best way to accomplish a task.
* No Vendor lock-in - plug and play different models depending on your needs.

### UX
Discoverability: users can see what you tool can do.


## Development Guidelines
* Apply the "Rule of three". Copy and paste three times before refactoring.
* Use the smallest model fit for the job.
* Use local models when practicable.
* Balance development speed, completion quality and model size.
* Use clear common sense prompts that solve one task at a time.
* Proper prompt formating does matter.
* This is a general but opiniated solution.
