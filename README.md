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

### 5. Gemini API key
Go to https://aistudio.google.com/app/apikey to claim your gemini api key.
Set it to the environment:
```
export GEMINI_API_KEY=...
```

## Example usage
```
slopify pick-ticket
```

## A case for more non-agentic workflows

### Security
* No literally random arbitrary shell command execution (A traditional no-go in software development)
* Code can be audited


### Simplicity
* No sandboxing needed
* It's just a few hundert lines of script.
  
### Environmental impact / Costs
* Forseable costs. A fixed number of API calls to the big models.
* Certain LLM completions can be handled locally.
* Hand-pick the most economical model for the job.

### Control
* Error cases can be handled sanely at all.
* Precisely curate the context to the LLMs -> Better performance.
* Plan beforehand the best way to accomplish a task.
* No Vendor lock-in - plug and play different models depending on your needs.

### UX
* Discoverability: users can see what your tool can do.
* No need for users to oversee and rubber-stamp AIs intermediate steps.


## Development Guidelines
* Apply the "Rule of three". Copy and paste three times before refactoring.
* Use the smallest model fit for the job.
* Use local models when practicable.
* Balance development speed, completion quality and model size.
* Use clear common sense prompts that solve one task at a time.
* Proper prompt formating does matter.
* This is a general but opiniated solution.
